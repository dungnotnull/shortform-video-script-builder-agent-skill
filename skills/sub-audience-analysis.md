---
name: sub-audience-analysis
description: (shortform-video-script-builder) Profile the target viewer (platform, niche, intent, scroll behavior) so hook and pacing match audience psychology.
---

# Sub-skill: audience-analysis

## Purpose
Profile the target viewer (platform, niche, intent, scroll behavior) so hook and pacing match audience psychology. This stage builds the foundation for all subsequent scoring by establishing who will watch this content, how they behave on their chosen platform, and what psychological triggers will capture their attention.

## When the Harness Calls This
Stage 1 of the `shortform-video-script-builder` main workflow. This is the first analytical stage after intake and must complete before framework selection occurs.

## Inputs
- **Primary:** User's video script or content concept (text artifact)
- **Context from intake:** Target platform (YouTube Shorts/TikTok/Reels), content niche, stated goals (awareness/conversion/engagement), target demographic
- **Framework reference:** Hook-Retention-Payoff (HRP) model for audience-matching hooks

## Procedure

### 1. Artifact Ingestion and Context Extraction
Read and parse the user's content to extract:
- **Content type:** Educational, entertainment, promotional, storytelling, tutorial
- **Format indicators:** Script length, visual cues description, audio elements mentioned
- **Stated audience:** Any explicit mentions of target viewer characteristics
- **Platform signals:** Platform-specific language, formatting, or references

**Extraction Template:**
```
Content Length: X characters/words
Format Type: [spoken/visual/mixed]
Primary Topic: [identified from content]
Platform Affinity: [detected from style/references]
Explicit Audience Claims: [yes/no + details]
```

### 2. Platform Psychology Analysis
Map the content to platform-specific viewer psychology using this framework:

| Platform | Avg View Duration | Scroll Behavior | Hook Expectation | Pacing Tolerance |
|----------|-------------------|-----------------|-------------------|------------------|
| TikTok | 7-10 seconds | Ultra-fast (<1s decision) | Visual+Audio pattern interrupt | 0.5-2s per beat |
| YouTube Shorts | 10-15 seconds | Fast but discoverable | Value proposition or curiosity | 1-3s per beat |
| Instagram Reels | 8-12 seconds | Fast, visually-driven | Aesthetic + conceptual hook | 0.75-2.5s per beat |

**Analysis Requirements:**
- Identify the primary platform from user input or content signals
- Apply the corresponding psychology baseline
- Note any platform mismatches (e.g., TikTok pacing on YouTube)
- Calculate the "attention window" available for hook delivery

### 3. Audience Dimension Profiling
Build a 4-dimensional profile of the target viewer:

#### Dimension A: Platform Expertise Level
- **Native:** Highly familiar with platform conventions, expects format-native creativity
- **Regular:** Active user, understands platform culture and trends
- **Casual:** Infrequent user, less sensitive to platform-specific cues
- **New:** Unfamiliar with platform norms, requires more explicit value signals

#### Dimension B: Content Intent State
- **Entertainment-seeking:** Wants fun, escape, emotional engagement
- **Problem-solving:** Looking for specific information or solutions
- **Discovery:** Open to novel content, browsing algorithmically
- **Social:** Looking for shareable, identity-signaling content

#### Dimension C: Niche Sophistication
- **Expert:** Deep knowledge in the content domain, will spot inaccuracies
- **Intermediate:** Familiar with basics, can follow moderate complexity
- **Beginner:** New to the topic, needs clear explanations and simple hooks
- **Curious:** Non-practitioner with casual interest in the niche

#### Dimension D: Attention Allocation
- **High-intent:** Actively sought this content, willing to invest attention
- **Medium-intent:** Browsing with purpose, open to relevant content
- **Low-intent:** Passive scrolling, high bar for engagement
- **Entertainment-only:** No utility intent, pure entertainment value required

### 4. Research-Based Audience Validation
Use WebSearch with these targeted queries to validate and refine the profile:

**Query Set 1: Platform-Specific Viewer Psychology**
- `[platform] viewer psychology attention span 2024 2025`
- `[platform] algorithm viewer behavior retention`
- `[platform] content strategy audience psychology`

**Query Set 2: Niche-Specific Audience Expectations**  
- `[niche] short-form video audience expectations`
- `[niche] social media content viewer psychology`
- `[niche] educational video engagement patterns`

