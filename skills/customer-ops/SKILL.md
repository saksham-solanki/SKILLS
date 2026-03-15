---
name: customer-ops
description: >
  Customer success, support, feedback, surveys, retention, and community management. Use this skill
  whenever the user needs to handle customer support, gather feedback, reduce churn, build community,
  or improve customer experience. Trigger on: support, feedback, survey, churn, retention, community,
  help desk, NPS, customer success, ticket, review, testimonial, onboarding, customer experience.
---

# Customer Ops

You are the customer success center. Support, retain, and grow.

## Business Context

### NovaGems (Primary for this pillar)
- **130 clients**, need to reduce churn and increase expansion
- **Support**: Direct support model
- **Reviews**: Need Capterra, G2, GetApp optimization (Phase 4 of roadmap)

### SakshamSolanki.com
- **Client success**: Track ROI delivery for each engagement
- **Testimonials**: Need to collect from 15 past clients
- **Community**: AI Builders Club (newsletter + community)

## Sub-Skills to Use

| Task | Skill | When |
|------|-------|------|
| Help desk | `gorgias-automation`, `helpwise-automation`, `re-amaze-automation` | Support ticketing |
| Feedback collection | `canny-automation`, `formbricks-automation`, `productboard-automation` | Feature requests |
| NPS/CSAT | `satismeter-automation`, `simplesat-automation`, `retently-automation` | Satisfaction scores |
| Surveys | `survey-monkey-automation`, `qualaroo-automation`, `refiner-automation` | Customer surveys |
| Churn prevention | `churn-prevention` | Retention strategies |
| Reviews | `endorsal-automation`, `gatherup-automation` | Review collection |
| Community chat | `slack-bot`, `discord-bot`, `telegram-bot` | Community building |
| Customer messaging | `respond-io-automation`, `wati-automation`, `customerio-automation` | Multi-channel messaging |
| Customer engagement | `beamer-automation`, `userlist-automation` | In-app communication |
| Process workflows | `process-street-automation` | SOPs and checklists |
| Idea management | `idea-scale-automation` | Innovation management |
| Live chat | `landbot-automation`, `botsonic-automation` | Website chat |
| Customer analytics | `mopinion-automation`, `segmetrics-automation` | Customer behavior |

## Workflow Templates

### Review Collection Campaign (NovaGems)
1. `retently-automation` — send NPS survey to 130 clients
2. Promoters (9-10): `endorsal-automation` — request G2/Capterra review
3. Passives (7-8): `customerio-automation` — engagement campaign
4. Detractors (0-6): `canny-automation` — collect specific feedback, escalate

### Community Setup (SakshamSolanki.com)
1. `slack-bot` or `discord-bot` — set up AI Builders Club community
2. `beamer-automation` — announce new content/updates
3. `customerio-automation` — onboarding email sequence
4. `formbricks-automation` — regular pulse checks
