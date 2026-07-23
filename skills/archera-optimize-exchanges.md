---
name: Optimize commitments via exchange recommendations
description: Archera flow to review recommended exchanges (returning and repurchasing commitments to improve efficiency) and apply them.
api: openapi/archera-openapi-original.json
operations:
  - GET /v1/org/{org_id}/exchanges/recommendations
  - POST /v1/org/{org_id}/exchanges/recommendations/apply
---

# Optimize commitments via exchange recommendations

Use this skill to improve an organization's commitment efficiency by exchanging
(returning + repurchasing) existing commitments per Archera's recommendations.
The apply step is a **write**.

## Auth
`x-api-key` header or OAuth 2.0 bearer token; apply needs `archera:write`.
Base URL `https://api.archera.ai`. See `authentication/archera-authentication.yml`.

## Steps
1. **Get exchange recommendations.** `GET /v1/org/{org_id}/exchanges/recommendations`
   returns the recommended returns/purchases and the projected savings delta.
2. **Summarize the trade-off** for the user: what is returned, what is bought,
   and the net savings (`ExchangeRecommendationDelta`).
3. **Apply.** `POST /v1/org/{org_id}/exchanges/recommendations/apply` with the
   selected recommendation payload (`ApplyExchangeRecommendationsArgs`).
   **Get explicit user confirmation first** — this returns and repurchases real
   commitments.

## Conventions & errors
- Idempotency is not supported; on a timeout, re-fetch recommendations rather
  than replaying the apply (`conventions/archera-conventions.yml`).
- A 409 Conflict indicates the underlying commitments changed — refresh and
  retry. Errors use the `ApiErrorResponse` envelope
  (`errors/archera-problem-types.yml`).
