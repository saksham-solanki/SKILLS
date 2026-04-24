---
paths:
  - "app/**"
  - "next.config.mjs"
  - "lib/constants.ts"
---

# Site Architecture

## Live Routes

```
/                           Homepage (hero + dashboard mockup + flow + inbox + results + solutions + club + blog + CTA)
/how-it-works               3-tier AI Revenue System deep-dive (Launch/Scale/Dominate) with mockups per tier
/solutions                  Custom AI Solutions (3 tiers + 4 categories + process + PreQualificationForm)
/case-studies               Case study listing
/case-studies/[slug]        Individual case study (MetricsHero + TechStackBar + BeforeAfterTable + MDX)
/ai-builders-club           Community + newsletter landing (Skool + Beehiiv + topics + activity feed + FAQ)
/blog                       Blog listing (filterable by category)
/blog/[slug]                Individual blog post (MDX)
/about                      Headshot + story + what I do + beliefs
/newsletter                 Newsletter signup page (BeehiivForm)
/newsletter/[slug]          Individual newsletter issue
/melih                      Private proposal page for Melih deal (not in nav)
```

## Redirects

```
/consulting  -->  /solutions        (permanent, in next.config.mjs and page.tsx)
/services    -->  /solutions        (permanent, in next.config.mjs and page.tsx)
/resources   -->  /ai-builders-club (in page.tsx)
```

## API Routes

```
/api/qualify      Pre-qualification form submission handler
/api/indexnow     IndexNow URL submission to search engines
```

## Navigation

```
[Logo]   How It Works | Solutions | Case Studies | AI Builders Club | Blog   [Book a Call]
```

- Component: `TubelightNav` (tubelight-style active indicator)
- "Book a Call" always visible as CTA button in nav
- About page in footer only, not main nav
- Mobile: hamburger menu
- Defined in `lib/constants.ts` as `navLinks`

## Custom AI Solutions Structure

### 4 Solution Categories

1. **Operations Automation**: internal workflow, data processing, document handling
2. **Customer-Facing AI**: chatbots, voice agents, support triage
3. **Sales & Revenue AI**: pipeline automation, lead scoring, outbound
4. **Industry-Specific Systems**: vertical solutions for specific industries

### 3 Engagement Tiers

| Tier         | Name                       | Timeline   | Deliverable                              |
|--------------|----------------------------|------------|------------------------------------------|
| Entry Point  | AI Opportunity Audit       | 2-3 weeks  | AI Opportunity Report + Roadmap          |
| Core Offer   | AI Operations Sprint       | 45-60 days | Production AI systems + training         |
| Enterprise   | AI Transformation Program  | 3-6 months | Multi-system deployment + optimization   |
