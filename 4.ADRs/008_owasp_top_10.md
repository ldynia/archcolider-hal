< [Back](README.md) < [Back to Home](../README.md#solution-structure)

# Security Response Headers

## Date

2021-11-02

## Status

Proposed

## Context

[The Open Web Application Security Project](https://owasp.org/) is an international non-profit organization dedicated to web application security. Organization created a document that describes [Top 10](https://owasp.org/Top10/) web applications vulnerabilities. One of the point talks about insecure response headers. We'd like to mitigate those threats.

## Decision

Following OWASP [secure headers documentation](https://owasp.org/www-project-secure-headers/), we will add below response headers to AWS API Gateway. This way our application will be compliant with OWASP.

| Header | Value |
| --- | --- |
| X-Frame-Options | deny |
| X-Content-Type-Options | nosniff |
| X-XSS-Protection | 1; mode=block |
| X-Permitted-Cross-Domain-Policies | none |
| Cross-Origin-Opener-Policy | same-origin |
| Cross-Origin-Resource-Policy | same-origin |
| Cross-Origin-Embedder-Policy | require-corp |
| Strict-Transport-Security | max-age=31536000; includeSubdomains; preload |
| Referrer-Policy | origin-when-cross-origin, strict-origin-when-cross-origin |
| Permissions-Policy | interest-cohort=() |
| Cache-Control | no-cache, no-store, must-revalidate |

We will create a [fitness function](https://en.wikipedia.org/wiki/Fitness_function), that will check security headers compliance. In the fitness function we will use security score obtained from https://securityheaders.com/  as a reference value.

## Consequences

**Positive:** Frontend and backend applications will be OWASP Top 10 compliant (from the perspective of response headers).

**Negative:** `Cache-Control: no-cache, no-store, must-revalidate` header will prevent resources from being cached, this might not be desirable functionality for frontend application that is Single Page Application (SPA).

**Risks:** There might be a spike of cross-origin errors, if encountered then the errors should be addressed and headers adjusted.

< [Back](README.md) < [Back to Home](../README.md#solution-structure)