---
paths:
  - "components/**"
  - "app/**/page.tsx"
---

# Component Reference

## Layout Components

| Component       | Path                                    | Purpose                                       |
|-----------------|-----------------------------------------|-----------------------------------------------|
| TubelightNav    | `components/layout/TubelightNav.tsx`    | Main navigation with tubelight active indicator|
| Footer          | `components/layout/Footer.tsx`          | Site footer                                   |
| FooterWrapper   | `components/layout/FooterWrapper.tsx`   | Client wrapper for footer                     |

## UI Components

| Component              | Path                                          | Purpose                         |
|------------------------|-----------------------------------------------|---------------------------------|
| Button                 | `components/ui/Button.tsx`                    | CTA buttons (filled/outlined)   |
| Badge                  | `components/ui/Badge.tsx`                     | Category/tag pills              |
| SectionLabel           | `components/ui/SectionLabel.tsx`              | ALL CAPS eyebrow (`.section-label`) |
| Container              | `components/ui/Container.tsx`                 | Max-width wrapper (1280px)      |
| Section                | `components/ui/Section.tsx`                   | Section wrapper with padding    |
| Logo                   | `components/ui/Logo.tsx`                      | Site logo                       |
| BeehiivForm            | `components/ui/BeehiivForm.tsx`               | Newsletter signup embed         |
| LogoMarquee            | `components/ui/LogoMarquee.tsx`               | Scrolling logo strip            |
| InteractiveHoverButton | `components/ui/interactive-hover-button.tsx`  | Hover-animated button           |
| Spotlight              | `components/ui/spotlight.tsx`                 | Spotlight effect                |

## Graphics Components

| Component              | Path                                              | Purpose                                    |
|------------------------|---------------------------------------------------|--------------------------------------------|
| BrowserFrame           | `components/graphics/BrowserFrame.tsx`            | Browser window wrapper                     |
| DashboardMockup        | `components/graphics/DashboardMockup.tsx`         | Stats, bar chart, lead pipeline            |
| EmailInboxMockup       | `components/graphics/EmailInboxMockup.tsx`        | Fake email inbox with reply threads        |
| SystemFlowDiagram      | `components/graphics/SystemFlowDiagram.tsx`       | 5-step vertical pipeline                   |
| TerminalMockup         | `components/graphics/TerminalMockup.tsx`          | Code/config in terminal style              |
| BeforeAfterTable       | `components/graphics/BeforeAfterTable.tsx`        | Before vs after metrics                    |
| MetricsHero            | `components/graphics/MetricsHero.tsx`             | Animated metric counters (case studies)    |
| TechStackBar           | `components/graphics/TechStackBar.tsx`            | Tool logo pills horizontal                 |
| ToolLogoGrid           | `components/graphics/ToolLogoGrid.tsx`            | Grid of 20 tool logos                      |
| ContentPipelineMockup  | `components/graphics/ContentPipelineMockup.tsx`   | SEO content pipeline visualization         |
| SEODashboardMockup     | `components/graphics/SEODashboardMockup.tsx`      | SEO analytics dashboard                    |
| AdDashboardMockup      | `components/graphics/AdDashboardMockup.tsx`       | Ad performance dashboard                   |
| FlywheelDiagram        | `components/graphics/FlywheelDiagram.tsx`         | Circular revenue flywheel                  |
| TierComparisonTable    | `components/graphics/TierComparisonTable.tsx`     | 3-tier feature comparison (no pricing)     |
| MetricCounter          | `components/graphics/MetricCounter.tsx`           | Single animated metric counter             |
| PipelineDiagram        | `components/graphics/PipelineDiagram.tsx`         | Pipeline visualization                     |
| CaseStudyArchitecture  | `components/graphics/CaseStudyArchitecture.tsx`   | Architecture diagram for case studies      |

## Content Components

| Component             | Path                                           | Purpose                            |
|-----------------------|------------------------------------------------|------------------------------------|
| BlogCard              | `components/blog/BlogCard.tsx`                 | Blog post card for listings        |
| InlineCTA             | `components/blog/InlineCTA.tsx`                | Mid-article CTA for AI Builders Club|
| NewsletterSignup      | `components/blog/NewsletterSignup.tsx`         | End-of-article newsletter embed    |
| CaseStudyCard         | `components/case-studies/CaseStudyCard.tsx`    | Case study card for listings       |
| MetricsBar            | `components/case-studies/MetricsBar.tsx`       | Horizontal metrics display         |
| ResourceCard          | `components/resources/ResourceCard.tsx`        | Resource download card             |
| PreQualificationForm  | `components/PreQualificationForm.tsx`          | Multi-step form on /solutions      |

## Proposal Components (Private)

Located in `components/proposal/`. Used only on `/melih`:
ScrollProgress, ProposalNav, ProposalHero, ProposalVideo, CurrentStateAudit, CompetitorGap, ProcessTimeline, PlatformStrategy, BlogRestructure, PricingTiers, ProposalCTA, SampleContent
