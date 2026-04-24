# Claude Code Skills, Agents & Orchestrators

A comprehensive collection of **1,276 skills**, **16 agents**, **2 custom meta-skills**, and **8 rules** for [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

Built and maintained by [Saksham Solanki](https://sakshamsolanki.com) as part of a production AI consulting practice.

## What's Inside

| Directory | Count | Description |
|-----------|-------|-------------|
| `skills/` | 1,276 | Invocable slash-command skills (832 platform automations + 444 strategy/content/SEO/growth skills) |
| `agents/` | 16 | Specialized sub-agents for blog pipeline, outreach, validation, and system orchestration |
| `custom-skills/` | 2 | Meta-skills: stochastic consensus and fan-out research patterns |
| `rules/` | 8 | Project rules for brand voice, design system, SEO, architecture, and agent contracts |

## Skills (1,276)

Each skill lives in its own directory with a `SKILL.md` file. Some include `references/`, `assets/`, and `scripts/` subdirectories.

### Strategy & Growth (444 skills)

Skills for SEO, content marketing, paid ads, conversion optimization, growth strategy, and more.

**SEO & Search**
`seo` `seo-audit` `seo-content` `seo-content-brief` `seo-content-writer` `seo-dataforseo` `seo-dominator` `seo-geo` `seo-google` `seo-hreflang` `seo-image-gen` `seo-images` `seo-local` `seo-maps` `seo-monitoring` `seo-page` `seo-plan` `seo-programmatic` `seo-schema` `seo-sitemap` `seo-strategy` `seo-technical` `seo-competitor-pages` `serp-analysis` `serp-analyzer` `serp-features` `search-console` `google-search-console` `keyword-research` `backlink-analysis` `backlink-analyzer` `backlink-audit` `schema-markup` `schema-markup-generator` `robots-txt` `xml-sitemap` `indexing` `indexnow` `canonical-tag` `heading-structure` `url-structure` `url-slug-generator` `internal-links` `internal-linking-optimizer` `site-crawlability` `on-page-seo-auditor` `domain-architecture` `domain-authority-auditor` `domain-selection` `featured-snippet` `entity-optimizer` `entity-seo` `meta-description` `meta-tags-optimizer` `title-tag` `open-graph` `twitter-cards` `core-web-vitals` `mobile-friendly` `image-optimization` `rendering-strategies` `technical-seo-checker` `content-quality-auditor` `geo-content-optimizer` `generative-engine-optimization` `ai-seo` `ai-traffic-tracking` `rank-tracker` `programmatic-seo`

**Blog & Content**
`blog` `blog-analyze` `blog-audio` `blog-audit` `blog-brief` `blog-calendar` `blog-cannibalization` `blog-chart` `blog-factcheck` `blog-geo` `blog-google` `blog-image` `blog-notebooklm` `blog-outline` `blog-page-generator` `blog-persona` `blog-repurpose` `blog-rewrite` `blog-schema` `blog-seo-check` `blog-strategy` `blog-taxonomy` `blog-write` `write-blog` `content-calendar` `content-creator` `content-gap-analysis` `content-machine` `content-marketing` `content-optimization` `content-refresher` `content-repurposing` `content-research-writer` `content-strategy` `content-writer` `copy-editing` `copywriting` `article-content` `thread-writer` `newsletter` `email-subject-lines`

**Paid Ads**
`ads` `ads-audit` `ads-budget` `ads-commander` `ads-competitor` `ads-creative` `ads-google` `ads-landing` `ads-linkedin` `ads-meta` `ads-microsoft` `ads-plan` `ads-tiktok` `ads-youtube` `ad-creative` `google-ads` `google-ads-report` `facebook-ads` `linkedin-ads` `meta-ads` `reddit-ads` `tiktok-ads` `youtube-ads` `ctv-ads` `display-ads` `native-ads` `app-ads` `directory-listing-ads` `paid-ads` `paid-ads-strategy` `competitive-ads-extractor` `campaign-analytics` `video-ad-analysis`

**Growth & Marketing**
`growth-funnel` `growth-strategist` `growth-strategy` `gtm-strategy` `launch-strategy` `cold-start-strategy` `pmf-strategy` `product-launch` `product-hunt-launch` `demand-gen` `lead-magnet` `outbound-engine` `cold-email` `email-marketing` `email-sequence` `referral-program` `affiliate-marketing` `influencer-marketing` `podcast-marketing` `video-marketing` `reddit-marketing` `distribution-channels` `integrated-marketing` `marketing-ideas` `marketing-psychology` `marketing-skills` `marketing-strategy-pmm` `marketing-demand-acquisition` `product-marketing` `product-marketing-context` `icp-builder` `competitor-analysis` `competitor-research` `competitor-alternatives` `traffic-analysis` `analytics-intel` `analytics-tracking` `google-analytics`

**Social Media**
`linkedin-content` `linkedin-posts` `twitter-x-posts` `twitter-algorithm-optimizer` `twitter-cards` `pinterest-posts` `reddit-posts` `medium-posts` `bluesky` `tiktok-captions` `social-content` `social-amplifier` `social-media-analyzer` `viral-content` `content-creator` `youtube-analytics` `youtube-seo`

**Conversion & CRO**
`conversion-optimization` `conversion-lab` `conversion-ops` `form-cro` `page-cro` `popup-cro` `onboarding-cro` `signup-flow-cro` `paywall-upgrade-cro` `churn-prevention` `retention-strategy` `ab-test-setup` `pricing-strategy`

**Page Generators**
`404-page-generator` `about-page-generator` `affiliate-page-generator` `alternatives-page-generator` `article-page-generator` `blog-page-generator` `careers-page-generator` `category-page-generator` `changelog-page-generator` `contact-page-generator` `contest-page-generator` `cookie-policy-page-generator` `customer-stories-page-generator` `disclosure-page-generator` `docs-page-generator` `download-page-generator` `faq-page-generator` `features-page-generator` `feedback-page-generator` `glossary-page-generator` `homepage-generator` `integrations-page-generator` `landing-page-generator` `legal-page-generator` `media-kit-page-generator` `migration-page-generator` `press-coverage-page-generator` `pricing-page-generator` `privacy-page-generator` `products-page-generator` `refund-page-generator` `resources-page-generator` `services-page-generator` `shipping-page-generator` `showcase-page-generator` `signup-login-page-generator` `solutions-page-generator` `startups-page-generator` `status-page-generator` `template-page-generator` `terms-page-generator` `tools-page-generator` `use-cases-page-generator`

**Design & UI**
`design-studio` `design-taste-frontend` `design-motion-principles` `frontend-design` `graphic-design` `svg-designer` `high-end-visual-design` `industrial-brutalist-ui` `minimalist-ui` `stitch-design-taste` `ui-ux-pro-max` `theme-factory` `shadcn` `tailwind-design-system` `web-design-guidelines` `brand-guidelines` `brand-visual-generator` `branding` `rebranding-strategy` `logo-generator` `favicon-generator` `carousel` `card` `grid` `masonry` `tab-accordion` `hero-generator` `footer-generator` `sidebar-generator` `navigation-menu-generator` `breadcrumb-generator` `cta-generator` `popup-generator` `social-share-generator` `top-banner-generator` `trust-badges-generator` `testimonials-generator` `newsletter-signup-generator` `toc-generator` `infographic-generator`

**Documents & Presentations**
`document-docx` `document-pdf` `document-pptx` `document-xlsx` `presentation-design` `motion-graphics` `canvas-design`

**Engineering & DevOps**
`dev-ops` `deploy-to-vercel` `vercel-deployment` `webapp-testing` `browserstack` `react-nextjs` `next-best-practices` `next-cache-components` `next-upgrade` `vercel-cli-with-tokens` `vercel-composition-patterns` `vercel-react-best-practices` `vercel-react-native-skills` `engineering-skills` `engineering-advanced-skills` `prisma-automation` `n8n-code-javascript` `n8n-code-python` `n8n-expression-syntax` `n8n-mcp-tools-expert` `n8n-node-configuration` `n8n-validation-expert` `n8n-workflow-patterns` `mcp-builder`

**Meta & Utility**
`init` `setup` `run` `fix` `eval` `list` `merge` `extract` `generate` `spawn` `loop` `connect` `connect-apps` `connect-automate` `review` `report` `status` `coverage` `challenge` `hard-call` `board` `board-prep` `find-skills` `skill-creator` `skill-share` `template-skill` `remember` `memory-management` `full-output-enforcement` `stochastic-consensus`

**Superpowers (Claude Code Meta-Skills)**
`superpowers-brainstorming` `superpowers-dispatching-parallel-agents` `superpowers-executing-plans` `superpowers-finishing-a-development-branch` `superpowers-receiving-code-review` `superpowers-requesting-code-review` `superpowers-subagent-driven-development` `superpowers-systematic-debugging` `superpowers-test-driven-development` `superpowers-using-git-worktrees` `superpowers-using-superpowers` `superpowers-verification-before-completion` `superpowers-writing-plans` `superpowers-writing-skills`

### Platform Automations (832 skills)

Each `*-automation` skill contains integration patterns, API references, and workflow templates for a specific platform. Covers CRMs, email tools, analytics, payments, cloud infrastructure, social platforms, and more.

<details>
<summary>Full list of 832 automation skills</summary>

Includes integrations for: Ably, Abstract, AbuseIPDB, Abyssale, Accelo, Accredible, AccuLynx, ActiveCampaign, AddressZen, Adobe, AdRapid, Adyntel, Aero Workflow, AeroLeads, Affinda, Affinity, AgencyZoom, AgentMail, AgentQL, Agenty, Agiled, Agility CMS, Ahrefs, AI/ML API, AIVoov, Alchemy, Algodocs, Algolia, AllImagesAI, Alpha Vantage, Altoviz, AltText AI, Amara, Amazon, Ambee, Ambient Weather, AmCards, Anchor Browser, Anonyflow, Anthropic, Apaleo, Apex27, API Bible, API Labz, API Ninjas, API Sports, Api2PDF, APIFlash, Apify, Apilio, ApiPie AI, APITemplate.io, APIVerve, Apollo, AppCircle, AppDrag, Appointo, AppsFlyer, AppVeyor, Aryn, Ascora, Ashby, ASIN Data API, Astica AI, Async Interview, Atlassian, Attio, Auth0, Autobound, Autom, Axonaut, Ayrshare, Backendless, BannerBear, Bart, BaseLinker, Baserow, Basin, BattleNet, BeaconChain, Beaconstac, Beamer, Beeminder, Bench, Benchmark Email, Benzinga, BestBuy, Better Proposals, Better Stack, Bidsketch, Big Data Cloud, BigMailer, BigML, BigPicture.io, Bitquery, Bitwarden, Blackbaud, Blackboard, BlockNative, BoldSign, Bolna, BoloForms, Bolt IoT, Bonsai, BookingMood, Booqable, Borneo, BotBaba, Botpress, Botsonic, BotStar, Bouncer, BoxHero, Braintree, Brandfetch, Breeze, Breezy HR, Brex, BrightData, BrightPearl, Brilliant Directories, BrowseAI, BrowserBase, BrowserHub, Browserless, BTCPay Server, Bubble, BugBug, BugHerd, Bugsnag, Buildkite, BuiltWith, BunnyCDN, ByteForms, CabinPanda, Cal.com, CalendarHero, CallerAPI, Callingly, CallPage, Campaign Cleaner, Campayn, Canny, Canvas, Capsule CRM, Carbone, Cardly, Castingwords, Cats, CDR Platform, Census Bureau, CentralStationCRM, Certifier, Chaser, ChatBotKit, ChatFAI, ChatWork, CHMeetings, Cincopa, Claid AI, ClassMarker, ClearOut, ClickMeeting, Clockify, CloudCart, CloudConvert, Cloudflare, Cloudinary, CloudLayer, CloudPress, Coassemble, Codacy, CodeInterpreter, CodeReadr, Coinbase, CoinMarketCal, CoinMarketCap, CoinRanking, College Football Data, Composio, Connecteam, ContentfulGraphQL, Contentful, Control-D, ConversionTools, ConvertAPI, Conveyor, Convolo AI, Corrently, Countdown API, Coupa, CraftMyPDF, Crowdin, CrustData, Cults, Curated, Currents API, CustomerIO, CustomGPT, CustomJS, Cutt.ly, D2L Brightspace, DaData.ru, Daffy, DailyBot, Datagma, DataRobot, Deadline Funnel, Deel, Deepgram, Demio, Detrack, DialMyCalls, Dialpad, Dictionary API, Diffbot, DigiCert, Digital Ocean, DiscordBot, Docsbot AI, Docsumo, DocuGenerate, Documenso, Documint, DocuPilot, DocuPost, DocuSeal, Doppler Marketing, Doppler SecretOps, DotSimple, Dovetail, DPD2, Draftable, DreamStudio, Drip Jobs, Dripcel, Dromo, Dropbox Sign, DropContact, Dungeon Fighter Online, Dynamics365, Echtpost, ElevenLabs, Elorus, Emailable, EmailListVerify, EmailOctopus, Emelia, Encodian, Endorsal, Enginemailer, Enigma, Entelligence, EODHD APIs, Epic Games, eSignatures.io, EspoCRM, eSputnik, eTermin, Evenium, Eventbrite, Eventee, Eventzilla, Everhour, Eversign, Exa, Excel, Exist, ExpoFP, Extracta AI, Facebook, FaceUp, Factorial, Feathery, Feishu/Lark, Felt, Fibery, Fidel API, Files.com, Fillout Forms, Finage, FindYMail, FinerWorks, Fingertip, FinMei, FireBerry, Firecrawl, Fireflies, Firmao, Fitbit, Fixer, Fixer.io, FlexiSign, Flowise AI, Flutterwave, FluxGuard, Folk, Fomo, ForceManager, FormBricks, FormCarry, FormDesk, FormSite, Foursquare, FraudLabs Pro, FreshBooks, Front, FullEnrich, GageList, Gamma, GAN AI, GatherUp, Gemini, Gender API, GenderAPI.io, Genderize, Geoapify, Geocodio, GeoKeo, GetForm, Gift Up, Gigasheet, Giphy, Gist, GiveButter, Gladia, Gleap, GlobalPing, GoDialer, Go To Webinar, Gong, Goodbits, Goody, Google (Admin, Address Validation, Ads, BigQuery, Calendar, Classroom, Cloud Vision, Docs, Drive, Maps, Meet, Photos, Search Console, Slides, Super, Tasks), Gorgias, GoSquared, Grafbase, GraphHopper, Griptape, Grist, Grokipedia, GroqCloud, Gumroad, Habitica, HackerNews, Happy Scribe, Harvest, Hashnode, Helcim, HelloLeads, Helpwise, Here, HeyGen, HeyReach, Heyzine, HigherGov, HighLevel, Honeybadger, HoneyHive, Hookdeck, HotspotSystem, HTML-to-Image, HumanITix, Humanloop, Hunter, HypeAuditor, Hyperbrowser, Hyperise, Hystruct, iCIMS, ICYPeas, Idea Scale, IdentityCheck, IgniSign, ImageKit, ImgBB, Imgix, InfluxDB Cloud, Insighto AI, Instacart, Instantly, Intelliprint, Interzoid, Invoice Organizer, IP2Location, IP2Proxy, IP2Whois, IPdata, IPinfo, IQAir, JigsawStack, JobNimbus, Jotform, JumpCloud, JungleScout, Kadoa, Kaggle, Kaleido, Keap, Keen.io, KickBox, Kit, Klipfolio, Ko-fi, Kommo, Kontent AI, Kraken.io, L2S, Labs64 NetLicensing, Landbot, Langbase, LangSmith, LastPass, Launch Darkly, Leadfeeder, Leadoku, Leiga, Lemlist, Lemon Squeezy, LessonSpace, Lever, Leverly, LexOffice, LinguaPop, LinkHut, LinkUp, ListClean, ListenNotes, LiveSession, LMNT, Lodgify, Logo.dev, Loomio, Loyverse, Magnetic, MailBluster, MailboxLayer, Mailcheck, Mailcoach, MailerLite, MailerSend, Mails.so, MailSoftly, MaintainX, ManyChat, Mapbox, Mapulus, MBouM, Melo, Mem, Mem0, MemberSpot, MemberStack, MemberVault, MetaAds, Metaphor, Mezmo, Microsoft (Clarity, Tenant), Minerstat, Missive, Mistral AI, Mocean, Moco, Modelry, Moneybird, MoonClerk, Moosend, Mopinion, More Trees, Moxie, Moz, MSG91, MX Technologies, MX Toolbox, Nango, Nano Nets, NASA, Nasdaq, NCScale, Needle, Neon, NetSuite, NeuronWriter, Neutrino, NeverBounce, New Relic, News API, NextDNS, Ngrok, Ninox, NoCRM.io, NPM, OCR Web Service, OCRSpace, Omnisend, OnceHub, OneDesk, OnePage, OneSignal, OpenAI, OpenCage, OpenGraph.io, OpenPerplex, OpenRouter, OpenWeather API, OptimoRoute, Owl Protocol, Page X, PandaDoc, Paradym, Parallel, Parma, ParseHub, Parsera, Parseur, Passslot, PassCreator, Payhip, PDF API, PDF.co, PDF4me, PDFless, PDFMonkey, PeopleDataLabs, Perigon, Perplexity AI, PersistIQ, Pexels, PhantomBuster, Piggy, Piloterr, Pilvio, Pingdom, Pipeline CRM, PlaceKey, Placid, Plain, Plasmic, PlateRecognizer, Plisio, Polygon, Polygon.io, Poptin, PostGrid, PostGrid Verify, Precoro, Prerender, PrintAutoPilot, Prismic, Process Street, Procfu, ProductBoard, ProductLane, Project Bubble, Proofly, ProxiedMail, Pushbullet, Pushover, Quaderno, Qualaroo, QuickBooks, Radar, Rafflys, Ragic, Raisely, Ramp, RavenSEOTools, Re:amaze, RealPhoneValidation, RecallAI, Recruitee, Refiner, Remarkety, Remote Retrieval, Remove.bg, RenderForm, RepairShopr, Replicate, Reply, Reply.io, Respond.io, Retailed, Retell AI, Retently, Rev AI, Revolt, Ring Central, Rippling, RiteKit, RKVST, Rocketlane, Rootly, Rosette, Route4Me, SafetyCulture, Sage, Salesforce (Marketing Cloud, Service Cloud), Salesmate, SAP SuccessFactors, SatisMeter, Scrape.do, ScrapeGraph AI, Scrapfly, ScrapingAnt, ScrapingBee, Screenshot.fyi, ScreenshotOne, Seat Geek, SecurityTrails, SegMetrics, Seismic, SemanticScholar, Semrush, Sendbird, Sendbird AI Chatbot, SendFox, Sendlane, Sendloop, SendSpark, Sensibo, Seqera, SerpAPI, SerpDog, Serply, ServiceM8, SevDesk, SharePoint, ShipEngine, Short.io, Short Menu, Shortcut, Shorten.rest, ShortPixel, ShotStack, Sidetracker, Signaturely, SignPath, SignWell, SimilarWeb, Simla.com, Simple Analytics, SimpleSat, SiteSpeakAI, Skyfire, Slack, SlackBot, SmartProxy, SmartRecruiters, SMS Alert, SMTP2GO, SmugMug, Snowflake, Sourcegraph, Splitwise, Spoki, Spondyr, Spotify, Spotlightr, SSLMate, Stack Exchange, Stannp, Starton, StatusCake, StoreGanise, StoreRocket, StormGlass.io, Strava, Streamtime, Supadata, SuperChat, SupportBee, SupportiveKoala, Survey Monkey, Svix, Sympla, SynthFlow AI, Taggun, TalentHR, Tally, Tapfiliate, TapForm, Tavily, TaxJar, TeamCamp, Telegram Bot, Telnyx, TelTel, Templated, Test App, Text-to-PDF, TextCortex, TextIt, TextRazor, Thanks.io, The Odds API, Thumbnail Creator, Ticketmaster, TickTick, TimeCamp, TimeKit, TimelinesAI, TimeLink, Timely, TinyURL, Tisane, Toggl, Token Metrics, Tomba, TomTom, ToneDen, TPS Check, TriggerCMD, TripAdvisor, Turbot Pipes, Turso, Twelve Data, Twitch, TwoCaptcha, Typefully, Typless, U301, UniOne, Updown.io, UploadCare, UptimeRobot, V0, Venly, Veo, VerifiedEmail, Veriphone, Vero, Vestaboard, VirusTotal, Visme, Waboxapp, Wachete, WaiverFile, Wakatime, WATI, Wave Accounting, WeatherMap, WebEx, WebScraping AI, WebVizio, WHAutomate, Winston AI, Wit.ai, Wiz, Wolfram Alpha, Woodpecker, Workable, Workday, Workiom, Worksnaps, Writer, Xero, Y.gy, Yandex, Yelp, YNAB, YouSearch, Zeplin, ZeroBounce, Zoho (Automation, Bigin, Books, Desk, Inventory, Invoice, Mail), ZoomInfo, Zylvie, Zyte API, and more.

</details>

## Agents (16)

Specialized sub-agents that run as autonomous workers within Claude Code.

### Blog Pipeline

| Agent | Purpose |
|-------|---------|
| `blog-orchestrator` | Coordinates the full blog pipeline: research, strategy, writing, editing, publishing |
| `blog-research` | SEO keyword research, SERP analysis, competitive gap identification |
| `blog-strategy` | Content outlines, heading hierarchy, keyword targets, internal link plans |
| `blog-writer` | Drafts blog posts following brand voice and SEO requirements |
| `blog-editor` | Quality review, fact-checking, brand compliance, SEO optimization |
| `blog-publisher` | Final formatting, MDX preparation, and publishing |
| `blog-monitor` | Content health monitoring, freshness scans, orphan page audits |

### Outreach Pipeline

| Agent | Purpose |
|-------|---------|
| `outreach-orchestrator` | LinkedIn outreach engine with Unipile delivery, multi-LLM research |
| `prospect-research` | Prospect enrichment using web search and data APIs |
| `lead-scorer` | Scores prospects against ICP and assigns routing tier |
| `message-personalizer` | Generates personalized outreach using score, sequence, and case study context |
| `comment-automator` | LinkedIn comment automation: discovers posts, generates and validates comments |
| `reply-classifier` | Classifies inbound replies and recommends next action |

### System

| Agent | Purpose |
|-------|---------|
| `system-supervisor` | Top-level workflow router for content, outreach, research, and ops |
| `run-validator` | Validates agent output contracts, failure classes, and promotion readiness |
| `outreach-validator` | Validates outbound research, scoring, and message assets |

## Custom Skills (2)

### Stochastic Consensus

Spawns N agents with the same or varied prompts to independently generate solutions, then finds statistical consensus and surfaces outliers. Use for strategic decisions, brainstorming, or any problem where "what am I missing?" matters.

### Fan-Out Research

Parallelizes research across multiple agents, each tackling a different angle, then synthesizes findings into a unified brief.

## Rules (8)

Project-scoped rules that govern how agents and skills operate.

| Rule | Purpose |
|------|---------|
| `agent-task-contract` | Operating contract for all agent workflows: objectives, constraints, failure classes |
| `brand-voice` | Voice guidelines, banned words, content accuracy standards |
| `design-system` | Color palette, typography, shadows, animations, icon rules |
| `site-architecture` | Routes, redirects, navigation structure, solutions taxonomy |
| `component-reference` | All component paths and purposes (layout, UI, graphics, content) |
| `css-architecture` | Global styles, utility classes, layer definitions |
| `content-structure` | Blog and case study frontmatter schemas, categories |
| `seo-infrastructure` | Schema types, SEO utilities, technical SEO, third-party integrations |

## Usage

### Installing Skills

Copy any skill directory into your project's `.claude/skills/` or symlink it:

```bash
# Copy a single skill
cp -r skills/seo-audit /path/to/project/.claude/skills/

# Symlink all skills
ln -s /path/to/SKILLS/skills/* /path/to/project/.claude/skills/
```

### Installing Agents

Copy agent files into `.claude/agents/`:

```bash
cp agents/*.md /path/to/project/.claude/agents/
```

### Installing Rules

Copy rule files into `.claude/rules/`:

```bash
cp rules/*.md /path/to/project/.claude/rules/
```

### Invoking Skills

Once installed, skills are available as slash commands in Claude Code:

```
/seo-audit
/blog-write
/ads-google
/competitor-analysis
/stochastic-consensus
```

## Structure

```
SKILLS/
  skills/           # 1,276 invocable skills
    seo-audit/
      SKILL.md
      references/   # (some skills include these)
      assets/
      scripts/
    blog-write/
      SKILL.md
    ...
  agents/            # 16 specialized sub-agents
    blog-orchestrator.md
    outreach-orchestrator.md
    system-supervisor.md
    ...
  custom-skills/     # 2 meta-skills
    stochastic-consensus/
      SKILL.md
    fan-out-research/
      SKILL.md
  rules/             # 8 project rules
    agent-task-contract.md
    brand-voice.md
    design-system.md
    ...
```

## License

MIT

## Author

[Saksham Solanki](https://sakshamsolanki.com) - AI Systems Architect
