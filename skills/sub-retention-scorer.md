---
name: sub-retention-scorer
description: (shortform-video-script-builder) Map the script to a second-by-second retention curve and score against the HRP model and platform watch-time norms.
---

# Sub-skill: retention-scorer

## Purpose
Map the video script to a second-by-second retention curve and score against the Hook-Retention-Payoff (HRP) model and platform watch-time norms. This stage provides the quantitative backbone of the evaluation, translating qualitative content features into predicted retention performance across 6 critical dimensions.

## When the Harness Calls This
Stage 4 of the `shortform-video-script-builder` main workflow, following research/evidence gathering. Must complete before challenge phase.

## Inputs
- **Primary:** User's video script with timing/visual cues
- **From Stage 1:** Audience profile (platform psychology, attention windows)
- **From Stage 2:** Selected hooks with 3-Second Rule scores
- **From Stage 3:** Research evidence and framework applications
- **Framework Reference:** Hook-Retention-Payoff (HRP) model, dimension weights from hook engineering

## Procedure

### 1. Content-Timing Mapping
Parse the script into second-by-second segments with content classification:

**Segment Classification System:**
| Segment Type | Duration Range | Retention Risk | Value Delivery |
|--------------|----------------|----------------|-----------------|
| **Hook** | 0-3s | Critical | Pattern interrupt + value signal |
| **Bridge** | 3-7s | High | Connect hook to core content |
| **Content Intro** | 7-15s | Medium-High | Establish value proposition |
| **Core Content** | 15-45s | Medium | Primary information delivery |
| **Pattern Break** | Every 8-12s | Variable | Reset attention, prevent fatigue |
| **Payoff Build** | 45-55s | Medium | Build toward resolution |
| **Payoff Delivery** | 55-58s | Critical | Deliver promised value |
| **CTA Setup** | 58-60s | High | Set up call-to-action |
| **CTA Delivery** | 60s end | Critical | Action prompt |

**Mapping Template:**
```
| Time | Content Type | Visual | Audio | Retention Risk | Value Score |
|------|--------------|--------|-------|----------------|-------------|
| 0-0.5s | Hook-Visual | [description] | [audio] | Critical | Pattern-Interrupt |
| 0.5-1.5s | Hook-Audio | [description] | [script] | Critical | Value-Signal |
| 1.5-3s | Hook-Resolution | [description] | [script] | High | Gap-Creation |
| [... continue for full script ...]
```

### 2. Retention Curve Prediction
Generate a predicted retention curve using this model:

**Baseline Platform Retention:**
| Platform | 0-3s Retention | 3-15s Retention | 15-45s Retention | 45-60s Retention | Avg View Duration |
|----------|---------------|-----------------|------------------|------------------|-------------------|
| TikTok | 60-75% | 40-55% | 30-45% | 25-40% | 7-10s |
| YouTube Shorts | 65-80% | 50-65% | 40-55% | 35-50% | 10-15s |
| Instagram Reels | 62-78% | 45-60% | 35-50% | 30-45% | 8-12s |

**Content Adjustment Modifiers:**
```
Hook Quality Bonus: (3-Second Score - 3) × 5% retention boost
Pattern Break Bonus: +3% retention per effective pattern break
Value Density Bonus: +2% retention per high-value segment
Pacing Penalty: -1% retention per pacing weak point
Length Penalty: -0.5% retention per 5s over 60s optimum
```

**Predicted Curve Generation:**
```
For each second 0-60:
  Base Retention = [Platform baseline for time period]
  + Content Modifiers
  + Audience Adjustment (attention allocation factor)
  = Predicted Retention %
```

**Output Visualization:**
```
Retention Curve:
100% |█
 90% |███
 80% |████
 70% |██████
 60% |████████← Hook strength establishes baseline
 50% |███████████
 40% |██████████████
 30% |██████████████████
 20% |███████████████████████
 10% |████████████████████████████
  0% |████████████████████████████████
     0   10   20   30   40   50   60 seconds
```

### 3. Dimension 1: Hook Strength (First 3s) Scoring
**Weight:** [From Stage 2 framework selection, typically 18-22%]

**Scoring Rubric (0-5):**

