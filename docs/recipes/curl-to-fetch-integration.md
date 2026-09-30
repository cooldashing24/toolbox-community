# Downstream Developer Recipe: Translating Chrome DevTools cURL to Modern TypeScript Fetch

> **Toolbox Resource**: [cURL to Code Converter](https://toolbox.vishnudigital.com/curl)  
> **Companion Engineering Guide**: [HTTP Security Headers Hardening Guide](https://blog.toolbox.vishnudigital.com/http-security-headers-hardening-guide/)  
> **Author**: Toolbox Engineering Team (`contact@toolbox.vishnudigital.com`)

---

## The Challenge: From Browser Network Tab to Production Code

During API integration and debugging, developers typically inspect network calls in Chrome or Firefox DevTools, right-click, and select **"Copy as cURL"**.

While cURL is great for terminal testing, converting a complex cURL command (with multi-line payloads, cookies, compressed encodings, and headers) into clean, type-safe TypeScript `fetch` calls often results in:
- Escaping syntax errors in JSON strings.
- Incompatible pseudo-headers (`:authority`, `:method`, `:path`).
- Accidental inclusion of compressed stream headers (`Accept-Encoding: gzip, deflate, br`) that break client-side automatic decompression.

---

## 1. Quick Translation via Toolbox

1. In DevTools Network tab, right-click any request and click **Copy** > **Copy as cURL**.
2. Open **[Toolbox cURL to Code Converter](https://toolbox.vishnudigital.com/curl)**.
3. Paste the terminal command.
4. Select **JavaScript Fetch (TypeScript)** to receive clean, production-ready source code.

---

## 2. Production-Grade Downstream Fetch Wrapper

Below is an idiomatic TypeScript wrapper demonstrating how to translate raw cURL structures into a resilient API client featuring abort timeouts, JSON serialization, and status validation:

```typescript
// ============================================================================
// Types & Options
// ============================================================================
export interface ApiRequestOptions extends RequestInit {
  timeoutMs?: number;
  params?: Record<string, string | number | boolean | undefined>;
}

export class ApiError extends Error {
  constructor(
    public status: number,
    public statusText: string,
    public data?: unknown
  ) {
    super(`API Error ${status}: ${statusText}`);
    this.name = "ApiError";
  }
}

// ============================================================================
// Robust Fetch Client
// ============================================================================
export async function executeTranslatedRequest<T = unknown>(
  url: string,
  options: ApiRequestOptions = {}
): Promise<T> {
  const { timeoutMs = 10000, params, headers = {}, body, ...restOptions } = options;

  // 1. Construct URL with query parameters
  const requestUrl = new URL(url);
  if (params) {
    Object.entries(params).forEach(([key, value]) => {
      if (value !== undefined) {
        requestUrl.searchParams.set(key, String(value));
      }
    });
  }

  // 2. Abort Controller for strict timeout guarantees
  const controller = new AbortController();
  const timeoutId = setTimeout(() => controller.abort(), timeoutMs);

  // 3. Normalize headers (Sanitize browser pseudo-headers)
  const normalizedHeaders = new Headers(headers);
  normalizedHeaders.delete(":authority");
  normalizedHeaders.delete(":method");
  normalizedHeaders.delete(":path");
  normalizedHeaders.delete(":scheme");

  // Let the browser/runtime set Host and Content-Length automatically
  normalizedHeaders.delete("host");
  normalizedHeaders.delete("content-length");

  try {
    const response = await fetch(requestUrl.toString(), {
      ...restOptions,
      headers: normalizedHeaders,
      body,
      signal: controller.signal,
    });

    if (!response.ok) {
      let errorBody: unknown;
      try {
        errorBody = await response.json();
      } catch {
        errorBody = await response.text();
      }
      throw new ApiError(response.status, response.statusText, errorBody);
    }

    // Parse JSON if response is application/json
    const contentType = response.headers.get("content-type") || "";
    if (contentType.includes("application/json")) {
      return (await response.json()) as T;
    }

    return (await response.text()) as unknown as T;
  } catch (error: unknown) {
    if (error instanceof Error && error.name === "AbortError") {
      throw new Error(`Request to ${url} timed out after ${timeoutMs}ms`);
    }
    throw error;
  } finally {
    clearTimeout(timeoutId);
  }
}
```

---

## 3. Example: Transformed cURL Command to Production Code

### Raw cURL Command:
```bash
curl 'https://api.example.com/v1/orders' \
  -H 'Authorization: Bearer sec_live_99214ab9' \
  -H 'Content-Type: application/json' \
  --data-raw '{"items":[{"sku":"PROD-101","qty":2}],"currency":"USD"}' \
  --compressed
```

### Downstream TypeScript Invocation:
```typescript
interface OrderResponse {
  orderId: string;
  totalAmount: number;
  status: string;
}

async function placeOrder() {
  const result = await executeTranslatedRequest<OrderResponse>(
    "https://api.example.com/v1/orders",
    {
      method: "POST",
      headers: {
        Authorization: "Bearer sec_live_99214ab9",
        "Content-Type": "application/json",
      },
      body: JSON.stringify({
        items: [{ sku: "PROD-101", qty: 2 }],
        currency: "USD",
      }),
      timeoutMs: 8000,
    }
  );

  console.log("Order confirmed:", result.orderId);
}
```

---

## Converting Other Languages
Need Python (`requests`, `httpx`), Go (`net/http`), Rust (`reqwest`), or Axios? Use **[Toolbox cURL to Code](https://toolbox.vishnudigital.com/curl)** to generate immediate, syntax-checked code for multi-language microservices.
