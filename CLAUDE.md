# CLAUDE.md — Short-form Video Script Builder (YouTube/TikTok/Reels)

**Skill name:** `shortform-video-script-builder`
**Tagline:** Short-form Video Script Builder (YouTube/TikTok/Reels)
**Source idea:** #69  |  **Cluster:** `marketing-content-branding` (Marketing, Content & Branding)
**Current phase:** Phase 2 complete (core sub-skills + harness + quality gates). Phase 3 knowledge pipeline scaffolded.

## Problem This Skill Solves
Creators waste effort on videos that lose viewers in the first 3 seconds. This skill engineers scripts for hook strength, retention curve, payoff and shareability, then scores them against proven creative frameworks.

## Harness Flow Summary
1. **Intake / scoping** → `sub-audience-analysis.md` gathers context and constraints.
2. **Framework selection** → `sub-hook-engineer.md` chooses the named evaluation frameworks for this case.
3. **Research / evidence** → WebSearch + WebFetch pull authoritative sources; fall back to SECOND-KNOWLEDGE-BRAIN.md if offline.
4. **Scoring / analysis** → `sub-retention-scorer.md` scores across the 6 dimensions.
5. **Challenge phase** → devil's-advocate review (`sub-quality-reviewer.md`).
6. **Synthesis** → main harness assembles the final professional deliverable (score + prioritized roadmap).

Standard quality gates apply (see Quality Gates below).

## Sub-skills
- `skills/sub-audience-analysis.md` — Profile the target viewer (platform, niche, intent, scroll behavior) so hook and pacing match audience psychology.
- `skills/sub-hook-engineer.md` — Generate and score 5+ opening hooks against the 3-Second Hook Rule, curiosity gap and pattern-interrupt theory.
- `skills/sub-retention-scorer.md` — Map the script to a second-by-second retention curve and score against the HRP model and platform watch-time norms.
- `skills/sub-quality-reviewer.md` — Devil's-advocate pass: check originality, claim safety, platform policy fit and CTA strength before final output.

## Tools Required
- WebSearch, WebFetch (research-first evidence gathering)
- Read, Write (deliverable assembly)
- Bash / Python (run `tools/knowledge_updater.py`)

## Knowledge Sources
- ArXiv categories: cs.HC, cs.MM, cs.SI
- Domain sources: YouTube Creator Insider / Creator Academy, TikTok Newsroom & Creative Center trends, Meta for Creators (Reels best practices), arXiv cs.HC & cs.MM (attention, multimedia), Think with Google video research

## Supporting Python Tools
- `tools/knowledge_updater.py` — crawl4ai pipeline that refreshes `SECOND-KNOWLEDGE-BRAIN.md` weekly.

## Active Development Tasks
- [x] Scaffold folder + 8 required deliverables
- [x] Define 7 named evaluation frameworks
- [x] Implement 4 sub-skills (min 3)
- [ ] Wire shared cluster sub-skills across `marketing-content-branding`
- [ ] First live crawl to seed SECOND-KNOWLEDGE-BRAIN knowledge log

## Reference Docs
- `PROJECT-detail.md` — full technical spec
- `PROJECT-DEVELOPMENT-PHASE-TRACKING.md` — phase roadmap
- `SECOND-KNOWLEDGE-BRAIN.md` — self-improving knowledge base
