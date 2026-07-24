---
name: Submit a Huma module result and review flags
description: >-
  Submit a patient measurement / ePRO / questionnaire result to a Huma deployment
  and review clinician-flagged results, grounded in real Module Results operations.
api: openapi/huma-platform-openapi-original.yml
operations:
  - "api_extensions_v1_user_retrieve_[retrieve_user_profile]"
  - "api_extensions_v1_public_module_create_[create_module_result]"
  - "api_extensions_v1_user_flagged_modules_retrieve_[retrieve_unseen_module_results]"
  - "api_extensions_v1_user_module_result_sign_create_[update_module_result_status_sign]"
---

# Submit a Huma module result and review flags

Use this skill to capture a patient-reported or device measurement into Huma and
surface it for clinical review.

## Preconditions
- A valid Huma JWT (see `skills/huma-backend-token-exchange.md`).
- The target `user_id` and the module `shortcode` / `module_id` from your deployment.

## Steps
1. Confirm the patient with **`api_extensions_v1_user_retrieve_[retrieve_user_profile]`**
   (`GET /api/extensions/v1/user/{user_id}`).
2. Submit the result with **`api_extensions_v1_public_module_create_[create_module_result]`**
   (`POST /api/extensions/v1/public-module/{shortcode}`).
3. Pull clinician-flagged / unseen results with
   **`api_extensions_v1_user_flagged_modules_retrieve_[retrieve_unseen_module_results]`**
   (`GET /api/extensions/v1/user/{user_id}/flagged-modules`).
4. Sign off a reviewed result with
   **`api_extensions_v1_user_module_result_sign_create_[update_module_result_status_sign]`**
   (`POST /api/extensions/v1/user/{user_id}/module-result/{module_id}/sign`).

## Conventions
- List endpoints page with `skip` / `limit` (`conventions/huma-conventions.yml`).
- Writes are not idempotent — do not blindly retry a failed submission.
- This is CE-marked / EU MDR Class IIb medical-device software; treat clinical data
  and sign-off actions as safety-relevant (`agentic-access/huma-agentic-access.yml`).
