# User Feedback & Roadmap Platform — Feature & Functionality Survey

> Candidate #309 · Researched: 2026-05-03

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Canny | Commercial SaaS | Proprietary; free plan, paid from $99/mo | https://canny.io |
| Productboard | Commercial SaaS | Proprietary; from $19/maker/mo | https://www.productboard.com |
| Aha! Roadmaps | Commercial SaaS | Proprietary; from $59/user/mo | https://www.aha.io |
| Featurebase | Commercial SaaS | Proprietary; free plan, paid from $42/mo | https://www.featurebase.app |
| UserVoice | Commercial SaaS | Proprietary; enterprise ~$800–$2,000+/mo | https://www.uservoice.com |
| Gleap | Commercial SaaS | Proprietary; from $149/mo | https://www.gleap.io |
| Frill | Commercial SaaS | Proprietary; from $25/mo | https://frill.co |
| ClearFlask | Open Source | Apache 2.0; self-hosted or cloud | https://clearflask.com |
| Astuto | Open Source | MIT; self-hosted | https://github.com/astuto/astuto |
| Fider | Open Source | MIT; self-hosted | https://fider.io |

## Feature Analysis by Solution

### Canny

**Core features**
- Public and private feedback boards with upvoting
- Status workflow (Under Review, Planned, In Progress, Complete, Closed)
- Auto-notification of upvoters on status change
- Public changelog with rich-text entries and email distribution
- Roadmap view (Kanban-style board and timeline)
- AI-powered duplicate detection ("Autopilot") that auto-merges similar requests
- User segmentation by company, plan tier, or custom attributes
- Internal commenting and tagging for PM team

**Differentiating features**
- Autopilot AI: automatically identifies and merges near-duplicate feedback before it fragments votes
- 50+ native integrations: Jira, Linear, GitHub, HubSpot, Salesforce, Intercom, Slack, Teams, Zapier
- Revenue-weighted voting via CRM integration (shows ARR behind each request)
- SSO and custom domain whitelabelling

**UX patterns**
- Clean, minimal public portal; board/card layout familiar to Trello users
- In-app widget for embedding feedback collection inside the product
- Admin dashboard is information-dense but accessible for non-technical PMs

