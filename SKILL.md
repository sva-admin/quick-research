---
name: quick-research
description: Fast single-pass research with a structured TL;DR brief (summary, key features, pros/cons, pricing, bottom line). Trigger on "quick research", "TL;DR on", "what is [new tool/release/product]", or any request to quickly understand ONE topic, product, or announcement in ~5 minutes. If they are installed, defer to a deep-research skill for multi-source cited briefs, a trend skill for what's buzzing socially, research-scout for what's-changed updates, and an explainer-graphic skill for visual breakdowns.
---

# Quick Research

Fast, structured research briefs on any topic.

## Process
1. Take the topic/product/release from the user
2. Search the web for the most recent and authoritative sources
3. Generate a structured brief

## Output Format

```markdown
# Quick Research: [Topic]
Date: [date]

## TL;DR (3 sentences max)
[What it is, why it matters, who should care]

## How It Works
[4-6 bullet points explaining the core mechanics]

## Key Features
[Top 5-7 features or capabilities]

## Requirements & Availability
- Platform: [where it runs]
- Pricing: [cost breakdown]
- Access: [how to get it]

## Pros
- [genuine strengths]

## Cons
- [honest limitations]

## Bottom Line
[1-2 sentences: should you use/buy/adopt this?]

## Sources
- [URL 1]: [what this source covered]
- [URL 2]: [what this source covered]
```

## Rules
- Prioritize official sources (company blogs, docs, papers) over aggregator articles
- Include pricing if it's a product/service
- Be honest about limitations, don't oversell
- Date-stamp everything so freshness is clear
- If conflicting information exists, note both positions
- Keep the entire brief under 500 words

## Output
Return the brief inline in chat, leading with the Bottom Line.

If the user keeps a notes directory (an Obsidian vault, a `notes/` or `research/` folder in the project, or whatever their setup defines), also save the brief to `<notes>/<topic-slug>.md` with frontmatter `title`, `source: quick-research`, `created`, `tags`, and report the clickable path. Never invent a location: if there is no obvious notes directory, inline only.
