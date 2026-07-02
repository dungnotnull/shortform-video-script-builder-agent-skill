# Phase 5: Cross-Skill Wiring & Integration

## Cluster Integration Overview

**Skill:** shortform-video-script-builder (idea #69)
**Cluster:** marketing-content-branding
**Status:** ✅ Complete
**Last Updated:** 2026-07-02

This document defines cross-skill integration patterns, shared sub-skill references, and standardization protocols for the marketing-content-branding cluster. It ensures no duplicated sub-skill logic across sibling skills and provides consistent integration patterns for future cluster development.

---

## Cluster Architecture

### Current Cluster Skills (marketing-content-branding)

1. **shortform-video-script-builder** (#69) — Primary skill
   - Focus: Short-form video retention and optimization
   - Platform: YouTube Shorts, TikTok, Instagram Reels
   - Output: Script evaluation, scoring, improvement roadmap

2. **Future Skills (Planned for Cluster Integration)**
   - Content Strategy Planner — Long-form content planning and optimization
   - Social Media Campaign Architect — Multi-platform campaign strategy
   - Brand Voice Designer — Brand identity and communication consistency
   - Audience Persona Builder — Target audience research and profiling
   - Marketing Analytics Interpreter — Performance analysis and insights

### Shared Sub-Skill Architecture

The cluster uses a **hub-and-spoke** model for shared capabilities:

**Central Hub Skills (Shared Across Cluster):**
- `shared-audience-analysis` — Universal audience profiling
- `shared-research-validator` — Evidence grading and citation
- `shared-quality-reviewer` — Challenge-phase validation
- `shared-roadmap-generator` — Prioritized recommendation synthesis

**Skill-Specific Sub-Skills:**
- `sub-hook-engineer` — Unique to video content
- `sub-retention-scorer` — Unique to time-based content

---

## Shared Sub-Skill Specifications

### shared-audience-analysis

**Purpose:** Universal audience profiling for any marketing content

**Inputs:**
- Content artifact (any marketing material)
- Content type (video, text, image, campaign)
- Platform/channel context
- Stated goals and objectives

**Outputs:**
- 4-dimensional audience profile
- Platform/channel psychology mapping
- Content intent classification
- Attention allocation assessment

**Shared Framework:**
```markdown
## Universal Audience Profile Template

### Platform/Channel Psychology
- Channel Type: [social/web/email/print/etc.]
- Attention Environment: [fast/slow/medium]
- Decision Window: [specific time range]
- Engagement Expectations: [high/medium/low]

### 4-Dimensional Profile
**A. Platform/Channel Expertise:** [native/regular/casual/new]
**B. Content Intent State:** [entertainment/problem-solving/discovery/social]
**C. Domain/Niche Sophistication:** [expert/intermediate/beginner/curious]
**D. Attention Allocation:** [high-intent/medium-intent/low-intent/passive]

### Integration Notes
- [Skill-specific guidance for next stages]
```

**Usage Across Cluster:**
- Video skills: Focus on visual attention and scroll behavior
- Content skills: Emphasize reading patterns and engagement triggers
- Campaign skills: Consider multi-channel journey and attribution
- Brand skills: Include brand perception and identity factors

---

### shared-research-validator

**Purpose:** Standardized evidence grading and citation across all cluster skills

**Evidence Hierarchy (Universal):**
```
Tier 1: Systematic Review — Meta-analyses, comprehensive reviews
Tier 2: High-Quality Studies — RCTs, large cohort studies
Tier 3: Individual Studies — Single research papers, case studies
Tier 4: Expert Consensus — Industry standards, professional guidelines
Tier 5: Expert Opinion — Thought leaders, practitioner insights
Tier 6: General Knowledge — Blog posts, popular articles (lowest tier)
```

**Citation Standard:**
```markdown
[Source Title](URL) — **Tier [1-6]** — [Specific finding applied]
```

**Validation Protocol:**
1. For any claim requiring evidence, search for sources
2. Grade source by evidence hierarchy
3. Cite with tier designation and specific finding
4. If no source available, flag as "Unsubstantiated Claim"

**Usage Across Cluster:**
- All skills use same evidence grading
- Consistent citation format across outputs
- Shared quality standards for research claims
- Cross-skill learning from validated sources

---

### shared-quality-reviewer

**Purpose:** Universal challenge-phase validation for all cluster outputs

**Challenge Categories (Universal):**
1. **Originality Verification** — Plagiarism and derivative content detection
2. **Claim Safety Audit** — Factual claim validation and risk assessment
3. **Platform/Channel Compliance** — Policy and guideline adherence
4. **CTA/Action Clarity** — Call-to-action effectiveness validation
5. **Scoring Robustness** — Challenge analytical assumptions and conclusions
6. **Audience Assumptions** — Stress-test audience profile conclusions

**Challenge Output Format (Universal):**
```markdown
## Quality Review Report

### Challenge Summary
- Total Challenges Generated: X
- Validated Challenges: X (resulting in revisions)
- Critical Issues Identified: X

### Specific Challenge Sections
[Each category with detailed challenges]

### Revision Recommendations by Priority
**P0 - Critical (Fix Before Deployment):**
**P1 - High (Strongly Recommended):**
**P2 - Medium (Address When Feasible):**
**P3 - Low (Optional Improvement):**
```

**Usage Across Cluster:**
- All skills run challenge phase before final output
- Consistent challenge categories adapted to domain
- Shared priority framework for recommendations
- Universal quality gate enforcement

---

### shared-roadmap-generator

**Purpose:** Standardized prioritization and recommendation synthesis

**Prioritization Framework:**
```
Priority Score = (Impact Score × 0.6) + (Effort Inverse × 0.4)

Impact Scoring: High (3) / Medium (2) / Low (1)
Effort Scoring: High (3) / Medium (2) / Low (1)
Effort Inverse: 4 - Effort Score (so Low effort = highest inverse)
```

**Output Format (Universal):**
```markdown
## Prioritized [Improvement/Recommendation] Roadmap

### Tier 1: High Impact, Low Effort (Immediate Wins)
[Table with #, Recommendation, Impact, Effort, Framework Basis]

### Tier 2: High Impact, Medium Effort (Significant Gains)
[Same table format]

### Tier 3: Medium Impact, Medium Effort (Future Iterations)
[Same table format]

### Tier 4: Lower Priority (Long-term Considerations)
[Same table format]
```

**Usage Across Cluster:**
- All skills produce prioritized roadmaps
- Consistent impact/effort assessment
- Standard tier structure for recommendations
- Cross-skill comparable priority scoring

---

## Integration Patterns

### Pattern 1: Sequential Pipeline

**Use Case:** Skills that process content through defined stages

**Flow:**
```
Input → shared-audience-analysis → [Skill-Specific Stage] →
shared-research-validator → [Skill-Specific Scoring] →
shared-quality-reviewer → shared-roadmap-generator → Output
```

**Examples:**
- shortform-video-script-builder (current implementation)
- future content-strategy-planner
- future campaign-architect

**Integration Points:**
- Audience profile feeds all subsequent stages
- Research validation occurs before scoring
- Quality review challenges scoring conclusions
- Roadmap synthesis prioritizes from all prior analysis

---

### Pattern 2: Parallel Analysis

**Use Case:** Skills that analyze multiple aspects simultaneously

**Flow:**
```
Input → shared-audience-analysis → Parallel Tracks:
  ├─ Track A: [Analysis Type A] → shared-research-validator
  ├─ Track B: [Analysis Type B] → shared-research-validator
  └─ Track C: [Analysis Type C] → shared-research-validator
     → shared-quality-reviewer → shared-roadmap-generator → Output
```

**Examples:**
- future brand-voice-designer (analyzing tone, style, messaging)
- future marketing-analytics-interpreter (analyzing metrics, trends, insights)

**Integration Points:**
- Audience profile informs all parallel tracks
- Each track validates with research independently
- Quality review challenges all track conclusions
- Roadmap prioritizes across all track findings

---

### Pattern 3: Iterative Refinement

**Use Case:** Skills that improve content through multiple passes

**Flow:**
```
Input → shared-audience-analysis → Analysis Cycle:
  ├─ [Analysis] → shared-research-validator → shared-quality-reviewer
  ├─ Revision based on review
  └─ Repeat until convergence
     → shared-roadmap-generator → Output
```

**Examples:**
- future content-optimizer (iterative improvement cycles)
- future campaign-refiner (progressive campaign enhancement)

**Integration Points:**
- Each iteration uses consistent validation
- Quality review drives refinement priorities
- Convergence criteria prevent infinite loops
- Final roadmap documents improvement journey

---

## Standardization Protocols

### Output Format Standards

**All Cluster Skills Must Include:**

1. **Executive Summary**
   - Overall score/rating
   - Top 3 strengths
   - Top 3 priority fixes

2. **Detailed Analysis Section**
   - Score/analysis table or equivalent
   - Evidence citations with tiers
   - Framework applications

3. **Challenge/Review Section**
   - Counter-arguments considered
   - Revisions made based on challenges
   - Remaining limitations or caveats

4. **Prioritized Roadmap**
   - Tier-based recommendations
   - Impact/effort ratings
   - Framework basis for each item

5. **Sources & Evidence**
   - Numbered citations
   - Evidence tier designation
   - Specific findings referenced

### Quality Gate Standards

**All Cluster Skills Must Enforce:**

- [ ] Analysis is complete before challenge phase
- [ ] All claims have evidence citations or explicit disclaimers
- [ ] At least one framework is explicitly applied
- [ ] Challenge phase generates ≥3 counter-arguments
- [ ] Roadmap items include impact/effort ratings
- [ ] Output follows standard format structure
- [ ] Degraded mode is explicitly labeled when applicable

### Naming Conventions

**Sub-Skills:**
- Shared: `shared-[function]-analysis/review/etc.`
- Skill-Specific: `sub-[function]-engineer/scorer/etc.`

**Files:**
- Skills: `skills/[skill-name].md`
- Tests: `tests/test-[scenario-name].md`
- Docs: `docs/[document-name].md`
- Tools: `tools/[tool-name].py`

**Functions/Methods:**
- Snake_case: `calculate_retention_score()`
- Descriptive: `generate_hook_options()`

---

## Cross-Skill Learning Protocol

### Shared Knowledge Base

**SECOND-KNOWLEDGE-BRAIN.md Structure:**
```markdown
## Cluster-Wide Frameworks
[Frameworks applicable across all cluster skills]

## Skill-Specific Frameworks: shortform-video-script-builder
[Video-specific frameworks and methodologies]

## Skill-Specific Frameworks: [Future Skill Names]
[Future skill-specific sections]

## Shared Research Sources
[Universal high-quality sources for all skills]

## Domain-Specific Sources
[Sources for specific skill domains]
```

### Knowledge Update Protocol

**Weekly Crawl Sources:**
- ArXiv categories: cs.HC, cs.MM, cs.SI (universal for cluster)
- Domain-specific sources per skill
- Industry research and platform updates

**Shared vs. Skill-Specific:**
- **Shared:** Core frameworks, fundamental research, universal principles
- **Skill-Specific:** Platform nuances, domain techniques, specialized methods

---

## Future Cluster Integration

### Planned Skills and Integration Points

**1. Content Strategy Planner (Future)**
- **Shared Components:** audience-analysis, research-validator, quality-reviewer, roadmap-generator
- **Skill-Specific:** long-form-content-architect, narrative-structure-analyzer
- **Integration:** Shares audience profiling with video skills, different content timing

**2. Social Media Campaign Architect (Future)**
- **Shared Components:** All shared sub-skills
- **Skill-Specific:** multi-platform-coordinator, campaign-flow-designer
- **Integration:** Leverages platform knowledge from video skills for campaign channels

**3. Brand Voice Designer (Future)**
- **Shared Components:** research-validator, quality-reviewer, roadmap-generator
- **Skill-Specific:** tone-consistency-analyzer, brand-alignment-validator
- **Integration:** Uses audience insights from other skills for brand positioning

**4. Audience Persona Builder (Future)**
- **Shared Components:** research-validator, roadmap-generator
- **Skill-Specific:** persona-research-aggregator, empathy-mapping-generator
- **Integration:** Becomes the central audience intelligence hub for cluster

**5. Marketing Analytics Interpreter (Future)**
- **Shared Components:** quality-reviewer, roadmap-generator
- **Skill-Specific:** metrics-pattern-analyzer, trend-detector
- **Integration:** Validates performance assumptions made by other skills

### Cross-Skill Workflow Example

**Scenario:** Creator wants comprehensive content strategy

1. **shortform-video-script-builder** → Optimize individual videos
2. **content-strategy-planner** → Plan long-form content series
3. **social-media-campaign-architect** → Design multi-platform campaign
4. **audience-persona-builder** → Deep audience research (shared across all)
5. **marketing-analytics-interpreter** → Analyze performance, validate assumptions

**Shared Benefits:**
- Consistent audience profiling across all content types
- Unified research validation and evidence standards
- Coordinated quality standards and challenge protocols
- Integrated roadmap prioritization across skill recommendations

---

## Maintenance and Evolution

### Cluster Coordination

**Version Alignment:**
- Shared sub-skills versioned independently
- Cluster skills pin to specific shared sub-skill versions
- Breaking changes require coordinated cluster updates

**Quality Standards:**
- Shared sub-skills undergo rigorous testing before cluster deployment
- All cluster skills must pass integration tests
- Regression testing across cluster when shared components updated

**Documentation Standards:**
- Shared sub-skills have comprehensive documentation
- Integration patterns clearly documented with examples
- Cross-skill workflows documented for common scenarios

### Future Enhancements

**Planned Cluster Capabilities:**

1. **Unified Dashboard**
   - Single interface for all cluster skills
   - Cross-skill insight aggregation
   - Integrated roadmap prioritization

2. **Knowledge Graph**
   - Cross-skill concept linking
   - Framework relationship mapping
   - Shared citation network

3. **Performance Analytics**
   - Cross-skill recommendation tracking
   - Outcome measurement across skills
   - Continuous improvement feedback loop

4. **Collaborative Filtering**
   - Learn from successful skill applications
   - Recommend related skills based on outcomes
   - Cluster-wide best practice identification

---

## Integration Checklist

**Before Marking Phase 5 Complete:**

- [x] Shared sub-skill specifications documented
- [x] Integration patterns defined with examples
- [x] Output format standards established
- [x] Quality gate standards specified
- [x] Naming conventions documented
- [x] Cross-skill learning protocol defined
- [x] Future cluster integration planned
- [x] Maintenance and evolution strategy outlined
- [x] No duplicated sub-skill logic within current implementation
- [x] Clear path for adding future skills to cluster

---

## Status: ✅ PHASE 5 COMPLETE

**Cross-skill wiring is fully documented and ready for cluster expansion.**

All integration patterns, shared components, and standardization protocols are defined. The cluster architecture supports seamless addition of new skills without duplication and maintains consistent quality standards across all marketing-content-branding capabilities.

**Next Phase:** Production deployment and user feedback collection for iterative improvement.
