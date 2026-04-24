---
name: fan-out-research
description: >
  Fan-out/fan-in research pattern. Spawns N parallel sonnet sub-agents to research
  a question from different angles, then synthesizes results with opus. Use when
  user says "deep research", "fan out", "parallel research", "research thoroughly",
  "find the best", "compare options", "comprehensive analysis", or any research
  task that benefits from multiple independent perspectives.
---

# Fan-Out / Fan-In Research

## Purpose
Maximize research quality and coverage by spawning multiple independent research
agents (sonnet, cheap and fast) that each explore a different angle, then synthesize
all findings with the main thread (opus, smart and expensive).

## When to Use
- Comparing APIs, tools, platforms, or frameworks
- Competitive research and market analysis
- Finding the best approach to solve a problem
- Any research where a single pass would miss important angles
- Deal research on companies or people
- Content research for blog posts or LinkedIn content

## Execution Steps

### 1. Decompose the Query
Break the user's research question into 5-8 distinct research angles. Each angle
should be independent and explore a different facet of the problem.

Example for "find the best CRM for AI agencies":
- Agent 1: Feature comparison of top 10 CRMs
- Agent 2: Pricing and scalability analysis
- Agent 3: Integration ecosystem (especially AI tools)
- Agent 4: User reviews and satisfaction scores
- Agent 5: Implementation complexity and onboarding time
- Agent 6: API quality and automation capabilities

### 2. Fan Out -- Spawn Sub-Agents
Spawn all research agents in parallel using the Agent tool with `model: "sonnet"`.
Each agent gets:
- A focused research prompt for its specific angle
- Instructions to be thorough but concise
- A request to output structured findings (not prose)

Use this exact pattern:
```
Agent(
  description: "Research [angle]",
  prompt: "Research the following question thoroughly: [specific angle].
  Output your findings as a structured list with:
  - Key findings (bullet points)
  - Data points with sources
  - Recommendations
  - Confidence level (high/medium/low) for each finding
  Be thorough. Use web search and web fetch as needed.",
  model: "sonnet",
  subagent_type: "general-purpose"
)
```

### 3. Fan In -- Synthesize with Opus
Once all agents return, synthesize using the main thread (opus):
- Identify consensus findings (mentioned by 3+ agents)
- Flag high-confidence recommendations
- Surface outlier insights (mentioned by only 1 agent but high-value)
- Resolve contradictions between agents
- Produce a ranked recommendation with confidence scores

### 4. Output Format
```markdown
## Research Synthesis: [Topic]

### Consensus Findings (agreed by 3+ agents)
- [finding] -- confidence: HIGH

### Strong Recommendations
1. [recommendation] -- why: [reason]

### Outlier Insights (unique but valuable)
- [insight from single agent] -- worth investigating because: [reason]

### Contradictions Resolved
- Agent A said X, Agent B said Y. Resolution: [explanation]

### Next Steps
- [actionable items]
```

## Token Economics
- Each sonnet sub-agent: ~$0.10-0.30
- 6 agents total: ~$0.60-1.80
- Opus synthesis: ~$0.50-1.00
- Total: ~$1.10-2.80 for research that would take 30+ minutes manually
- Time saved: 5-8x faster than sequential research
