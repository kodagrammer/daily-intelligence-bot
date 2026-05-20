# Project Overview

This project is not a generic AI news summarizer.

The goal is to continuously track high-signal AI engineering trends,
analyze them from a backend/software engineering perspective,
and accumulate structured long-term reasoning.

The system prioritizes:
- signal over information volume
- engineering applicability over hype
- long-term architectural impact over short-term trends
- structured interpretation over shallow summarization


# Current Iteration Scope

Current scope:
- AI trend daily reporting bot only

Out of scope:
- market/stock analysis
- portfolio management
- RAG
- vector database
- dashboard infrastructure
- multi-agent orchestration
- autonomous agent execution
- long-term memory architecture


# Primary Goals

The bot should help answer:

- Why are engineers interested in this?
- What problem does it solve?
- What trade-offs exist?
- What are the operational/security implications?
- How might this evolve?
- How can backend engineers realistically apply this?


# Trend Selection Criteria

Trend priority order:

1. Active discussion among engineers
2. Real production usage
3. Backend engineering relevance
4. Security and operational implications
5. Long-term architectural impact
6. High mention frequency within the last 30 days

Preferred sources:
- GitHub
- Hacker News
- Reddit engineering communities
- engineering blogs
- official technical documentation
- production engineering discussions


# Report Philosophy

The report should NOT:
- become a shallow AI news digest
- overwhelm readers with excessive information
- focus on hype without engineering value
- contain excessive deep dives
- optimize for token-heavy verbosity

The report SHOULD:
- remain concise and high-signal
- contain actionable engineering interpretation
- explain trade-offs clearly
- help build long-term technical judgment


# Engineering Constraints

Prefer:
- simple Python scripts
- GitHub Actions
- markdown-first architecture
- minimal dependencies
- explicit over abstracted design

Avoid:
- premature abstractions
- unnecessary infrastructure
- complex orchestration
- framework-heavy architecture
- introducing databases too early


# Repository Structure Philosophy

The repository is designed to evolve gradually.

Shared infrastructure should remain reusable:
- GitHub integration
- Telegram notification
- report generation
- scheduler workflows

Domain-specific logic should remain isolated:
- AI trend analysis
- market analysis
- future research agents


# Future Direction

Potential future expansion:
- GPT post-processing layer
- thesis tracking
- long-term reasoning accumulation
- market trend reporting
- engineering signal scoring

However:
future expansion must not compromise simplicity in the current iteration.


# Decision-Making Principle

When uncertain:
- prefer simplicity
- prefer readability
- prefer maintainability
- prefer explicit structures
- prefer iteration over over-engineering

# 추가 권장 항목

## Trend Selection Constraints

Avoid repeatedly selecting the same topic within a short time window.

Constraints:
- Do not select topics heavily covered within the last 7 days
- Prefer emerging or meaningfully evolving discussions
- Repeated topics are only allowed if:
  - major architectural changes occurred
  - significant production adoption happened
  - important security/operational incidents emerged
  - the engineering consensus meaningfully shifted

The goal is to avoid repetitive reporting
and maximize long-term signal diversity.
