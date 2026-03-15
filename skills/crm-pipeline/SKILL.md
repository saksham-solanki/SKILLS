---
name: crm-pipeline
description: >
  Sales pipeline, CRM management, proposals, contracts, invoicing, and deal tracking. Use this skill
  whenever the user mentions CRM, pipeline, deals, proposals, contracts, invoicing, HubSpot, follow-ups,
  sales process, discovery calls, or client management. Trigger on: CRM, pipeline, deal, proposal,
  contract, invoice, HubSpot, follow-up, sales process, close, discovery, qualification, onboarding.
---

# CRM Pipeline

You are the sales operations center. Pipeline management, proposals, and deal flow.

## Business Context

### SakshamSolanki.com (Default)
- **CRM**: HubSpot (Free tier, upgrade at 10+ deals)
- **Pipeline stages**: 6 stages with custom properties
- **Discovery**: 45-min COI diagnostic + BANT, 70% listening ratio
- **Proposals**: 7 sections with ICP-specific variants
- **Follow-up**: 5-email sequence (21 days), 14 objection scripts
- **Offers**: Audit ($15-20K, 100% upfront), Sprint ($75-100K, 50/50), Transformation ($250-350K+, 30/30/30/10)
- **Past clients**: 15 unique clients for reactivation outreach
- **No pricing on website** — revealed on calls only

## Sub-Skills to Use

| Task | Skill | When |
|------|-------|------|
| HubSpot CRM | `hubspot` | HubSpot setup and management |
| Zoho CRM | `zoho-automation` or `zoho-bigin-automation` | Zoho ecosystem |
| Salesforce | `salesforce-service-cloud-automation` | Enterprise CRM |
| Pipeline CRM | `pipeline-crm-automation` or `attio-automation` | Pipeline tracking |
| Capsule CRM | `capsule-crm-automation` or `capsule_crm-automation` | Lightweight CRM |
| Proposals | `better-proposals-automation` or `bidsketch-automation` | Proposal creation |
| Contracts | `pandadoc-automation` or `docuseal-automation` | Contract management |
| E-signatures | `signwell-automation`, `dropbox-sign-automation`, `eversign-automation`, `boldsign-automation` | Digital signatures |
| Invoicing | `quickbooks-automation`, `freshbooks-automation`, `xero-automation`, `wave-accounting-automation` | Billing |
| Scheduling | `calendarhero-automation`, `oncehub-automation`, `cal-automation`, `googlemeet-automation` | Meeting booking |
| Sales engagement | `gong-automation` | Call recording and analysis |
| Follow-ups | `reply-automation`, `keap-automation` | Automated sequences |
| Lead scoring | `leadfeeder-automation` | Score and prioritize leads |

## Workflow Templates

### New Deal Flow (SakshamSolanki.com)
1. Lead comes in → `hubspot` to log deal
2. `calendarhero-automation` for scheduling discovery
3. Discovery call (COI diagnostic, 45 min, 70% listening)
4. `better-proposals-automation` for proposal
5. `pandadoc-automation` for contract
6. `quickbooks-automation` for invoice
7. 5-email follow-up sequence if no response

### Past Client Reactivation
1. Pull 15 past clients from `hubspot`
2. `email-sequence` for reactivation outreach
3. Track responses in pipeline
4. `calendarhero-automation` for booking expansion calls
