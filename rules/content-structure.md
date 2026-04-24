---
paths:
  - "content/**"
  - ".blog-engine/**"
---

# Content Structure

## Blog Posts (`content/blog/*.mdx`)

```mdx
---
title: "Post Title Here"
slug: "url-slug-here"
date: "2026-03-15"
category: "AI Agents"
description: "Meta description under 160 characters."
readingTime: "8 min"
featured: false
---

Content in MDX...
```

**Blog categories** (defined in `lib/constants.ts`):
All, AI Automation, AI Agents, Workflow Automation, AI Tools, Case Studies, AI Strategy, Industry Guides

## Case Studies (`content/case-studies/*.mdx`)

Case studies use frontmatter for metrics, tech stack, and before/after data. They render with MetricsHero, TechStackBar, and BeforeAfterTable above the MDX body.

Current case studies (15):
ai-voice-agent-real-estate, saas-support-triage, enterprise-workflow-automation, crm-pipeline-automation-b2b, rag-chatbot-saas-support, ai-loyalty-rewards-platform, ecommerce-content-automation, ai-skin-analysis-ecommerce, cloud-telephony-sales-automation, automated-crypto-trading-platform, ai-hotel-management-system, ai-pos-restaurant-automation, ai-fleet-management-logistics, ai-legal-marketplace, ai-wellness-platform-fitelo