**Query Set 3: Demographic Correlation**
- `[demographic] short-form video viewing habits`
- `[age group] `[platform] content preferences`

**Evidence Grading:**
- **Tier 1 (Systematic Review):** Meta-analyses of viewer behavior studies
- **Tier 2 (Expert Consensus):** Platform official guidelines, industry research
- **Tier 3 (Single Studies):** Individual academic papers on attention/retention
- **Tier 4 (Expert Opinion):** Creator case studies, platform consultant insights
- **Tier 5 (Blog/Popular):** General advice articles, anecdotal evidence

### 5. Hook-Pacing Recommendation Matrix
Generate a structured recommendation for hook and pacing based on the audience profile:

| Profile Element | Hook Strategy | Pacing Recommendation | Evidence Source |
|-----------------|---------------|----------------------|-----------------|
| Platform: [detected] | [specific hook approach] | [beat frequency and duration] | [citation or fallback] |
| Expertise: [level] | [complexity appropriateness] | [information density] | [citation or fallback] |
| Intent: [state] | [value delivery timing] | [payoff pacing] | [citation or fallback] |
| Attention: [level] | [immediacy requirements] | [hook-to-value ratio] | [citation or fallback] |

### 6. Quality Validation
Before output completion, verify:

**Completeness Check:**
- [ ] All 4 audience dimensions are explicitly profiled
- [ ] Platform psychology is mapped with specific attention windows
- [ ] At least 2 WebSearch queries were attempted (or fallback labeled)
- [ ] Hook-pacing matrix includes evidence citations or fallback labels

**Evidence Integrity Check:**
- [ ] All claims about audience behavior are cited with evidence tiers
- [ ] No assertions about platform performance without source
- [ ] Niche-specific claims are validated by research
- [ ] Demographic assumptions are flagged as such

**Coherence Check:**
- [ ] Profile elements are internally consistent
- [ ] Recommendations align with established platform norms
- [ ] Hook strategies are appropriate for attention allocation level

### 7. Structured Output Generation
Produce markdown output in this exact format:

```markdown
## Audience Analysis Profile

### Platform Psychology Mapping
**Primary Platform:** [detected platform]
**Avg Attention Window:** [X seconds]
**Scroll Speed:** [fast/medium/slow with evidence]
**Hook Expectation:** [visual/audio/conceptual with evidence]

### 4-Dimensional Audience Profile

**A. Platform Expertise:** [native/regular/casual/new]
- Implications: [what this means for hook sophistication and pacing]

**B. Content Intent:** [entertainment/problem-solving/discovery/social]
- Value Delivery: [how and when value must be communicated]
- Payoff Structure: [immediate/gradual/late-payoff requirements]

**C. Niche Sophistication:** [expert/intermediate/beginner/curious]
- Complexity Threshold: [maximum complexity level that retains engagement]
- Credibility Requirements: [what level of proof/authority is needed]

**D. Attention Allocation:** [high-intent/medium-intent/low-intent/entertainment-only]
- Hook Immediacy: [how quickly the hook must deliver]
- Value Density: [how much value per second is required]

### Hook-Pacing Recommendation Matrix
[Table as specified in Section 5]

### Research Sources
1. [Source title and link] — [Evidence Tier] — [Key finding relevant to this profile]
2. [... additional sources ...]

### Integration Notes for Hook Engineering
- [Specific guidance for sub-hook-engineer stage]
- [Platform-specific hook requirements]
- [Audience sophistication considerations for hook complexity]
- [Pacing constraints to pass forward]

### Fallback Mode Label
[If WebSearch/WebFetch were unavailable, explicitly state:]
⚠️ **DEGRADED MODE:** Audience analysis based on cached knowledge from SECOND-KNOWLEDGE-BRAIN.md. Some platform psychology trends may be outdated.
```

## Outputs
- **Primary:** Structured audience profile in markdown format above
- **Secondary:** Hook-pacing recommendations for the next stage
- **Tertiary:** Research citations with evidence tiers

## Quality Gate
**ALL conditions must be TRUE before passing to next stage:**

- [ ] Platform is identified and psychology is mapped with specific attention windows
- [ ] All 4 audience dimensions are explicitly profiled with implications
- [ ] Hook-pacing matrix is complete with evidence citations or labeled fallback
- [ ] Research section includes minimum 2 sources or explicit fallback label
- [ ] Integration notes provide specific guidance for hook engineering stage
- [ ] No unsupported assertions about audience behavior without evidence or disclaimer

## Failure Modes and Recovery

**Insufficient Context Recovery:**
If the artifact lacks clear platform or audience signals:
1. Use platform-specific language and format cues to make educated inference
2. Flag uncertainty with "⚠️ INFERRED:" labels
3. Provide multiple platform scenarios if ambiguous
4. Recommend clarification questions for intake stage

**Research Tool Failure Recovery:**
If WebSearch/WebFetch are unavailable:
1. Rely on SECOND-KNOWLEDGE-BRAIN.md frameworks
2. Explicitly label the degraded mode
3. Use cached platform psychology baselines
4. Flag any potentially outdated assumptions

**Niche-Specific Gaps Recovery:**
If research cannot validate niche-specific audience expectations:
1. Cross-reference similar niches for patterns
2. Apply platform-general psychology principles
3. Flag the gap with "⚠️ GENERALIZED:" label
4. Recommend additional research if high-stakes decision

## Framework Application Notes

**Hook-Retention-Payoff (HRP) Model Integration:**
- **Hook Phase:** Audience profile determines appropriate hook intensity and sophistication
- **Retention Phase:** Attention allocation level maps to required value density throughout
- **Payoff Phase:** Content intent state determines optimal payoff timing and structure

**AIDA Model Integration:**
- **Attention:** Platform expertise level determines how attention is captured
- **Interest:** Niche sophistication determines what creates genuine interest
- **Desire:** Content intent shapes how desire is built and maintained  
- **Action:** Attention allocation influences CTA effectiveness requirements

## Tools Required
- **Read:** Ingest artifact and context from intake stage
- **WebSearch:** Validate audience psychology with targeted query sets
- **WebFetch:** Retrieve detailed information from authoritative sources
- **Write:** Generate structured audience profile output
