---
name: stochastic-consensus
description: >
  Stochastic multi-agent consensus and debate pattern. Spawns N agents with the
  same or slightly varied prompts to independently generate solutions, then finds
  statistical consensus and surfaces outliers. Use when user says "consensus",
  "poll agents", "stochastic", "brainstorm thoroughly", "debate this", "model chat",
  "what are ALL the ways to", "come up with every option", or any decision where
  you want to scan the full solution space.
---

# Stochastic Consensus & Debate

## Purpose
Exploit the stochastic nature of LLMs: running the same prompt N times produces
different outputs each time. By collecting all outputs and finding consensus,
you get both the statistically most likely answers AND rare outlier ideas that
a single run would miss.

## When to Use
- Strategic decisions (pricing, positioning, go-to-market)
- Brainstorming where coverage of the solution space matters
- Any problem where "what am I missing?" is the key question
- Evaluating trade-offs between approaches
- Creative ideation (content angles, hook ideas, offer framing)
- Architecture decisions with multiple valid approaches

## Mode 1: Stochastic Consensus

### Execution Steps

#### 1. Frame the Query
Take the user's question and create a core prompt that each agent will receive.
Then create N variations by assigning each agent a different "perspective":

Example perspectives for 8 agents:
1. Conservative/risk-averse analyst
2. Aggressive growth optimizer
3. Technical feasibility expert
4. Customer/user experience advocate
5. Contrarian who challenges conventional wisdom
6. First-principles reasoner
7. Industry veteran with pattern matching
8. Data-driven quantitative analyst

#### 2. Spawn N Agents in Parallel
Spawn all agents simultaneously using `model: "sonnet"`:

```
Agent(
  description: "Consensus agent [N] - [perspective]",
  prompt: "You are a [perspective description].
  Given this question: [user's question]

  Generate exactly 10 independent solutions or recommendations.
  For each, provide:
  - The solution (one sentence)
  - Why it works (one sentence)
  - Confidence: HIGH/MEDIUM/LOW

  Be specific and actionable. No generic advice.",
  model: "sonnet"
)
```

#### 3. Aggregate and Find Consensus
Once all agents return, in the main opus thread:

1. **List all unique solutions** across all agents
2. **Count frequency** -- how many agents suggested each solution
3. **Rank by consensus** -- solutions mentioned by most agents first
4. **Identify outliers** -- solutions mentioned by only 1 agent
5. **Score each solution**: consensus_score = (frequency / N) * avg_confidence

#### 4. Output Format
```markdown
## Stochastic Consensus: [Topic]
**Agents polled:** [N] | **Total raw ideas:** [count] | **Unique ideas:** [count]

### Tier 1: Strong Consensus (mentioned by 5+ agents)
- [solution] -- frequency: [X/N], confidence: HIGH

### Tier 2: Moderate Consensus (mentioned by 3-4 agents)
- [solution] -- frequency: [X/N], confidence: MEDIUM

### Tier 3: Emerging Ideas (mentioned by 2 agents)
- [solution] -- frequency: [X/N]

### Outliers Worth Investigating (mentioned by 1 agent only)
- [solution] -- perspective: [which agent], why interesting: [reason]

### Statistical Summary
- Consensus rate: [% of ideas that appeared 3+ times]
- Solution space coverage: [estimated % of total possibilities explored]
```

## Mode 2: Debate (Multi-Round)

### When to Use Over Consensus
Use debate when solutions interact with each other, when you need agents to
challenge and refine ideas, or when the problem benefits from adversarial testing.

### Execution Steps

#### Round 1: Independent Generation
Same as consensus mode -- spawn N agents, each generates solutions independently.

#### Round 2: Cross-Pollination
Spawn N agents again, but this time each agent receives:
- Its own Round 1 output
- ALL other agents' Round 1 outputs
- Instruction: "Review all solutions. Update your list. Add new ideas inspired by
  others. Remove ideas you now think are weak. Challenge at least 2 ideas from
  other agents."

#### Round 3: Convergence (Optional)
One more round where agents see Round 2 outputs and produce final recommendations.
Typically converges after 2-3 rounds.

#### Final Synthesis
Opus synthesizes all rounds, tracking how ideas evolved:
- Ideas that survived all rounds = highest confidence
- Ideas that were challenged and defended = battle-tested
- Ideas that emerged in later rounds = creative combinations
- Ideas that were eliminated = documented as "explored and rejected"

## Token Economics
- Consensus (8 sonnet agents, 1 round): ~$1.50-3.00
- Debate (8 sonnet agents, 3 rounds): ~$5.00-10.00
- Opus synthesis: ~$1.00-2.00
- Use consensus for quick scans, debate for critical decisions