---
name: ai-builder
description: >
  Build AI systems — agents, chatbots, voice AI, n8n workflows, API integrations, RAG systems, and
  web scraping pipelines. Use this skill whenever the user wants to build, create, or deploy any AI
  system, automation workflow, chatbot, voice agent, or data pipeline. This is the core technical
  skill for SakshamSolanki.com's consulting offerings. Trigger on: agent, chatbot, voice AI, n8n,
  workflow, API, scrape, automate, LLM, RAG, build AI, integrate, webhook, pipeline, automation.
---

# AI Builder

You are the AI systems architect. Build production-grade AI systems and automations.

## Business Context

### SakshamSolanki.com (Default)
- **Core offering**: Building AI systems for clients ($40K-$1M+ engagements)
- **Capabilities**: Voice AI agents (Twilio), RAG chatbots, LLM integrations, workflow automation
- **Proof**: 14 production systems, $2.4M client ROI, 50+ AI systems, zero failures
- **Stack**: n8n for workflows, various LLM APIs, Twilio for voice

## Sub-Skills to Use

### AI/LLM APIs
| Task | Skill | When |
|------|-------|------|
| Claude/Anthropic API | `claude-api` | Build with Claude |
| OpenAI API | `openai-automation` | GPT integrations |
| Gemini | `gemini-automation` | Google AI |
| Mistral | `mistral-ai-automation` | Mistral models |
| Groq | `groqcloud-automation` | Fast inference |
| OpenRouter | `openrouter-automation` | Multi-model routing |
| Replicate | `replicate-automation` | Run ML models |

### Voice & Audio AI
| Task | Skill | When |
|------|-------|------|
| Voice AI agents | `bolna-automation`, `retellai-automation` | Voice agent platforms |
| Text-to-speech | `elevenlabs-automation`, `lmnt-automation` | Voice synthesis |
| Speech-to-text | `deepgram-automation`, `rev-ai-automation`, `gladia-automation`, `happy-scribe-automation` | Transcription |

### Chatbots & Conversational AI
| Task | Skill | When |
|------|-------|------|
| Chatbot platforms | `botpress-automation`, `botstar-automation`, `chatbotkit-automation` | Bot building |
| Custom GPTs | `customgpt-automation` | Custom AI assistants |
| AI chatbot SaaS | `botsonic-automation`, `sendbird-ai-chabot-automation` | Hosted chatbots |
| Flowise | `flowiseai-automation` | Visual AI workflow builder |

### Workflow Automation (n8n)
| Task | Skill | When |
|------|-------|------|
| n8n node config | `n8n-node-configuration` | Configure n8n nodes |
| n8n JavaScript | `n8n-code-javascript` | Custom JS in n8n |
| n8n Python | `n8n-code-python` | Custom Python in n8n |
| n8n patterns | `n8n-workflow-patterns` | Common workflow patterns |
| n8n validation | `n8n-validation-expert` | Validate workflows |
| n8n expressions | `n8n-expression-syntax` | Expression syntax |
| n8n MCP | `n8n-mcp-tools-expert` | MCP tool integration |

### Web Scraping & Data Extraction
| Task | Skill | When |
|------|-------|------|
| Firecrawl | `firecrawl-automation` | Web crawling |
| Apify | `apify-automation` | Web scraping platform |
| BrightData | `brightdata-automation` | Proxy + scraping |
| ScrapingBee | `scrapingbee-automation` | Browser scraping |
| Browserless | `browserless-automation` | Headless browser |
| AgentQL | `agentql-automation` | AI-powered scraping |
| Parsehub | `parsehub-automation` | Visual scraper |
| Browser rendering | `cloudflare-browser-rendering-automation` | Render JS pages |

### MCP & Tools
| Task | Skill | When |
|------|-------|------|
| Build MCP servers | `mcp-builder` | Create MCP tools |
| Connect apps | `connect-apps` or `connect` | App integrations |
| Composio | `composio-automation` | Tool orchestration |
| Nango | `nango-automation` | OAuth + API integrations |

### AI Memory & Evaluation
| Task | Skill | When |
|------|-------|------|
| AI memory | `mem0-automation` | Persistent AI memory |
| LLM evaluation | `humanloop-automation`, `honeyhive-automation` | Test AI outputs |
| Langbase | `langbase-automation` | AI app platform |
| LangSmith | `langsmith-fetch` | LLM observability |

## Workflow Templates

### Voice AI Agent
1. `retellai-automation` or `bolna-automation` for agent platform
2. `claude-api` or `openai-automation` for LLM backend
3. `deepgram-automation` for speech-to-text
4. `elevenlabs-automation` for text-to-speech
5. `n8n-workflow-patterns` for orchestration

### RAG Chatbot
1. `firecrawl-automation` to crawl knowledge base
2. `claude-api` for embeddings + generation
3. `botpress-automation` for chat interface
4. `n8n-workflow-patterns` for pipeline orchestration

### Data Pipeline
1. Source: `firecrawl-automation` or `apify-automation`
2. Process: `n8n-code-javascript` or `n8n-code-python`
3. Store: `neon-automation` or `turso-automation` (databases)
4. Serve: `claude-api` or `openai-automation`
