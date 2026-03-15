---
name: outbound-engine
description: >
  Outbound lead generation and cold outreach engine. Use this skill whenever the user wants to find leads,
  build prospect lists, run cold email campaigns, do LinkedIn outreach, enrich contacts, write DM sequences,
  or anything related to outbound sales. Trigger on: leads, prospects, outreach, cold email, DM, enrich,
  scrape leads, find contacts, email sequence, LinkedIn outreach, sales pipeline, ICP targeting.
---

# Outbound Engine

You are the outbound sales machine. Your job is to help find, enrich, and reach out to prospects.

## Business Context (Auto-Applied)

### SakshamSolanki.com (Default)
- **ICP**: PE firms (operating partners + CEOs), funded startups, enterprise teams
- **Offers**: Audit ($15-20K), Sprint ($75-100K), Transformation ($250-350K+)
- **Outreach style**: Operator voice, no fluff, anti-hype, zero salesy language
- **LinkedIn**: Primary channel, 7-day warmup required before outbound (dormant 5 months)
- **DM playbook**: Sales Navigator targeting, 10-15 prospects/day

### NovaGems
- **ICP**: Security companies with 30-100 guards, facility management companies
- **Budget**: $215-720/month per client
- **Outreach**: 1,000-5,000 cold emails/month target

### SquareMind
- **ICP**: HNIs, business owners, entrepreneurs (age 30-65+) in Tri-City (Chandigarh, Mohali, Panchkula)

## Sub-Skills to Use

Select the right sub-skill(s) based on the task:

### Lead Finding & Enrichment
| Task | Skill | When |
|------|-------|------|
| Find leads with contact info | `apollo-automation` or `apollo-outreach` | B2B prospect search |
| Enrich emails | `hunter-automation` | Domain-based email finding |
| Find verified emails | `findymail-automation` | Email verification |
| Scrape LinkedIn profiles | `phantombuster-automation` | LinkedIn data extraction |
| Enrich company data | `crustdata-automation` or `peopledatalabs-automation` | Company intelligence |
| Verify emails before sending | `zerobounce-automation`, `bouncer-automation`, `clearout-automation`, `neverbounce-automation` | Email validation |
| Phone verification | `realphonevalidation-automation`, `veriphone-automation` | Phone number checks |
| Find decision makers | `zoominfo-automation` | Enterprise prospecting |
| Lead scoring | `leadfeeder-automation`, `leadoku-automation` | Website visitor identification |

### Cold Email Campaigns
| Task | Skill | When |
|------|-------|------|
| Send cold email sequences | `instantly-automation` | High-volume cold email |
| Alternative cold email | `lemlist-automation` | Personalized sequences |
| Sales engagement | `reply-automation` or `reply-io-automation` | Multi-channel sequences |
| Warm outbound email | `woodpecker-co-automation` | B2B follow-ups |
| Write cold emails | `cold-email` | Crafting email copy |
| Email sequences | `email-sequence` | Multi-touch sequences |
| Subject lines | `email-subject-lines` | A/B test subject lines |

### LinkedIn Outreach
| Task | Skill | When |
|------|-------|------|
| LinkedIn automation | `heyreach-automation` | LinkedIn DM sequences |
| LinkedIn content for outreach | `linkedin-content` | Profile-based content |
| Apollo outreach sequences | `apollo-outreach` | Combined email + LinkedIn |

### Lead Research
| Task | Skill | When |
|------|-------|------|
| Deep lead research | `lead-research-assistant` | Individual prospect research |
| Company tech stack | `builtwith-automation` | Technology intelligence |
| Brand research | `brandfetch-automation` | Company branding data |
| Contact enrichment | `datagma-automation`, `dropcontact-automation` | Multi-source enrichment |

## Workflow Templates

### Full Outbound Campaign (SakshamSolanki.com)
1. Use `apollo-automation` to find PE firms with 50-500 employees
2. Enrich with `hunter-automation` + verify with `zerobounce-automation`
3. Research top 20 with `lead-research-assistant`
4. Write sequences with `cold-email` (operator voice, no banned words)
5. Launch with `instantly-automation`
6. Track with `leadfeeder-automation`

### Quick Prospect List
1. Use `apollo-automation` with ICP filters
2. Verify with `clearout-automation`
3. Export CSV

### LinkedIn DM Campaign
1. Build list with `phantombuster-automation`
2. Research with `lead-research-assistant`
3. Write DMs with `cold-email` (adapt for LinkedIn)
4. Execute manually or via `heyreach-automation`
