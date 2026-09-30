# Downstream Developer Recipe: Safe Client-Side JWT Decoding & Expiry Auditing

> **Toolbox Resource**: [JWT Token Inspector](https://toolbox.vishnudigital.com/jwt-decoder)  
> **Companion Engineering Guide**: [JWT Claims & Security 101 Guide](https://blog.toolbox.vishnudigital.com/jwt-security-101-decode-inspect-claims-guide/)  
> **Author**: Toolbox Engineering Team (`contact@toolbox.vishnudigital.com`)

---

## The Challenge: Inspecting Tokens Client-Side Without Bloat or Security Traps

Single-Page Applications (React, Next.js, Vue) frequently need to inspect JWT claims to:
- Determine whether an access token has expired before dispatching an API request.
- Read non-sensitive user identity claims (e.g., `sub`, `name`, `roles`) to update UI routing state.
- Schedule optimistic token refresh cycles.

However, many applications introduce vulnerable or bloated third-party dependencies, or make the mistake of trusting client-side claims for **authorization decisions**.

---

## Strict Security Rules for Client-Side JWT Handling

1. **Inspection $\neq$ Verification**: Client-side decoding only reveals claims; it does **NOT** cryptographically verify the signature. Authorization must always be enforced on your backend API using secret or public keys.
2. **Never Store Tokens in Unprotected LocalStorage**: Prefer HttpOnly, Secure, SameSite cookies for sensitive session tokens. If using in-memory access tokens, refresh them silently via an HttpOnly refresh cookie.
3. **Audit Claims Offline**: During development or debugging, inspect tokens using **[Toolbox JWT Inspector](https://toolbox.vishnudigital.com/jwt-decoder)** running in browser RAM rather than pasting bearer tokens into online formatters that log HTTP requests.

---

## Native, Dependency-Free Client-Side JWT Helper (TypeScript)

The following lightweight utility decodes RFC 7519 Base64Url tokens using native browser APIs (`atob`, `TextDecoder`) without adding external bundle dependencies:

```typescript
// ============================================================================
// Types
// ============================================================================
export interface StandardJwtPayload {
  iss?: string;      // Issuer
  sub?: string;      // Subject (User ID)
  aud?: string | string[]; // Audience
  exp?: number;      // Expiration time (UNIX epoch in seconds)
  nbf?: number;      // Not before (UNIX epoch in seconds)
  iat?: number;      // Issued at (UNIX epoch in seconds)
  jti?: string;      // JWT ID
  [key: string]: unknown;
}

export interface JwtInspectionResult<T = StandardJwtPayload> {
  header: Record<string, unknown>;
  payload: T;
  isExpired: boolean;
  expiresInSeconds: number | null;
}

// ============================================================================
// Base64Url Decoder (RFC 4648 Section 5)
// ============================================================================
function decodeBase64Url(base64UrlString: string): string {
  // Convert Base64Url to standard Base64:
  // '-' -> '+', '_' -> '/', add padding '='
  let base64 = base64UrlString.replace(/-/g, "+").replace(/_/g, "/");
  const pad = base64.length % 4;
  if (pad === 2) base64 += "==";
  else if (pad === 3) base64 += "=";

  // Safe UTF-8 decoding in browser environments
  const binaryString = window.atob(base64);
  const bytes = Uint8Array.from(binaryString, (c) => c.charCodeAt(0));
  return new TextDecoder().decode(bytes);
}

// ============================================================================
// Safe Parser & Expiry Calculator
// ============================================================================
export function inspectJwtClientSide<T = StandardJwtPayload>(
  token: string,
  clockToleranceSeconds: number = 30
): JwtInspectionResult<T> | null {
  if (!token || typeof token !== "string") return null;

  const parts = token.trim().split(".");
  if (parts.length !== 3) {
    console.warn("Invalid JWT structure: Expected exactly 3 segments separated by dots.");
    return null;
  }

  try {
    const rawHeader = decodeBase64Url(parts[0]);
    const rawPayload = decodeBase64Url(parts[1]);

    const header = JSON.parse(rawHeader) as Record<string, unknown>;
    const payload = JSON.parse(rawPayload) as T & StandardJwtPayload;

    // Check expiration
    const nowEpochSeconds = Math.floor(Date.now() / 1000);
    let isExpired = false;
    let expiresInSeconds: number | null = null;

    if (typeof payload.exp === "number") {
      expiresInSeconds = payload.exp - nowEpochSeconds;
      // Consider expired if within clock drift tolerance
      isExpired = expiresInSeconds <= clockToleranceSeconds;
    }

    return {
      header,
      payload,
      isExpired,
      expiresInSeconds,
    };
  } catch (error) {
    console.error("Failed to decode JWT segments:", error);
    return null;
  }
}
```

---

## Example Usage: Optimistic Token Refresh in Fetch Interceptor

```typescript
async function fetchWithAutoRefresh(url: string, currentToken: string, refreshTokenFn: () => Promise<string>) {
  const inspection = inspectJwtClientSide(currentToken);

  let activeToken = currentToken;

  // If token is expired or expires within 30 seconds, trigger refresh proactively
  if (!inspection || inspection.isExpired) {
    console.log("Token expired or nearing expiration. Initiating silent refresh...");
    activeToken = await refreshTokenFn();
  }

  return fetch(url, {
    headers: {
      Authorization: `Bearer ${activeToken}`,
      "Content-Type": "application/json",
    },
  });
}
```

---

## Live Debugging & Security Auditing
Before deploying custom auth flows, test your tokens for common misconfigurations (such as Key Confusion attacks, missing `exp` claims, or invalid `aud` parameters) on **[Toolbox JWT Token Inspector](https://toolbox.vishnudigital.com/jwt-decoder)**.
