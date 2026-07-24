---
name: Huma backend token exchange
description: >-
  Exchange a Workspace-issued huma-config.json for a Huma platform JWT from a
  backend service, then act as the signed-in integration user. Grounds the
  login/register flow documented in the Huma backend quick-start.
api: openapi/huma-platform-openapi-original.yml
operations:
  - "api_integration_v1_auth_signin_create_[sign_in]"
  - "api_integration_v1_auth_sign_consent_create_[sign_consent]"
  - "api_auth_v1_me_retrieve_[me]"
  - "api_auth_v1_refreshtoken_create_[refresh_token_v1]"
---

# Huma backend token exchange

Use this skill to authenticate a backend service to the Huma Platform / Integration
API and obtain a JWT it can use for subsequent calls.

## Preconditions
- A `huma-config.json` downloaded from the Huma Workspace (contains API credentials).
- A Huma Workspace account with the Integration API enabled.

## Auth model
- All calls use `Authorization: Bearer <jwt>` (JWT auth) or `Authorization: Hawk ...`
  (Hawk MAC) — see `authentication/huma-authentication.yml`.
- The JWT carries `projectId` and `clientId` in its user claims.

## Steps
1. Sign in the integration user with **`api_integration_v1_auth_signin_create_[sign_in]`**
   (`POST /api/integration/v1/auth/signin`). Supply the user email, client type and
   deployment id sourced from your Workspace config. On success you receive tokens
   and a `uid`. (Per the backend quick-start, a `403` means the user does not exist —
   fall back to your registration flow.)
2. If consent is required, sign it with
   **`api_integration_v1_auth_sign_consent_create_[sign_consent]`**
   (`POST /api/integration/v1/auth/sign-consent`).
3. Verify the session with **`api_auth_v1_me_retrieve_[me]`** (`GET /api/auth/v1/me`).
4. Before the access token expires, refresh with
   **`api_auth_v1_refreshtoken_create_[refresh_token_v1]`**
   (`POST /api/auth/v1/refreshtoken`).

## Conventions
- No idempotency key is supported — do not assume safe retries on writes
  (`conventions/huma-conventions.yml`).
- Errors return `application/json` (not RFC 9457); handle `400`/`404`
  (`errors/huma-problem-types.yml`).
