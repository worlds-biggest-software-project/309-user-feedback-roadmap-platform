# User Feedback & Roadmap Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform for collecting user feedback, prioritising feature requests, and publishing public roadmaps and changelogs.

User Feedback & Roadmap Platform is an idea board, voting, roadmap, and changelog tool for product teams who want to run community-driven prioritisation without paying per-maker SaaS fees. It is aimed at PLG SaaS founders, product managers, and DevRel teams who need a transparent feedback loop with their users and currently choose between expensive incumbents (Productboard, Aha!) or feature-thin open-source options (Fider, Astuto).

---

## Why User Feedback & Roadmap Platform?

- Incumbent SaaS pricing escalates quickly — Canny starts at $99/month, Productboard at $19/maker/month, Aha! at $59/user/month, and Gleap at $149/month — pushing growing teams to either downgrade their process or pay enterprise rates.
- Existing open-source options (ClearFlask, Astuto, Fider) lack AI-powered duplicate detection, revenue-weighted voting, CRM integration, and modern roadmap views found in the commercial tools.
- AI-native features like feedback deduplication, sentiment scoring, and changelog narrative generation are emerging as the 2026 differentiator but are absent from every open-source option in the category.
- Per-user pricing is being replaced by flat pricing across the category, signalling buyer fatigue with seat-based billing — an opening for an open-source alternative with no seat tax.
- The feedback management sub-segment of the $12.5B product management market is growing faster than the parent category, driven by PLG companies prioritising community-led roadmapping.

---

## Key Features

### Feedback Collection & Voting

- Public and private feedback boards with upvoting and threaded comments
- Status workflow (Under Review, Planned, In Progress, Shipped, Closed) with auto-notification of all upvoters on status change
- Embeddable in-app JavaScript widget for in-product feedback capture
- User and company segmentation by plan tier, custom attributes, or CRM data
- Revenue-weighted voting that surfaces ARR/MRR behind each request

### Roadmap & Changelog Publishing

- Public roadmap with Kanban three-column view (Planned / In Progress / Shipped)
- Roadmap timeline view as an alternative to Kanban
- Changelog with searchable entries, email digest, and standalone page
- In-app changelog popup widget to drive feature adoption post-launch
- Custom branding, white-label domain, and audience-segmented sharing

### AI-Augmented Triage

- AI duplicate detection with one-click merge suggestion to prevent vote fragmentation
- Auto-categorisation and tagging of incoming feedback to remove manual PM triage
- Sentiment and urgency scoring on raw submissions to flag emotionally charged or time-sensitive requests
- AI-generated changelog narratives ("why we built this") synthesised from merged feedback clusters
- AI-drafted specifications converting high-upvote requests into user stories and acceptance criteria

### Integrations & API

- REST API with API-key authentication covering posts, users, votes, tags, and companies
- Webhook events for status changes, new submissions, and votes (HMAC-signed)
- Native integrations with Slack, Linear, Jira, GitHub, Intercom, HubSpot, and Salesforce
- OAuth 2.0 SSO / OIDC for enterprise identity federation
- NPS and CSAT micro-survey module within the same portal

---

## AI-Native Advantage

Existing open-source tools in this category have no AI features at all, while commercial incumbents are only beginning to ship duplicate detection and trend analysis. This project treats AI as a first-class layer: semantic clustering of submissions, sentiment and urgency scoring, revenue-weighted prioritisation that joins votes with CRM data, automated changelog narrative generation, and draft specifications produced from highly-upvoted requests. The combined effect is to remove the manual triage burden that currently consumes PM time and to close the feedback loop with customer-facing copy generated from the underlying request themes.

---

## Tech Stack & Deployment

The platform targets self-hosted and cloud deployment modes with an embeddable JavaScript widget for in-product capture. Public APIs follow REST conventions with OpenAPI documentation, HMAC-signed webhooks, and idempotent event IDs — patterns established by Featurebase, Frill, and Aha!. JSON Feed and RSS are supported for changelog distribution. Standards alignment includes GDPR/CCPA for feedback data, WCAG 2.1 for the public portal, and OAuth 2.0 / OIDC for SSO.

---

## Market Context

The product management software market reached $12.5 billion in 2024 and is growing at 12.4% CAGR, with the feedback management sub-segment estimated at $800M+ and growing faster than the parent category. Incumbent pricing ranges from $15/month (Upvoty) to $149/month (Gleap) for SMB tools, and $19–$59/maker/month for enterprise suites (Productboard, Aha!), with UserVoice enterprise plans reaching $800–$2,000+/month. Primary buyers are product managers at PLG SaaS companies, founders seeking transparent roadmap communication, customer success teams correlating requests to ARR, and DevRel teams publishing changelogs to developer communities.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
