# Standards & API Reference

> Project: User Feedback & Roadmap Platform · Generated: 2026-05-03

## Industry Standards & Specifications

### ISO Standards

**ISO/IEC 27001:2022 — Information Security Management Systems**
URL: https://www.iso.org/standard/27001
Relevant because public feedback portals collect email addresses and personal data; SaaS operators storing user-submitted content must demonstrate information security governance to enterprise buyers. ISO 27001 certification is increasingly a procurement requirement.

**ISO/IEC 29101:2018 — Privacy Architecture Framework**
URL: https://www.iso.org/standard/45124.html
Defines a reference architecture for privacy protection in ICT systems. Applicable when designing consent flows, data retention policies, and user data deletion workflows for feedback platforms operating under GDPR and CCPA.

**ISO/IEC 27018:2019 — Protection of Personally Identifiable Information (PII) in Public Clouds**
URL: https://www.iso.org/standard/76559.html
Provides controls for cloud service providers handling PII. Relevant for platforms storing upvoter emails and CRM-linked customer profiles in multi-tenant SaaS infrastructure.

---

### W3C & IETF Standards

**WCAG 2.2 — Web Content Accessibility Guidelines**
URL: https://www.w3.org/TR/WCAG22/
Published as a W3C Recommendation on 5 October 2023. Level AA compliance is the legal expectation under the EU European Accessibility Act (in force June 2025) and US ADA/Section 508. Public-facing feedback portals and roadmap pages must meet Level AA, covering keyboard navigation, focus indicators, contrast ratios, and form labelling. Enterprise buyers now require a VPAT 2.5 documenting compliance.

**RFC 4287 — Atom Syndication Format**
URL: https://datatracker.ietf.org/doc/html/rfc4287
Defines the XML-based Atom feed format used by changelog RSS/Atom feed endpoints, which allow developer communities and aggregators to subscribe to product update streams. A common pattern in this category.

**RFC 5023 — Atom Publishing Protocol (AtomPub)**
URL: https://datatracker.ietf.org/doc/html/rfc5023
Defines an application-level protocol for publishing and editing web resources using HTTP and XML. Used in changelog publication workflows where external systems programmatically create changelog entries.

**JSON Feed Version 1.1**
URL: https://www.jsonfeed.org/version/1.1/
A pragmatic JSON alternative to Atom and RSS for changelog syndication, introduced in 2017 and widely adopted for developer-facing content. Easier to implement than XML-based Atom and increasingly preferred for modern SaaS changelogs.

**RFC 6749 — OAuth 2.0 Authorization Framework**
URL: https://datatracker.ietf.org/doc/html/rfc6749
Foundation for delegated authorisation. Required for any integration that allows third-party tools (Jira, Salesforce, Slack) to access platform data on behalf of users without sharing credentials. Also required for SSO implementations.

**RFC 7591 — OAuth 2.0 Dynamic Client Registration Protocol**
URL: https://datatracker.ietf.org/doc/html/rfc7591
Defines mechanisms for dynamically registering OAuth 2.0 clients with an authorisation server. Relevant for marketplace integrations where third-party developers register their apps at runtime without manual admin intervention.

**RFC 7617 — HTTP Basic Authentication**
URL: https://datatracker.ietf.org/doc/html/rfc7617
Foundational HTTP authentication scheme; often used for simple API-key-based access (API key passed as bearer or POST parameter) in feedback platform APIs.

**RFC 8288 — Web Linking**
URL: https://datatracker.ietf.org/doc/html/rfc8288
Defines the `Link` HTTP header for pagination and resource discovery in REST APIs. Used in changelog and post listing endpoints with cursor-based pagination.

**OpenID Connect Core 1.0**
URL: https://openid.net/specs/openid-connect-core-1_0.html
Identity layer on top of OAuth 2.0 used for SSO. Required when enterprise customers authenticate portal users via their corporate identity provider (Okta, Azure AD, Google Workspace). Featurebase, Canny, and UserVoice all expose SSO via OIDC/SAML.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1.0**
URL: https://swagger.io/specification/
The standard for describing REST APIs, including webhook definitions (introduced in 3.1.0 via the `webhooks` object). Feedback platforms (Aha!, ClearFlask) publish OpenAPI definitions for their APIs. A new platform should provide an OpenAPI 3.1 spec for both its REST endpoints and its webhook payload schemas.

