---
name: Review and apply a recommended commitment plan
description: Archera flow to fetch a recommended commitment plan, inspect its line items and savings comparison, then apply it (a write action).
api: openapi/archera-openapi-original.json
operations:
  - GET /v1/org/{org_id}/commitment-plans/recommended
  - GET /v1/org/{org_id}/commitment-plans/{plan_id}/line-items
  - GET /v1/org/{org_id}/commitment-plans/{plan_id}/comparison
  - POST /v1/org/{org_id}/commitment-plans/{plan_id}/apply
---

# Review and apply a recommended commitment plan

Use this skill to move a user from a recommendation to a committed purchase.
The final step is a **write** — treat it as consequential.

## Auth
`x-api-key` header or OAuth 2.0 bearer token. The apply step needs
`archera:write`. See `authentication/archera-authentication.yml`.

## Steps
1. **Get the recommendation.** `GET /v1/org/{org_id}/commitment-plans/recommended`
   to obtain the recommended plan and its `plan_id` (or use
   `.../commitment-plans/default`).
2. **Inspect line items.** `GET /v1/org/{org_id}/commitment-plans/{plan_id}/line-items`
   to see each commitment the plan would purchase.
3. **Confirm the savings.** `GET /v1/org/{org_id}/commitment-plans/{plan_id}/comparison`
   to compare offers and expected savings before committing.
4. **Apply.** `POST /v1/org/{org_id}/commitment-plans/{plan_id}/apply` with the
   purchase spec. **Confirm with the user first** — this places real cloud
   commitments and cannot be assumed. A 409 Conflict means the plan state
   changed; re-fetch the recommendation and retry.

## Conventions & errors
- No idempotency-key is supported, so never blind-retry the apply on a
  network timeout — re-read commitment state first (`conventions/archera-conventions.yml`).
- Errors use the `ApiErrorResponse` envelope; 422 = semantically invalid apply
  request. See `errors/archera-problem-types.yml`.