| Score | Pattern Interrupt | Value Signal | Audio-Visual Sync | Platform Fit |
|-------|-------------------|--------------|-------------------|--------------|
| **5** | Instant, involuntary attention capture | Crystal clear by 1s | Perfectly reinforcing | Native-feeling |
| **4** | Strong pattern break | Clear by 1.5s | Good reinforcement | Appropriate |
| **3** | Adequate break | Discernible by 2s | Decent alignment | Acceptable |
| **2** | Weak/subtle break | Vague/unclear | Poor alignment | Awkward |
| **1** | Minimal interrupt | Missing value signal | Misaligned | Jarring |
| **0** | No interrupt | No value signal | Detrimental | Platform-hostile |

**Evidence Requirements:**
- Cite 3-Second Hook Rule research or platform guidelines
- Reference pattern interrupt attention studies
- Use hook engineering scores from Stage 2 as foundation

### 4. Dimension 2: Retention Architecture Scoring
**Weight:** [From Stage 2, typically 15-18%]

**Pacing Analysis Framework:**

**Pattern Break Frequency (0-5 points):**
- 5: Pattern breaks every 8-10 seconds, maintains attention
- 4: Pattern breaks every 10-12 seconds, adequate pacing
- 3: Pattern breaks every 12-15 seconds, some fatigue risk
- 2: Pattern breaks every 15-20 seconds, notable fatigue zones
- 1: Pattern breaks >20 seconds apart, major fatigue
- 0: No pattern breaks, monotone delivery

**Value Distribution Quality (0-5 points):**
- 5: High-value moments distributed throughout, no dead zones
- 4: Good value distribution, minor lulls between peaks
- 3: Adequate distribution, some low-value segments
- 2: Uneven distribution, significant weak portions
- 1: Poor distribution, most value front or back-loaded
- 0: No value structure, random or absent value delivery

**Transition Strength (0-5 points):**
- 5: Seamless, invisible transitions between segments
- 4: Smooth transitions, minimal cognitive load
- 3: Functional transitions, some awkward moments
- 2: Rough transitions, noticeable jarring points
- 1: Poor transitions, disrupt viewing flow
- 0: No transitions, disjointed segments

**Dimension 2 Composite Score:**
```
(Pattern Break Frequency × 0.35) + (Value Distribution × 0.40) + 
(Transition Strength × 0.25) = Retention Architecture Score
```

### 5. Dimension 3: Payoff & Value Delivery Scoring
**Weight:** [From Stage 2, typically 16-20%]

**Payoff Quality Framework:**

**Hook-Payoff Alignment (0-5 points):**
- 5: Perfect alignment, hook promise fully realized
- 4: Strong alignment, minor expectation gaps
- 3: Adequate alignment, some expectations met
- 2: Weak alignment, significant expectation failures
- 1: Poor alignment, hook largely unaddressed
- 0: No alignment, hook and payoff disconnected

**Value Clarity (0-5 points):**
- 5: Crystal clear, unambiguous value delivery
- 4: Clear value, minor interpretation needed
- 3: Discernible value, some ambiguity present
- 2: Unclear value, significant interpretation required
- 1: Minimal value, barely discernible payoff
- 0: No value, no meaningful payoff delivered

**Timing Satisfaction (0-5 points):**
- 5: Optimal timing, payoff delivered at peak interest
- 4: Good timing, payoff delivered at appropriate moment
- 3: Adequate timing, payoff reasonably placed
- 2: Suboptimal timing, payoff too early or late
- 1: Poor timing, payoff disrupts flow
- 0: Terrible timing, payoff undermines engagement

**Value Magnitude (0-5 points):**
- 5: Exceptional value, exceeds viewer expectations
- 4: Strong value, meets high expectations
- 3: Adequate value, meets baseline expectations
- 2: Weak value, below average expectations
- 1: Minimal value, barely worth watching
- 0: No value, wasted viewer time

**Dimension 3 Composite Score:**
```
(Alignment × 0.30) + (Clarity × 0.30) + (Timing × 0.20) + 
(Magnitude × 0.20) = Payoff & Value Delivery Score
```

### 6. Dimension 4: Shareability / Saveability Scoring
**Weight:** [From Stage 2, typically 12-16%]