**JSON Schema (Draft 2020-12)**
URL: https://json-schema.org/specification
Used for defining and validating webhook payload structures and API request/response bodies. Webhook consumers rely on stable JSON Schema definitions to auto-generate client code and validate incoming payloads.

**Semantic Versioning 2.0.0**
URL: https://semver.org/
Convention for changelog versioning. Widely expected by developer communities consuming a SaaS product changelog; structured changelog entries should map release identifiers to SemVer strings where applicable.

---

### Security & Authentication Standards

**OWASP Top 10 (2021)**
URL: https://owasp.org/www-project-top-ten/
Security baseline for web application development. Public feedback portals are exposed to injection attacks (A03), broken access control (A01), and security misconfiguration (A05). API endpoints accepting user-generated content are particularly at risk.

**OWASP API Security Top 10 (2023)**
URL: https://owasp.org/www-project-api-security/
Specific guidance for REST APIs: covers broken object-level authorisation (API1), excessive data exposure (API3), and lack of rate limiting (API4). All of these are directly applicable to the feedback platform's public API and webhook delivery system.

**HMAC-SHA256 for Webhook Signature Verification**
Not a standalone RFC; a best-practice pattern (used by Stripe, GitHub, Featurebase, Frill). Webhook payloads should include an HMAC-SHA256 signature in a request header so consumers can verify authenticity and prevent replay attacks. Featurebase and Frill both implement this pattern.

**GDPR — General Data Protection Regulation (EU) 2016/679**
URL: https://gdpr-info.eu/
Applies directly: feedback portals collect voter email addresses and link them to CRM identities. Requirements include lawful basis for processing, right to erasure ("forget me"), data portability, and breach notification. Fines up to €20M or 4% of global annual turnover.

**CCPA — California Consumer Privacy Act**
URL: https://oag.ca.gov/privacy/ccpa
US equivalent to GDPR for California residents. Feedback platforms with US customers must honour data deletion requests and provide opt-out mechanisms for the sale of personal data.

**EU European Accessibility Act (EAA)**
URL: https://ec.europa.eu/social/main.jsp?catId=1202
Entered into force June 2025. Mandates WCAG 2.2 Level AA compliance for digital products and services sold in the EU market. Enterprise procurement now requires VPAT 2.5 documentation.

---

### MCP Server Specifications

**Model Context Protocol (MCP) — Anthropic**
URL: https://modelcontextprotocol.io/
An open protocol for exposing structured data and tools to AI coding assistants and agents. A feedback and roadmap platform could expose an MCP server providing tools for: querying top-voted features, retrieving roadmap status, creating changelog entries, and fetching feedback clusters. The 2026 MCP roadmap adds stateless Streamable HTTP transports suitable for SaaS deployment.

**MCP Streamable HTTP Transport**
URL: https://modelcontextprotocol.io/development/roadmap
The 2026 production transport for MCP servers; enables stateless horizontal scaling — appropriate for a multi-tenant SaaS platform where each tenant's workspace is isolated. An MCP server for the platform could allow AI agents to query "what are the top 10 feature requests with the most ARR behind them?" without bespoke API integration.

---

## Similar Products — Developer Documentation & APIs

### Canny

- **Description:** The most-established dedicated feedback and roadmap tool; REST API covering boards, posts, users, votes, companies, comments, and changelog entries.
- **API Documentation:** https://developers.canny.io/api-reference
- **SDKs/Libraries:** Community JavaScript wrapper (canny-js on GitHub); Python via dltHub (open-source data pipeline library); no official SDK.
- **Developer Guide:** https://help.canny.io/en/articles/4195400-the-canny-api
- **Standards:** REST/JSON; API key authentication via POST parameter or `x-api-key` header; no OpenAPI spec published.
- **Authentication:** API key (secret key from Company Settings).

---

### Productboard

- **Description:** Product management platform with the deepest feature prioritisation capabilities; REST API v2 for features, notes, components, releases, and custom fields.
- **API Documentation:** https://developer.productboard.com/
- **SDKs/Libraries:** No official SDK; Postman collection published at postman.com/pb-stargate/productboard-public-api.
- **Developer Guide:** https://developer.productboard.com/reference/introduction
- **Standards:** REST/JSON; OpenAPI; supports both API token and OAuth 2.0 for third-party integrations.
- **Authentication:** API Access Token (Bearer) or OAuth 2.0 with scoped permissions.

---

### Aha! Roadmaps

