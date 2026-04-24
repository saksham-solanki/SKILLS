---
paths:
  - "lib/seo.ts"
  - "app/**/page.tsx"
  - "app/**/layout.tsx"
  - "next.config.mjs"
---

# SEO Infrastructure

## Schema Types Used

| Schema         | Where                                    |
|----------------|------------------------------------------|
| Organization   | Homepage (root layout)                   |
| Person         | /about                                   |
| Article        | /blog/[slug], /case-studies/[slug]       |
| BreadcrumbList | All content pages                        |
| FAQPage        | /ai-builders-club, /how-it-works         |

## SEO Utilities (`lib/seo.ts`)

- `generateSEO()`: meta tags, OG, Twitter cards, canonical URL, robots
- `generateArticleSchema()`: Article structured data
- `generateBreadcrumbSchema()`: Breadcrumb structured data
- `generateOrganizationSchema()`: Organization structured data
- `generatePersonSchema()`: Person structured data
- `generateFAQSchema()`: FAQ structured data

## Technical SEO

- Static generation (SSG) for blog and case study pages
- Auto-generated sitemap
- IndexNow integration via `/api/indexnow`
- Canonical URLs on every page
- OG images configured (default at `/og/default.png`)
- Image optimization: AVIF + WebP formats, lazy loading
- Meta descriptions under 160 characters

## Third-Party Integrations

| Service          | Usage                                                                    |
|------------------|--------------------------------------------------------------------------|
| **Beehiiv**      | Newsletter embeds, magic link: `https://magic.beehiiv.com/v1/0f35a2f0-422a-44cb-be39-e45c6d09d2da` |
| **Skool**        | Community: `https://www.skool.com/ai-builders-club-3219`                 |
| **Calendly**     | Booking: `https://calendly.com/work-samsolanki/30min`                    |
| **Lucide React** | Icon library (outline style)                                             |
| **Fontshare CDN**| Satoshi font (via @font-face in globals.css)                             |