**Shareability Framework:**

**Social Currency Potential (0-5 points):**
- 5: High share-signal value, enhances sharer's identity
- 4: Good share-signal value, positive identity association
- 3: Moderate share-signal value, neutral identity impact
- 2: Low share-signal value, minimal social benefit
- 1: Negative share-signal value, potential embarrassment
- 0: Anti-shareable, actively harms sharer's image

**Conversation Starter Value (0-5 points):**
- 5: Natural conversation catalyst, inherently discussable
- 4: Strong conversation starter, notable talking points
- 3: Moderate conversation value, some discussion potential
- 2: Weak conversation starter, limited discussion topics
- 1: Minimal conversation value, not worth mentioning
- 0: No conversation value, nothing to discuss

**Save Utility (0-5 points):**
- 5: High reference value, worth rewatching multiple times
- 4: Good reference value, worth occasional revisiting
- 3: Moderate reference value, potentially worth saving
- 2: Low reference value, marginal save motivation
- 1: Minimal reference value, rarely worth saving
- 0: No reference value, not worth saving

**Emotional Resonance (0-5 points):**
- 5: Strong emotional trigger (inspired/outraged/delighted)
- 4: Good emotional trigger, clear emotional response
- 3: Moderate emotional trigger, mild emotional response
- 2: Weak emotional trigger, minimal emotional response
- 1: No emotional trigger, flat emotional experience
- 0: Negative emotional trigger, creates aversion

**Dimension 4 Composite Score:**
```
(Social Currency × 0.30) + (Conversation Value × 0.25) + 
(Save Utility × 0.25) + (Emotional Resonance × 0.20) = 
Shareability / Saveability Score
```

### 7. Dimension 5: Platform-Fit & Format Scoring
**Weight:** [From Stage 2, typically 14-18%]

**Platform Optimization Framework:**

**Vertical Format Optimization (0-5 points):**
- 5: Perfect vertical framing, maximizes screen real estate
- 4: Good vertical framing, effective screen use
- 3: Adequate vertical framing, acceptable screen use
- 2: Suboptimal framing, wasted screen space
- 1: Poor framing, significant screen waste
- 0: Horizontal/incorrect format, platform-incompatible

**Platform Native Styling (0-5 points):**
- 5: Fully native aesthetic, indistinguishable from top creators
- 4: Strong native styling, matches platform conventions
- 3: Moderate native styling, mostly appropriate
- 2: Weak native styling, some platform-alien elements
- 1: Poor native styling, feels out of place
- 0: Platform-hostile, actively rejects conventions

**Algorithm Optimization (0-5 points):**
- 5: Fully optimized for platform algorithm signals
- 4: Well-optimized for most algorithm factors
- 3: Moderately optimized, covers key algorithm signals
- 2: Poorly optimized, missing key signals
- 1: Barely optimized, minimal algorithm consideration
- 0: Algorithm-hostile, actively hurts performance

**Length Optimization (0-5 points):**
- 5: Optimal length for platform/content combination
- 4: Good length, near-optimal for use case
- 3: Adequate length, acceptable for platform
- 2: Suboptimal length, too short or long for content
- 1: Poor length, significantly off optimal range
- 0: Terrible length, platform-hostile duration

**Dimension 5 Composite Score:**
```
(Format Optimization × 0.30) + (Native Styling × 0.25) + 
(Algorithm Optimization × 0.25) + (Length Optimization × 0.20) = 
Platform-Fit & Format Score
```

### 8. Dimension 6: Call-to-Action Clarity Scoring
**Weight:** [From Stage 2, typically 10-14%]

**CTA Framework:**

**CTA Presence (0-5 points):**
- 5: Clear, explicit CTA that's impossible to miss
- 4: Strong CTA that most viewers will notice
- 3: Adequate CTA that attentive viewers will catch
- 2: Weak CTA that's easily missed
- 1: Minimal CTA that's barely present
- 0: No CTA, no action requested

**CTA Clarity (0-5 points):**
- 5: Crystal clear, unambiguous action specified
- 4: Clear CTA with minor interpretation needed
- 3: Adequate clarity, some ambiguity acceptable
- 2: Unclear CTA, significant interpretation required
- 1: Vague CTA, action not clearly specified
- 0: No clear CTA, no specific action requested

