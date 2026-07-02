# PROJECT-detail.md — Short-form Video Script Builder (YouTube/TikTok/Reels)

## Executive Summary
`shortform-video-script-builder` is a Claude Skill in the **Marketing, Content & Branding** cluster (idea #69). It acts as a short-form video strategist and retention scientist who has written and analyzed thousands of viral YouTube Shorts, TikToks and Instagram Reels. It runs a research-first, evidence-graded harness that profiles the input, selects named world-renowned frameworks, scores the subject across 6 dimensions, challenges its own conclusions, and emits a professional deliverable with a prioritized improvement roadmap.

## Problem Statement
Creators waste effort on videos that lose viewers in the first 3 seconds. This skill engineers scripts for hook strength, retention curve, payoff and shareability, then scores them against proven creative frameworks.

Domain context: practitioners in marketing, content & branding need decisions grounded in citable, current methodology rather than ad-hoc opinion. This skill enforces the evidence hierarchy (Systematic Review > Meta-Analysis > RCT > Cohort > Expert Opinion > Blog) and keeps its knowledge current through a weekly crawl.

## Target Users & Use Cases
- **Trigger example A:** User says *"Evaluate / score / optimize my short-form video script builder"* → skill runs the full harness and returns a scored report + roadmap.
- **Trigger example B:** User provides an artifact (document, dataset, design, plan) → skill audits it against the frameworks below.
- **Trigger example C:** User asks *"What should I improve first?"* → skill returns the impact/effort-ranked roadmap section only.

## Harness Architecture
```
USER INPUT
   |
   v
[Stage 1] sub-audience-analysis  --> scoped profile / context
   |
   v
[Stage 2] sub-hook-engineer  --> selected frameworks (Hook-Retention-Payoff (HRP) model, ...)
   |
   v
[Stage 3] RESEARCH (WebSearch/WebFetch) --> evidence pack  (fallback: SECOND-KNOWLEDGE-BRAIN.md)
   |
   v
[Stage 4] sub-retention-scorer  --> 6-dimension score
   |
   v
[Stage 5] sub-quality-reviewer  --> challenge / validation
   |
   v
[Stage 6] MAIN HARNESS --> final deliverable (score table + prioritized roadmap)
```

## Full Sub-Skill Catalog

### sub-audience-analysis
- **Purpose:** Profile the target viewer (platform, niche, intent, scroll behavior) so hook and pacing match audience psychology.
- **Inputs:** scoped context from prior stage + user artifact
- **Outputs:** structured findings passed to the next stage
- **Tools used:** Read, WebSearch, WebFetch, Write
- **Quality gate:** output must be evidence-linked and complete before the harness advances

### sub-hook-engineer
- **Purpose:** Generate and score 5+ opening hooks against the 3-Second Hook Rule, curiosity gap and pattern-interrupt theory.
- **Inputs:** scoped context from prior stage + user artifact
- **Outputs:** structured findings passed to the next stage
- **Tools used:** Read, WebSearch, WebFetch, Write
- **Quality gate:** output must be evidence-linked and complete before the harness advances

### sub-retention-scorer
- **Purpose:** Map the script to a second-by-second retention curve and score against the HRP model and platform watch-time norms.
- **Inputs:** scoped context from prior stage + user artifact
- **Outputs:** structured findings passed to the next stage
- **Tools used:** Read, WebSearch, WebFetch, Write
- **Quality gate:** output must be evidence-linked and complete before the harness advances

### sub-quality-reviewer
- **Purpose:** Devil's-advocate pass: check originality, claim safety, platform policy fit and CTA strength before final output.
- **Inputs:** scoped context from prior stage + user artifact
- **Outputs:** structured findings passed to the next stage
- **Tools used:** Read, WebSearch, WebFetch, Write
- **Quality gate:** output must be evidence-linked and complete before the harness advances

## Skill File Format Specification
Frontmatter schema (all skill files):
```yaml
---
name: shortform-video-script-builder            # or sub-<name>
description: <one-line summary shown in /help>
---
```
Required sections in `main.md`: Role & Persona, Workflow (Harness Flow), Sub-skills Available, Tools, Output Format, Quality Gates.

## E2E Execution Flow
1. Parse user request and artifact; if ambiguous, ask targeted intake questions.
2. Run `sub-audience-analysis` to build the scoped profile.
3. Run `sub-hook-engineer` to lock frameworks: Hook-Retention-Payoff (HRP) model, AIDA (Attention-Interest-Desire-Action), StoryBrand SB7, Open Loops / Curiosity Gap theory....
4. Research: issue WebSearch queries (short form video retention hook; viral video psychology attention; social video watch time optimization); WebFetch top authoritative hits; grade evidence. On failure, fall back to SECOND-KNOWLEDGE-BRAIN.md and label the degradation.
5. Run `sub-retention-scorer` to score the 6 dimensions.
6. Run `sub-quality-reviewer` challenge pass.


8. Synthesize the final deliverable.

## Scoring Dimensions
1. Hook strength (first 3s)
2. Retention architecture
3. Payoff & value delivery
4. Shareability / saveability
5. Platform-fit & format
6. Call-to-action clarity

Each dimension is scored 0–5 with an evidence citation and a one-line justification; the overall score is the weighted mean (weights set by `sub-hook-engineer`).

## SECOND-KNOWLEDGE-BRAIN Integration
- **Sources:** ArXiv (cs.HC, cs.MM, cs.SI); YouTube Creator Insider / Creator Academy, TikTok Newsroom & Creative Center trends, Meta for Creators (Reels best practices), arXiv cs.HC & cs.MM (attention, multimedia), Think with Google video research.
- **Crawl config:** weekly cron via `tools/knowledge_updater.py` (crawl4ai).
- **Append format:** scored entries (title, authors, year, DOI/URL, key finding, relevance) added to the Knowledge Update Log with a date stamp and dedup by URL/DOI hash.

## Supporting Tools Spec
`tools/knowledge_updater.py`:
- **Inputs:** search queries (above), ArXiv categories, last-run timestamp.
- **Outputs:** appended entries in `SECOND-KNOWLEDGE-BRAIN.md`.
- **Schedule:** weekly.

## Quality Gates (must all be TRUE before final output)
- Every dimension scored with a cited source or explicit fallback label.
- At least one framework from the catalog explicitly applied.
- Challenge phase documented (≥3 counter-arguments considered).


- Roadmap items carry impact + effort ratings.

## Test Scenarios (summary; full set in tests/)
1. Happy-path full audit of a typical marketing, content & branding artifact.
2. Ambiguous/incomplete input → intake clarification path.
3. Offline/degraded mode → graceful fallback to knowledge brain.
4. Edge artifact stress test (adversarial input).
5. Roadmap-only request → returns prioritized recommendations.

## Key Design Decisions
1. Framework-grounded scoring only — no ad-hoc criteria.
2. Research-first with explicit graceful degradation.
3. Mandatory challenge phase before synthesis.
4. Impact/effort roadmap is always the final artifact.
5. Self-improving knowledge base via weekly crawl.
