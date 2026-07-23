---
name: Review cloud commitment coverage and savings
description: Read-only Archera flow to inspect an organization's commitment coverage, utilization, and savings metrics across AWS/Azure/GCP.
api: openapi/archera-openapi-original.json
operations:
  - GET /v1/orgs
  - GET /v1/org/{org_id}/metrics
  - GET /v1/org/{org_id}/commitments
  - GET /v1/org/{org_id}/commitments/chart
---

# Review cloud commitment coverage and savings

Use this skill to give a user a read-only picture of their Archera cloud
commitment posture. All calls are `GET` and require only `archera:read`.

## Auth
Send an API key in the `x-api-key` header, or an OAuth 2.0 bearer token
(Authorization Code + PKCE). See `authentication/archera-authentication.yml`.
Base URL: `https://api.archera.ai`.

## Steps
1. **Find the organization.** `GET /v1/orgs` and pick the target `org_id` (also
   visible in the app URL as `&orgId=<org_id>`).
2. **Pull headline metrics.** `GET /v1/org/{org_id}/metrics?provider=aws`
   (repeat per provider) for lifetime savings, coverage, and utilization.
3. **List active commitments.** `GET /v1/org/{org_id}/commitments` with the
   required `provider`, `start_date`, `end_date` query params. Page with
   `page` + `page_size`; the response carries `PaginationMetadata`
   (`total`, `next_page`, ...). Use `search`, `filter`, `order_by`, `desc` to refine.
4. **Chart the trend.** `GET /v1/org/{org_id}/commitments/chart` for the
   time-series view of committed vs on-demand spend.

## Conventions & errors
- Pagination is page-number based (`page`/`page_size`) — see `conventions/archera-conventions.yml`.
- Errors return the `ApiErrorResponse` JSON envelope (`message`, `code`,
  `timestamp`, `type`); 401 = bad/missing key, 403 = not permitted for the org.
  See `errors/archera-problem-types.yml`.
- This flow is read-only and safe to run without human approval.