**Integration points**
- REST API (API key auth; base URL https://canny.io/api/v1) covering boards, posts, users, companies, votes, tags
- Webhooks (configurable per event type)
- Native Jira, Linear, GitHub (link posts to issues, sync status back)
- Zapier and Make (6,000+ downstream apps)
- HubSpot and Salesforce for revenue data overlay

**Known gaps**
- No built-in NPS or CSAT survey capability
- Limited analytics — no funnel or cohort views
- Price jumps steeply beyond 500 tracked users
- Cannot segment roadmap visibility by customer tier without workarounds
- No AI-generated changelog or spec drafting

**Licence / IP notes**
- Proprietary SaaS; no open-source components. Autopilot AI duplicate detection is a product feature, not a published patent.

---

### Productboard

**Core features**
- Centralised feedback inbox aggregating input from Intercom, Zendesk, Slack, email, and CSV import
- Customer segmentation linked to Salesforce and HubSpot CRM data
- User Impact Score: auto-calculated score surfacing top-requested features
- Prioritisation frameworks: RICE, WSJF, ROI — all modelable via formula builder
- Multiple roadmap view types: timeline, list, column (audience-switchable)
- Stakeholder-specific roadmap sharing (public link, embed, or PDF export)
- Objectives/OKR alignment layer connecting features to strategic goals
- Ideas portal (branded, public or private) for customer submissions

**Differentiating features**
- Deepest prioritisation framework support of any tool in the category
- Dynamic customer segmentation: slice impact scores by segment in real time
- OKR/strategy layer: trace every feature back to a business objective
- AI trend detection across feedback corpus (2026 addition)

**UX patterns**
- Complex dashboard; significant onboarding investment required
- Progressive disclosure in prioritisation views — score columns can be shown or hidden
- Separate "insights" module for tagging raw feedback notes to feature cards

**Integration points**
- REST API v2 (OAuth 2.0 and API token auth); full developer portal at developer.productboard.com
- Webhooks for feature status, note, and custom field change events
- Native: Jira, Azure DevOps, GitHub, Slack, Salesforce, Zendesk, Intercom, HubSpot, Google Sheets, Trello

**Known gaps**
- Steepest learning curve in category; not suitable for solo PMs or small teams
- Expensive for growing companies; per-maker pricing becomes prohibitive
- Changelog module is basic compared to dedicated tools
- No AI spec generation or changelog narrative drafting

**Licence / IP notes**
- Proprietary SaaS. Acquired by Zendesk in 2023.

---

### Aha! Roadmaps

**Core features**
- Visual product roadmaps: drag-and-drop timeline, release-based views, strategy maps
- Ideas portal with voting, scoring, and status updates
- Strategy module: business models, positioning, personas, OKRs
- Whiteboard integration with roadmaps (Q1 2026 addition)
- Releases and epics management connecting strategy to delivery milestones
- Custom workflow automation and configurable notification rules
- Audience-segmented roadmap publishing (internal, shared link, public)
- Reports and dashboards across product portfolio

**Differentiating features**
- Strongest strategy-to-delivery traceability in the market
- AI assistant "Elle" generates business model, positioning, persona drafts (2026)
- Portfolio-level roadmaps spanning multiple product lines
- Fully configurable scoring formulas for idea prioritisation

**UX patterns**
- Most complex UI in the category; enterprise PMs need weeks to master
- Heavy use of hierarchy (goals → initiatives → releases → features)
- Dedicated onboarding and CSM support at enterprise tier

**Integration points**
- REST API (OpenAPI-documented, available in JSON and Redocly formats)
- Three webhook types: activity (5-min delay), audit (live stream), integration (HTTP POST)
- Native: Jira, ADO, GitHub, GitLab, Salesforce, Slack, Teams, Zendesk, Trello

**Known gaps**
- Overkill for companies without multi-product portfolio complexity
- High per-user cost limits adoption across full product teams
- Public changelog not as polished as Canny or Featurebase
- No AI-powered feedback deduplication

**Licence / IP notes**
- Proprietary SaaS; bootstrapped and profitable. No open-source exposure.

---

### Featurebase

**Core features**
- Feedback boards with upvoting and comment threads
- Auto-notification to all upvoters when feature status changes
- AI duplicate detection (suggests merges before a request splits votes)
- Revenue-weighted voting (shows MRR behind each request)
- Public roadmap (Kanban-style; customisable branding)
- Changelog with in-app popup widget, email digest, and standalone page
- In-app feedback widget (embed snippet)
- NPS and CSAT survey module
- Customer segmentation by plan, company, or custom attributes
- Knowledge base module (help centre)

**Differentiating features**
- Generous free tier with unlimited feedback submissions
- Combined changelog + NPS + knowledge base in one tool — unusually complete for the price
- Revenue-weighted upvote display without needing a separate CRM connection
- In-app changelog popup boosts feature adoption after launch

**UX patterns**
- Fast setup; public portal live in under 10 minutes
- Clean, modern UI that feels consumer-grade
- Progressive feature disclosure — advanced modules (surveys, knowledge base) can be hidden until needed

**Integration points**
- REST API (API version 2026-01-01.nova); docs at docs.featurebase.app/rest-api
- Webhooks: HTTPS POST to configured URL, HMAC signature verification, idempotent event IDs
- Native: Slack, Linear, Jira, Intercom, HubSpot, Zendesk, ClickUp

**Known gaps**
- No strategy or OKR alignment layer
- No AI-generated spec or roadmap narrative
- Reporting is thinner than Productboard
- Roadmap timeline view absent (Kanban only)
- No audit log for enterprise compliance

**Licence / IP notes**
- Proprietary SaaS; no open-source components.

---

### UserVoice

**Core features**
- Idea forums with voting and status tracking
- Revenue and account-tier weighting on votes
- Advanced user segmentation and filtering
- Product discovery workflows with internal stakeholder input
- Salesforce deep integration (bi-directional idea sync and account data)
- Custom idea status workflows
- Internal roadmap (separate from public-facing portal)
- CSAT and NPS collection

**Differentiating features**
- Enterprise-grade access control and SSO
- Most mature Salesforce integration — account health data surfaces directly on ideas
- Separate internal and customer-facing roadmap views with fine-grained sharing controls
- Compliance features: audit logging, data residency options

**UX patterns**
- Feature-rich but dated UI compared to newer entrants
- Enterprise buyers value depth over aesthetics
- Onboarding assisted by dedicated CSM team

**Integration points**
- Admin API v2 (OAuth 2.0 and API key); developer portal at developer.uservoice.com
- Helpdesk API for end-user functionality
- Idea Collection API for custom mobile/web feedback capture
- Official SDKs: Python, C#, Java, PHP
- Native: Salesforce, Zendesk, Jira, Slack, HubSpot

**Known gaps**
- No public changelog module
- No AI duplicate detection
- High price point; unsuitable for small teams
- UI not modernised to match newer competitors

**Licence / IP notes**
- Proprietary SaaS; enterprise pricing only.

---

### Gleap

**Core features**
- In-app bug reporting with screenshots, session replays, and metadata capture
- Feature voting and public roadmap (integrated with the support platform)
- AI support agent "Kai" — auto-tags and categorises incoming feedback by topic
- Live chat and shared support inbox
- In-app surveys for quantifying demand
- Changelog and release notes
- Status update notifications when features move to Shipped
- Bug report annotations directly on screenshot

**Differentiating features**
- Only tool in the category that merges bug tracking + feature requests + live support in one platform
- Visual bug reports (annotated screenshots) enrich feature requests with reproduction context
- AI categorisation applied to all feedback types (bugs, features, support messages) uniformly

**UX patterns**
- Unified inbox approach — feature requests appear alongside bugs and support tickets
- Widget-first: all feedback originates from embedded in-app widget
- Optimised for mobile app developers as well as web teams

**Integration points**
- REST API documented at Postman (documenter.getpostman.com)
- Webhooks: HTTP POST to configured URL for all feedback types
- SDKs: JavaScript, iOS, Android, React Native, Flutter, Ionic, Node.js
- Native: Jira, Linear, Slack, Zapier, Intercom

**Known gaps**
- Feature voting is secondary to bug tracking — less sophisticated than Canny or Featurebase
- No revenue-weighted voting
- No prioritisation framework support
- Higher price for teams wanting only feedback management
- Roadmap view less polished than dedicated tools

**Licence / IP notes**
- Proprietary SaaS; JavaScript SDK is open source on GitHub (GleapSDK/JavaScript-SDK).

---

### Frill

**Core features**
- Idea collection board with public upvoting
- Public roadmap (three-column status view: Planned, In Progress, Shipped)
- Changelog / announcements module
- Email notification to submitter and upvoters on status change
- SSO embed (authenticate users via JWT)
- Custom branding and domain

**Differentiating features**
- Simplest setup of any tool surveyed; no configuration overhead
- API-first architecture: full REST API access at all paid tiers
- Strong GitHub and Jira integrations for developer-centric teams
- AI features in development (mentioned in roadmap)

**UX patterns**
- Minimal UI; deliberately avoids complexity
- Three-panel layout (Ideas / Roadmap / Changelog) visible from one navigation bar
- Embeddable widget and SSO via JWT for seamless in-app feel

**Integration points**
- REST API; developer portal at developers.frill.co
- Webhooks: HMAC-signed HTTP POST on idea created/updated/voted events; configurable from Settings → Webhooks
- Native: Jira, GitHub, Zapier (5,000+ apps via Zapier)

**Known gaps**
- No AI duplicate detection or sentiment analysis
- No revenue-weighted voting
- Limited reporting and segmentation (major complaint from reviewers)
- No NPS or CSAT surveys
- Survey count limited on lower plans

**Licence / IP notes**
- Proprietary SaaS; no open-source components.

---

### ClearFlask (Open Source)

**Core features**
- Feedback boards with voting and comment threads
- Public roadmap and status tracking
- Changelog with email notifications
- In-app widget
- Multi-project support
- Custom branding
- Polls and structured feedback forms
- SSO/OIDC support

**Differentiating features**
- Only self-hosted option with a comprehensive feature set comparable to Canny
- OpenAPI-defined internal API (frontend-to-backend communication is fully spec'd)
- AGPL-3.0 / Apache 2.0 licence permits self-hosting without vendor lock-in

**UX patterns**
- React frontend with SSR via Node.js Connect server
- Requires Java (Spring Boot) backend; non-trivial ops overhead

**Integration points**
- OpenAPI-specified REST API (internal spec publicly available on GitHub)
- Webhook support
- Self-hosted; integrations must be configured manually

**Known gaps**
- No AI features (deduplication, sentiment, prioritisation)
- Complex to self-host; requires 2 GB+ RAM
- Smaller ecosystem than commercial tools
- No revenue weighting or CRM integration

**Licence / IP notes**
- Apache 2.0 for the core; some components AGPL-3.0. Fully open source at github.com/clearflask/clearflask.

---

### Astuto (Open Source)

**Core features**
- Feature request boards with upvoting
- Status workflows (Planned, In Progress, Completed, Declined)
- Email notifications to voters on status change
- Admin dashboard for managing submissions
- Custom domain and branding
- Docker deployment

**Differentiating features**
- Lightest-weight open-source option; easiest to self-host
- MIT licence — no copyleft restrictions

**UX patterns**
- Simple, clean UI; deliberately minimal
- Onboarding requires only Docker and a domain

**Integration points**
- Basic REST API
- No native webhook support (community-requested)
- No third-party integrations beyond OAuth login providers

**Known gaps**
- No changelog module
- No roadmap view
- No AI features
- Very limited integrations
- Not suitable for enterprise use cases

**Licence / IP notes**
- MIT licence. Source at github.com/astuto/astuto.

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Public feedback board with upvoting
- Status workflow with email notification to upvoters on status change
- Public roadmap (minimum: Kanban-style three-column view)
- Changelog with searchable entries
- In-app embeddable widget for feedback collection
- Branding customisation (logo, colours, custom domain)
- At least basic REST API access for CRUD on posts and users
- Webhook events for feedback status changes
- Jira or Linear integration (common PM toolchain requirement)
- Slack notification for new submissions

### Differentiating Features
- AI duplicate detection and merge suggestions
- Revenue-weighted voting with CRM integration (Salesforce, HubSpot)
- NPS / CSAT survey integration in the same portal
- Strategy / OKR alignment layer tracing features to business goals
- Multiple roadmap view types (Kanban, timeline, list)
- Audience-segmented roadmap views (internal vs. customer-facing)
- AI auto-categorisation and tagging of incoming feedback
- In-app changelog popup widget to drive feature adoption
- Visual bug reports (screenshots, session replay) attached to feature requests
- SSO / OIDC for enterprise identity federation

### Underserved Areas / Opportunities
- AI-generated changelog narratives ("why we built this") from linked feedback themes
- AI-drafted specification from a high-upvote request (user stories, acceptance criteria)
- Sentiment and urgency scoring on raw submissions to prioritise PM review queue
- Revenue-weighted prioritisation in open-source tools (currently absent from all OSS options)
- Granular roadmap access control by customer tier without enterprise pricing
- Native mobile SDKs bundled with the core platform (most tools rely on third-party wrappers)
- Multi-product / portfolio roadmap view at affordable price points

### AI-Augmentation Candidates
- Duplicate detection and clustering: replaces manual review of near-identical submissions
- Sentiment and urgency analysis: flags emotionally charged or time-sensitive requests
- Auto-categorisation and tagging: eliminates manual PM triage of high-volume boards
- Changelog narrative generation: turns merged feedback clusters into customer-facing copy
- Spec drafting: converts an upvoted request into structured user stories for engineering handoff
- Revenue-impact prediction: estimates ARR influence of shipping a feature using CRM signal patterns

---

## Legal & IP Summary

No patents were identified for any features in this category. All commercial tools are proprietary SaaS with standard subscription licences; no open-source or copyleft obligations apply to the SaaS products. ClearFlask uses Apache 2.0 / AGPL-3.0, and Astuto uses MIT — both permit self-hosting and modification. Fider is MIT-licenced. Building an open-source tool in this space with an MIT or Apache 2.0 licence carries no known IP conflicts with existing products.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Public feedback board with upvoting, threaded comments, and status workflow
- Automated email notification to all upvoters on status change
- Public roadmap with at minimum a Kanban three-column view (Planned / In Progress / Shipped)
- Changelog with searchable entries and email distribution
- Embeddable in-app widget (JavaScript snippet)
- REST API (CRUD on posts, users, votes) with API key authentication
- Webhook events for post status changes
- Native integrations: Slack (notifications), Linear or Jira (issue linking)

**Should-have (v1.1)**
- AI duplicate detection with one-click merge suggestion
- Revenue-weighted voting via CRM webhook or CSV import
- OAuth 2.0 SSO / OIDC for enterprise identity federation
- In-app changelog popup widget to drive feature adoption post-launch
- NPS or CSAT micro-survey module within the same portal
- Roadmap timeline view as an alternative to Kanban
- Custom branding and white-label domain support

**Nice-to-have (backlog)**
- AI-generated changelog narrative from merged feedback clusters
- AI spec drafting from high-upvote request (user stories + acceptance criteria)
- Sentiment and urgency scoring on raw submissions
- Strategy / OKR alignment layer
- Audience-segmented roadmap sharing by customer tier
- Portfolio-level roadmap spanning multiple products
- MCP server exposing roadmap and feedback data to AI coding assistants