**CTA Actionability (0-5 points):**
- 5: Immediately actionable, zero friction to execute
- 4: Highly actionable, minimal friction to execute
- 3: Moderately actionable, some friction present
- 2: Low actionability, significant friction involved
- 1: Barely actionable, high friction barriers
- 0: Not actionable, impossible to execute CTA

**CTA Relevance (0-5 points):**
- 5: Perfectly relevant to content and audience intent
- 4: Highly relevant, appropriate to content
- 3: Moderately relevant, some connection to content
- 2: Weakly relevant, tangential to content
- 1: Poorly relevant, disconnected from content
- 0: Irrelevant, no connection to content

**Dimension 6 Composite Score:**
```
(Presence × 0.25) + (Clarity × 0.30) + (Actionability × 0.25) + 
(Relevance × 0.20) = Call-to-Action Clarity Score
```

### 9. Composite Score Calculation
Apply the dimension weights determined in Stage 2:

```
Overall Score = 
  (Hook Strength × Weight1) +
  (Retention Architecture × Weight2) +
  (Payoff & Value Delivery × Weight3) +
  (Shareability/Saveability × Weight4) +
  (Platform-Fit & Format × Weight5) +
  (Call-to-Action Clarity × Weight6)

Overall Score / 5 = Final X.X / 5 Rating
```

**Performance Classification:**
| Score Range | Classification | Expected Performance |
|-------------|----------------|---------------------|
| 4.5-5.0 | Exceptional | Top 5% of platform content |
| 4.0-4.4 | Excellent | Top 15% of platform content |
| 3.5-3.9 | Strong | Top 30% of platform content |
| 3.0-3.4 | Competent | Above average performance |
| 2.5-2.9 | Adequate | Average performance |
| 2.0-2.4 | Weak | Below average performance |
| 1.5-1.9 | Poor | Bottom 30% of platform content |
| 1.0-1.4 | Terrible | Bottom 15% of platform content |
| 0.0-0.9 | Failing | Bottom 5% of platform content |

### 10. Research Validation
Use WebSearch to validate scoring against platform benchmarks:

**Validation Queries:**
```
"[platform] retention benchmarks [year]"
"[platform] average view duration [content type]"
"short-form video performance metrics [year]"
"[platform] creator retention insights"
```

**Benchmark Comparison:**
- Compare predicted retention curve to platform averages
- Validate dimension scores against creator case studies
- Cross-reference scoring with industry best practices
- Note any significant deviations from expected patterns

### 11. Structured Output Generation
```markdown
## Retention Scoring Report

### Content-Timing Mapping
[Complete timing table from Section 1]

### Predicted Retention Curve
[Retention curve visualization and data table]

**Retention Predictions:**
- 0-3s Retention: X% (vs platform avg: Y%)
- 3-15s Retention: X% (vs platform avg: Y%)
- 15-45s Retention: X% (vs platform avg: Y%)
- 45-60s Retention: X% (vs platform avg: Y%)
- Predicted Avg View Duration: Xs (vs platform avg: Ys)

### Dimension Scoring

#### Dimension 1: Hook Strength (First 3s) — Score: X.X/5 — Weight: X%
**Pattern Interrupt:** X/5 — [Specific justification]
**Value Signal:** X/5 — [Specific justification]
**Audio-Visual Sync:** X/5 — [Specific justification]
**Platform Fit:** X/5 — [Specific justification]
**Audience Match:** X/5 — [Specific justification]

**Composite Calculation:** [Show math]
**Evidence Source:** [Citation with evidence tier]

[Repeat for Dimensions 2-6 with appropriate sub-dimensions]

### Overall Score Calculation
**Dimension Scores with Applied Weights:**
| Dimension | Score (0-5) | Weight | Weighted Score |
|-----------|-------------|--------|----------------|
| Hook Strength | X.X | XX% | X.XX |
| Retention Architecture | X.X | XX% | X.XX |
| Payoff & Value Delivery | X.X | XX% | X.XX |
| Shareability/Saveability | X.X | XX% | X.XX |
| Platform-Fit & Format | X.X | XX% | X.XX |
| Call-to-Action Clarity | X.X | XX% | X.XX |

**Overall Score:** X.XX / 5.00
**Performance Classification:** [Exceptional/Excellent/Strong/etc.]
**Platform Percentile:** Estimated top X% of [platform] content

### Dimensional Strengths and Weaknesses

**Top 3 Strengths:**
1. [Dimension] (X.X/5) — [Why this is strong and how to leverage]
2. [Dimension] (X.X/5) — [Why this is strong and how to leverage]
3. [Dimension] (X.X/5) — [Why this is strong and how to leverage]

**Top 3 Priority Fixes:**
1. [Dimension] (X.X/5) — [Why this is weak and impact of improvement]
2. [Dimension] (X.X/5) — [Why this is weak and impact of improvement]
3. [Dimension] (X.X/5) — [Why this is weak and impact of improvement]

### Framework Application Notes
[How HRP model was applied throughout scoring]
[Connection to Stage 2 hook scores]
[Foundation for challenge phase considerations]

### Research Validation
[Benchmark comparisons and validation notes]

### Research Sources
1. [Source] — [Evidence Tier] — [Applied to which dimensions/scoring]
2. [Additional sources...]

### Fallback Mode Label
[If research unavailable, explicit degradation label]
```

