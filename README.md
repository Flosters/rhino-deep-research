# rhino-deep-research

A Claude Code skill that implements the **RhinoInsight** methodology for deep research — producing thorough, citation-backed, and verifiable research reports from complex questions.

---

## What it does

Most AI research sessions suffer from two compounding problems:

- **Error accumulation** — vague planning leads to drift, and mistakes compound across steps
- **Context rot** — noise and irrelevant information pile up, degrading output quality

`rhino-deep-research` solves both with two control mechanisms borrowed directly from the RhinoInsight paper:

| Mechanism | What it controls |
|---|---|
| **Verifiable Checklist** | *What* Claude researches — converts your question into specific, acceptance-ready sub-goals |
| **Evidence Audit** | *What information* gets carried forward — structured, tagged, pruned after every search round |

The result is a structured 5-step research process that produces professional reports with inline citations, confidence tiers, and explicit knowledge boundaries.

---

## The 5-Step Process

1. **Verifiable Checklist + Hierarchical Outline** — decompose the question into concrete, verifiable sub-goals before touching any sources
2. **Iterative, Node-Specific Searches** — targeted searches per outline node, not one sprawling query
3. **Evidence Audit** — normalize findings into structured evidence units, prune noise, update the outline
4. **Evidence-Bound Drafting** — write node by node using only audited, tagged evidence with explicit citations
5. **Structured Final Report** — executive summary, methodology, analysis, confidence assessment, and full source list

---

## Report output format

Every run produces a report with:

- Executive Summary
- Research Scope and Methodology
- Detailed Analysis (one section per outline node)
- Insights and Recommendations
- Confidence Assessment (high / moderate / low tiers)
- Knowledge Boundaries
- Full Sources list

---

## Based on

This skill implements the framework described in:

> **RhinoInsight: Improving Deep Research through Control Mechanisms for Model Behavior and Context**
> Yu Lei, Shuzheng Si, Wei Wang, Yifei Wu, Gang Chen, Fanchao Qi, Maosong Sun
> arXiv:2511.18743 (November 2025)
> https://arxiv.org/abs/2511.18743

---

## Installation

### Prerequisites

- [Claude Code](https://claude.ai/code) CLI installed

### Install the skill

```
npx skills add Flosters/rhino-deep-research
```

---

## Usage

Once installed, the skill activates automatically when you ask Claude to conduct deep research. Trigger phrases include:

- `"Research X thoroughly"`
- `"Give me a deep dive on Y"`
- `"I need a comprehensive report on Z"`
- `"Help me research this properly"`
- `"Write a research report on..."`

Claude will then walk through the 5-step RhinoInsight process and produce a structured, citation-backed report.

---

## License

MIT — see [LICENSE](LICENSE)
