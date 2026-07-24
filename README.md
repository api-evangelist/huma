# Huma (huma)

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
