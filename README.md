# Huma (huma)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Huma (Huma Therapeutics Limited) is a United Kingdom-headquartered digital health and remote patient monitoring company providing a regulated, configurable platform for building and running healthcare and life-sciences applications. Huma Workspace lets clinical teams assemble no-code apps, connected-device data capture, ePRO questionnaires, algorithm-based assessments, and a clinician portal for telemedicine and remote monitoring, while a backend Integration API and native iOS/Android/Angular SDKs let developers embed Huma functionality into first-party applications. Huma operates as CE-marked / MDR Class IIb medical-device software and is ISO 13485 and ISO 27001 certified, and is used across the NHS in its UK home market, pharma, and clinical-trials programs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/huma/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/huma/refs/heads/main/apis.yml)

## Tags

- Healthcare
- United Kingdom
- Remote Patient Monitoring
- Telehealth
- Digital Health
- Clinical Trials
- SDK
- Medical Device Software
- Population Health

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Huma Integration API

Backend Integration API for embedding Huma platform functionality into first-party applications. Authentication uses a Workspace-issued `huma-config.json` (client-credentials style); a backend service exchanges its own authenticated user for a Huma token via login/register, then calls Huma backend methods. Access is gated behind a Huma Workspace account. No public HL7 FHIR CapabilityStatement or downloadable OpenAPI is published.

- **Human URL:** [https://docs.huma.com/api-integration/intro](https://docs.huma.com/api-integration/intro)
- **Base URL:** `https://workspace-gcp-uk.api.huma.com/api/integration/v1`

#### Properties

- [Documentation](https://docs.huma.com/api-integration/intro)
- [Getting Started](https://docs.huma.com/quick-start/backend/)

### Huma Mobile & Web SDK

Software development kits for building or enhancing applications with out-of-the-box Huma functionality across iOS, Android, and Angular — covering authentication/authorization, connected Device Kit, charts, questionnaires, modules, messaging, call kit, and object storage.

- **Human URL:** [https://docs.huma.com/sdk/next/intro](https://docs.huma.com/sdk/next/intro)

#### Properties

- [Documentation](https://docs.huma.com/sdk/next/intro)
- [Getting Started](https://docs.huma.com/quick-start/intro)

## Common Properties

- [Website](https://huma.com/)
- [Developer Portal](https://docs.huma.com/)
- [Documentation](https://docs.huma.com/)
- [Getting Started](https://docs.huma.com/quick-start/intro)
- [GitHub Organization](https://github.com/huma-engineering)
- [Status Page](https://status.huma.com/)
- [Sign Up / Workspace](https://workspace.huma.com/)
- [Security](https://docs.huma.com/trust-security/)
- [Compliance](https://docs.huma.com/trust-security/compliance/)
- [Privacy Policy](https://huma.com/legal/website-privacy-policy)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