## Outputs
- **Primary:** 6-dimension scoring with detailed sub-dimension analysis
- **Secondary:** Predicted retention curve with benchmark comparison
- **Tertiary:** Overall composite score with performance classification
- **Quaternary:** Strengths/weaknesses analysis for challenge phase

## Quality Gate
**ALL conditions must be TRUE before passing to challenge phase:**

- [ ] Content-timing mapping covers full 0-60s duration
- [ ] Predicted retention curve includes all platform benchmark comparisons
- [ ] All 6 dimensions scored with complete sub-dimension breakdown
- [ ] Each dimension score includes evidence citation or fallback label
- [ ] Composite score calculation shown with applied weights
- [ ] Performance classification matches overall score range
- [ ] Top 3 strengths and 3 weaknesses clearly identified
- [ ] Research validation includes minimum 2 sources or explicit fallback
- [ ] Output formatted in specified markdown structure

## Failure Modes and Recovery

**Script Timing Ambiguity Recovery:**
If script lacks clear timing/segmentation:
1. Apply standard timing assumptions based on word count
2. Flag assumptions with "⚠️ ESTIMATED TIMING" labels
3. Recommend timestamp additions for accurate analysis
4. Provide multiple timing scenarios if feasible

**Dimension Weight Mismatch Recovery:**
If Stage 2 weights seem misaligned with content:
1. Note the mismatch with justification
2. Suggest weight adjustments for this specific case
3. Calculate alternative overall score with adjusted weights
4. Flag for framework reconsideration

**Research Tool Failure Recovery:**
If WebSearch/WebFetch unavailable:
1. Apply baseline scoring from established frameworks
2. Use platform averages from SECOND-KNOWLEDGE-BRAIN.md
3. Explicitly label degraded mode with potential outdated data
4. Note confidence level in predictions without validation

## Framework Application Notes

**Hook-Retention-Payoff (HRP) Model Integration:**
- **Hook Phase:** Dimension 1 scoring directly measures HRP hook quality
- **Retention Phase:** Dimension 2 scoring measures HRP retention architecture
- **Payoff Phase:** Dimension 3 scoring measures HRP payoff delivery
- **Model Alignment:** All three phases must be strong for HRP success

**Platform Retention Analytics:**
- **Average View Duration:** Predicted duration compared to platform norms
- **Watch-Time Distribution:** Second-by-second retention curve visualization
- **Re-watch Potential:** Incorporated into shareability/saveability scoring
- **Algorithm Signals:** Platform-fit dimension includes algorithm optimization

## Tools Required
- **Read:** Ingest audience profile, hook scores, research evidence, and script
- **WebSearch:** Validate scoring against platform benchmarks and creator studies
- **WebFetch:** Retrieve detailed platform analytics and best practices
- **Write:** Generate comprehensive retention scoring report