- **Description:** Enterprise product management suite; REST API covers ideas, features, releases, goals, initiatives, epics, and webhook configuration.
- **API Documentation:** https://www.aha.io/api
- **SDKs/Libraries:** No official SDK; API documented via Redocly and available as an OpenAPI JSON spec.
- **Developer Guide:** https://www.aha.io/api/integrating-aha
- **Standards:** REST/JSON; OpenAPI 3.x spec available; three webhook types (activity, audit, integration).
- **Authentication:** OAuth 2.0 (user-delegated) and API key.

---

### Featurebase

- **Description:** Fast-growing all-in-one feedback, roadmap, changelog, and NPS tool; REST API at API version 2026-01-01.nova covering posts, boards, users, companies, and changelog entries.
- **API Documentation:** https://docs.featurebase.app/rest-api
- **SDKs/Libraries:** No official SDK; JavaScript embed snippet for in-app widget.
- **Developer Guide:** https://docs.featurebase.app/guides
- **Standards:** REST/JSON; webhooks documented with HMAC-SHA256 signature verification and idempotent event IDs.
- **Authentication:** API key.

---

### UserVoice

- **Description:** Enterprise feedback and product discovery platform; provides three distinct APIs for admin operations, helpdesk, and custom idea capture.
- **API Documentation:** https://developer.uservoice.com/
- **SDKs/Libraries:** Official SDKs: Python, C#, Java, PHP (all on developer.uservoice.com).
- **Developer Guide:** https://developer.uservoice.com/docs/api/v2/getting-started/
- **Standards:** REST/JSON; OAuth 2.0 and API key authentication; no public OpenAPI spec.
- **Authentication:** OAuth 2.0 (Admin API v2) and API key (Helpdesk API).

---

### Gleap

- **Description:** In-app bug reporting, feature voting, live chat, and changelog platform with multi-platform SDKs; REST API documented via Postman.
- **API Documentation:** https://documenter.getpostman.com/view/18586034/2s8YRiJYVC
- **SDKs/Libraries:** Official SDKs: JavaScript (npm/yarn), iOS (Swift), Android (Kotlin), React Native, Flutter, Ionic/Capacitor, Node.js — all open source on GitHub (GleapSDK org).
- **Developer Guide:** https://docs.gleap.io/introduction
- **Standards:** REST/JSON; webhook delivery to configured HTTPS endpoint for all feedback types.
- **Authentication:** SDK token (client-side) and API key (server-side).

---

### Frill

- **Description:** Lightweight feedback, roadmap, and changelog tool with a clean developer API; positioned as the simplest full-featured option.
- **API Documentation:** https://developers.frill.co/
- **SDKs/Libraries:** No official SDK; JavaScript embed snippet for widget.
- **Developer Guide:** https://help.frill.co/article/93-webhooks
- **Standards:** REST/JSON; HMAC-signed webhooks on idea created, updated, and voted events.
- **Authentication:** API key.

---

### ClearFlask (Open Source Reference)

- **Description:** Open-source self-hosted feedback and roadmap platform; OpenAPI-specified internal API between React frontend and Spring Boot backend.
- **API Documentation:** https://github.com/clearflask/clearflask
- **SDKs/Libraries:** No official SDK; full source code available for forking.
- **Developer Guide:** https://clearflask.com/open-source
- **Standards:** REST/JSON; OpenAPI spec for frontend-backend communication; Docker-based deployment.
- **Authentication:** Session cookie (internal); configurable OIDC/SSO for portal users.

---

## Notes

**Emerging: MCP as a first-class integration surface.** As AI coding assistants become standard in product team workflows, exposing roadmap and feedback data via an MCP server is an emerging differentiator. No existing tool in this category has shipped a production MCP server as of May 2026, representing a clear first-mover opportunity.

**Webhook standards are converging.** HMAC-SHA256 signature headers (as used by Stripe, GitHub, Featurebase, and Frill) are becoming the de-facto standard for webhook authenticity verification. New entrants should adopt this pattern from day one.

**OpenAPI 3.1 webhook definitions.** The `webhooks` object in OpenAPI 3.1 enables webhook payload schemas to be documented alongside REST endpoints in a single spec file, enabling auto-generated client libraries and validation tooling for webhook consumers. This is an underused pattern in this category.

**WCAG 2.2 Level AA is now a compliance floor, not a nice-to-have.** As of June 2025 (EU EAA enforcement), enterprise buyers in the EU require VPAT 2.5 documentation. Teams building public portals must budget for accessibility auditing from the start.
