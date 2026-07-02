# Test Scenarios — Short-form Video Script Builder (YouTube/TikTok/Reels)

Skill: `shortform-video-script-builder` · idea #69 · cluster `marketing-content-branding`
Comprehensive test suite with real implementations, expected outputs, and pass criteria.

## Test Framework Overview

**Test Categories:**
- **Happy Path:** Standard workflow execution with typical input
- **Edge Cases:** Boundary conditions, ambiguous inputs, degraded modes
- **Integration:** Cross-skill coordination and framework application
- **Quality Gates:** Validation of quality enforcement at each stage
- **Regression:** Consistency checks across multiple runs

**Test Execution Protocol:**
1. Setup: Prepare test input and environment
2. Execute: Run the skill or sub-skill being tested
3. Validate: Compare output against expected criteria
4. Document: Record results, deviations, and calibration needs

---

## Scenario 1: Happy Path — Full Script Evaluation

### Setup
**Input Script (TikTok educational content):**
```
[0-3s HOOK]
Visual: Sudden zoom into face, mouth covered with tape
Audio: "Stop scrolling if you're still using this to grow on TikTok!"

[3-15s BRIDGE & VALUE]
Visual: Remove tape, reveal confident expression
Audio: "Creators who don't use hooks lose 70% of viewers in the first second.
I spent 6 months analyzing 500 viral videos to find what actually works."

[15-45s CORE CONTENT]
Visual: Screen recording of analytics, hook examples side-by-side
Audio: "The 3 hooks that consistently get 300% more retention are:
pattern interrupts, curiosity gaps, and immediate value demonstrations.
Here's exactly how to use each one..."

[45-55s PAYOFF BUILD]
Visual: Montage of applying each hook type
Audio: "When you combine these three, watch what happens to your analytics..."

[55-60s CTA]
Visual: Phone screen with "Follow @creatorcoach" animation
Audio: "Comment 'HOOKS' and I'll send you my full hook template."
```

**Intake Context:**
- Platform: TikTok
- Niche: Creator education/growth
- Goal: Engagement (comments) and follows
- Target: Intermediate creators (6-12 months experience)

### Expected Behavior

**Stage 1 (Audience Analysis) Output:**
```
Platform Psychology Mapping:
- Primary Platform: TikTok
- Avg Attention Window: 7-10 seconds (ultra-fast scroll)
- Scroll Speed: Fast (<1s decision on hook)
- Hook Expectation: Visual+Audio pattern interrupt

4-Dimensional Audience Profile:
A. Platform Expertise: Regular (Active TikTok users, understand culture)
   - Implications: Expect platform-native hooks, reject generic content
B. Content Intent: Problem-solving (Looking for growth strategies)
   - Value Delivery: Must show clear, actionable advice
   - Payoff Structure: Immediate practical value
C. Niche Sophistication: Intermediate (6-12 months creating)
   - Complexity Threshold: Moderate complexity acceptable
   - Credibility Requirements: Need proof/stats for claims
D. Attention Allocation: Medium-intent (Browsing with purpose)
   - Hook Immediacy: Strong hook required but some tolerance for setup
   - Value Density: High value per second expected

Framework Selection:
- Primary: Hook-Retention-Payoff (HRP) model
- Secondary: AIDA (Attention-Interest-Desire-Action)
- Dimension Weights: Hook 22%, Retention 16%, Payoff 18%, Shareability 14%, Platform 18%, CTA 12%
```

**Stage 2 (Hook Engineering) Output:**
```
Hook #1: Visual Pattern Interrupt — Tier A — Score: 9.2/10

Hook Concept: Sudden zoom + tape-covered mouth → "Wait, what just happened?"
Hook Script: "Stop scrolling if you're still using this to grow on TikTok!"

3-Second Rule Analysis:
- Instant Pattern Interrupt: 5/5 — Extreme visual disruption
- Immediate Value Signal: 4/5 — Clear promise of better method
- Audio-Visual Sync: 5/5 — Audio reinforces visual shock
- Platform Native Feel: 5/5 — Fits TikTok aesthetic perfectly
- Audience Match: 4/5 — Matches intermediate creator expertise
Overall 3-Second Score: 4.6/5

Curiosity Gap Analysis:
- Gap Type: Information Gap ("What method am I using wrong?")
- Gap Strength: 5/5 — Specific, compelling gap demands resolution
- Resolution Path: Video reveals better methods throughout

Pattern Interrupt Analysis:
- Interrupt Type: Visual Shock
- Impact Score: 5/5 — Breaks scroll pattern involuntarily
- Sustainability: 4/5 — Transitions naturally into value content
- Production Complexity: 2/5 — Simple to execute

[Additional hooks #2-#6 follow with similar analysis...]

Framework Application Notes:
- These hooks strongly support HRP hook phase with pattern interrupt strength
- Retention architecture should capitalize on strong hook foundation
- Payoff delivery must validate the "still using this" setup
```

**Stage 4 (Retention Scoring) Output:**
```
Predicted Retention Curve:
- 0-3s Retention: 72% (vs TikTok avg: 60-75%) — Strong hook performance
- 3-15s Retention: 52% (vs TikTok avg: 40-55%) — Good bridge execution
- 15-45s Retention: 42% (vs TikTok avg: 30-45%) — Solid content delivery
- 45-60s Retention: 38% (vs TikTok avg: 25-40%) — Good payoff and CTA
- Predicted Avg View Duration: 11s (vs TikTok avg: 7-10s)

Dimension Scoring:

Dimension 1: Hook Strength (First 3s) — Score: 4.6/5 — Weight: 22%
- Pattern Interrupt: 5/5 — Extreme visual disruption captures attention
- Value Signal: 4/5 — Clear growth method promise
- Audio-Visual Sync: 5/5 — Perfect reinforcement
- Platform Fit: 5/5 — Native TikTok aesthetic
- Audience Match: 4/5 — Appropriate for intermediate creators

Dimension 2: Retention Architecture — Score: 4.2/5 — Weight: 16%
- Pattern Break Frequency: 4/5 — Good pacing with variety
- Value Distribution: 4/5 — High-value moments throughout
- Transition Strength: 4/5 — Smooth segment transitions

Dimension 3: Payoff & Value Delivery — Score: 4.4/5 — Weight: 18%
- Hook-Payoff Alignment: 5/5 — Perfect delivery on hook promise
- Value Clarity: 4/5 — Clear actionable advice provided
- Timing Satisfaction: 5/5 — Optimal payoff placement
- Value Magnitude: 4/5 — Strong practical value

[Dimensions 4-6 follow with similar detailed scoring...]

Overall Score: 4.38/5.00
Performance Classification: Excellent
Platform Percentile: Estimated top 15% of TikTok educational content

Dimensional Strengths and Weaknesses:
Top 3 Strengths:
1. Hook Strength (4.6/5) — Exceptional pattern interrupt capitalizes on first 3s
2. Platform-Fit & Format (4.5/5) — Native aesthetic and algorithm optimization
3. Payoff & Value Delivery (4.4/5) — Delivers on promise with clear actionable advice

Top 3 Priority Fixes:
1. Shareability/Saveability (4.0/5) — Could enhance conversation starter value
2. Retention Architecture (4.2/5) — Pattern break frequency could be more aggressive
3. Call-to-Action Clarity (3.8/5) — CTA clarity improvement needed
```

**Stage 5 (Quality Review) Output:**
```
Challenge Summary:
Total Challenges Generated: 7
Validated Challenges: 3 (resulting in score revisions)
Critical Issues Identified: 1
Overall Score Impact: -0.15 points

Originality Verification:
- Script Uniqueness: Low Risk — Distinctive hook and value proposition
- Concept Novelty: Medium Risk — Creator education is competitive niche
- Hook Originality: Low Risk — Tape mouth hook is distinctive approach
- Value Proposition: Low Risk — Specific analytics-backed methodology
- Visual Uniqueness: Low Risk — Creative visual execution

Claim Safety Audit:
Claims Identified: 4 total
- Critical Risk: 0 claims
- High Risk: 1 claim ("lose 70% of viewers in first second")
- Medium Risk: 2 claims ("300% more retention", "500 viral videos analyzed")
- Low Risk: 1 claim ("what actually works")

Claim Confidence Scores:
| Claim Statement | Type | Confidence (0-5) | Validation Status | Action Required |
|-----------------|------|------------------|-------------------|-----------------|
| "lose 70% viewers first second" | Statistical | 3.5 | Needs source citation | Add platform research reference |
| "300% more retention" | Statistical | 3.0 | Needs benchmark data | Add comparative study reference |
| "500 viral videos analyzed" | Research Claim | 4.0 | Reasonable methodology | No action required |
| "what actually works" | Expert Opinion | 3.0 | General claim | No action required |

Platform Policy Compliance:
- TikTok: Low Risk — Content compliant, no policy concerns
- YouTube Shorts: Low Risk — Would translate well to Shorts
- Instagram Reels: Medium Risk — Some aesthetic adjustments needed

CTA Strength & Clarity Assessment:
Current CTA: "Comment 'HOOKS' and I'll send you my full hook template"
- CTA Type: Engagement
- Clarity: 4/5 — Clear action specified
- Actionability: 3/5 — Some friction (expecting delivery)
- Relevance: 5/5 — Perfectly aligned with content
- Urgency: 3/5 — Moderate urgency present
- Specificity: 4/5 — Clear comment action defined
- Value Exchange: 4/5 — Good value proposition

CTA Effectiveness Score: 3.8/5

Score Revision Summary:
Original Overall Score: 4.38 / 5.00
Total Challenge Adjustments: -0.15 points
Revised Overall Score: 4.23 / 5.00
Performance Classification: Excellent → Strong
Platform Percentile: Top 15% → Top 25%
```

### Pass Criteria
- [ ] Report contains scoring table for all 6 dimensions
- [ ] Challenge notes document ≥3 counter-arguments
- [ ] Roadmap includes impact/effort ratings for all items
- [ ] Graded citations with evidence tiers present
- [ ] At least one named framework explicitly applied (HRP, AIDA)
- [ ] Overall score within ±0.5 of expected range (4.2-4.6)
- [ ] Platform percentile classification provided
- [ ] All quality gates checked and documented

---

## Scenario 2: Ambiguous Input — Intake Clarification Path

### Setup
**Input Script (Minimal context):**
```
Hey guys, today I'm showing you how to make money online.
It's really simple and anyone can do it.
[...continues with general money-making tips...]
```

**Intake Context:**
- Platform: Not specified
- Niche: Not specified
- Goal: Not specified
- Target: Not specified

### Expected Behavior

**Stage 1 (Audience Analysis) Should Detect Gaps:**
```
⚠️ INSUFFICIENT CONTEXT DETECTED

Missing Information:
- Primary Platform: Not specified — Critical for hook strategy
- Content Niche: Generic "make money online" — Needs specificity
- Goal: Not specified — Required for CTA optimization
- Target Audience: Not specified — Essential for value delivery

Clarification Questions:

1. Platform Selection:
   Which platform is this content for?
   - TikTok (fast-paced, visual hooks)
   - YouTube Shorts (slightly longer, educational focus)
   - Instagram Reels (aesthetic, lifestyle-oriented)
   - Multiple platforms (requires universal approach)

2. Niche Specificity:
   What specific money-making method are you covering?
   - [Please specify: e-commerce, freelancing, investing, etc.]
   - [What makes your approach different from existing content?]

3. Primary Goal:
   What's the main objective of this video?
   - Build followers/community
   - Drive clicks to a link
   - Get comments and engagement
   - Establish expertise/authority

4. Target Audience:
   Who is your ideal viewer for this content?
   - Complete beginners to online income
   - People looking for side hustles
   - aspiring entrepreneurs
   - [Other specific demographic]

⚠️ ANALYSIS HALTED — Awaiting clarification for accurate scoring
```

### Pass Criteria
- [ ] Skill detects insufficient context without fabricating data
- [ ] Asks ≤5 focused clarification questions
- [ ] Does not proceed to scoring without required information
- [ ] Clear explanation of why each piece of information is needed
- [ ] Professional, non-judgmental tone in clarification request

---

## Scenario 3: Offline Mode — Graceful Degradation

### Setup
**Environment:** WebSearch/WebFetch tools unavailable (simulated outage)

**Input Script:**
```
[Same complete script as Scenario 1]
```

**Intake Context:**
```
[Same complete context as Scenario 1]
```

### Expected Behavior

**Each Stage Should Label Degradation:**
```
⚠️ DEGRADED MODE: Research tools unavailable

Analysis proceeding using cached knowledge from SECOND-KNOWLEDGE-BRAIN.md.
Some platform psychology trends and benchmarks may be outdated.
Confidence in predictions is reduced without current validation.

⚠️ FALLBACK MODE ACTIVE
```

**Fallback Performance:**
- Audience profile uses cached platform psychology data
- Hook scoring proceeds with established frameworks
- Retention scoring uses baseline platform averages
- Quality review applies standard evaluation criteria
- All stages complete with clear degradation labels

**Expected Output Format:**
```
## Audience Analysis Profile

⚠️ DEGRADED MODE: Analysis based on cached knowledge from SECOND-KNOWLEDGE-BRAIN.md
⚠️ Platform psychology data may be 3-6 months old
⚠️ Current trends and algorithm changes not reflected in analysis

Platform Psychology Mapping:
[Proceeds with analysis using cached data...]

[Each section includes appropriate degradation notices]

### Fallback Mode Label
Research tools were unavailable during this analysis. The following
components rely on cached knowledge and may not reflect current
platform dynamics:

- Platform attention windows (cached: Q2 2025)
- Algorithm optimization signals (cached: Q1 2025)
- Trending content patterns (cached: Q2 2025)

Recommendation: Re-run analysis with research tools available for
current validation of scoring and recommendations.
```

### Pass Criteria
- [ ] Output explicitly flags fallback mode in every section
- [ ] Still produces a complete scored report
- [ ] All 6 dimensions scored despite research unavailability
- [ ] Clear caveats about potentially outdated information
- [ ] Specific recommendation to re-run with full tools
- [ ] No fabrications of current research or benchmarks

---

## Scenario 4: Challenge Phase — Score Revision

### Setup
**Input Script (Over-optimistic claims):**
```
[0-3s HOOK]
Visual: Extreme close-up, dramatic lighting
Audio: "This one trick made me a millionaire in 30 days!"

[3-60s CONTENT]
[Standard investment advice content]

[45-60s CTA]
Audio: "Comment 'MILLIONAIRE' to get my exclusive investment guide!"
```

**Intake Context:**
- Platform: TikTok
- Niche: Financial/investment education
- Goal: Build authority and get follows

### Expected Behavior

**Stage 5 (Quality Review) Should Surface Challenges:**

**Challenge #1: Claim Safety**
```
Challenge: "The claim 'made me a millionaire in 30 days' lacks specific
verification and could be flagged as misleading financial advice."

Impact: If unsupported, this violates platform financial content policies
and could trigger account penalties. Score reduction: -0.5 points for
Platform-Fit & Format dimension.

Evidence needed: Specific proof of earnings, disclaimers about results
not being typical, or revision to more modest claim.
```

**Challenge #2: Platform Policy Compliance**
```
Challenge: "Financial content promising quick wealth outcomes may violate
TikTok's financial content policy requiring responsible messaging."

Impact: High risk of content suppression or account warning. This is a
critical policy violation that must be addressed before deployment.

Evidence needed: TikTok financial content policy documentation and
examples of compliant financial content CTAs.
```

**Challenge #3: Scoring Robustness**
```
Challenge: "Hook Strength score of 4.5/5 assumes viewers will find
'one trick' claims credible. Given financial content skepticism, actual
pattern interrupt effectiveness may be lower."

Impact: If valid, Hook Strength score should be reduced to 3.5/5 to
reflect audience trust barriers in financial niche.

Evidence needed: Research on financial content engagement patterns
and viewer skepticism toward "get rich quick" claims.
```

**Revised Score Calculation:**
```
Original Overall Score: 4.10 / 5.00
Challenge Adjustments:
  - Challenge #1: -0.50 points (Platform-Fit & Format)
  - Challenge #2: -0.30 points (CTA Clarity - policy risk)
  - Challenge #3: -1.00 points (Hook Strength - credibility)
Revised Overall Score: 2.30 / 5.00
Performance Classification: Excellent → Poor
Platform Percentile: Top 15% → Bottom 30%

⚠️ CRITICAL: Multiple policy and credibility issues detected
⚠️ Priority revision required before deployment
```

**Revision Recommendations:**
```
P0 - Critical (Fix Before Deployment):
1. Financial Claim Accuracy — "made millionaire in 30 days" → "built
   wealth through disciplined investing" — Removes policy violation
2. Results Disclaimer — Add "results not typical, investing involves
   risk" — Addresses regulatory compliance

P1 - High (Strongly Recommended):
1. Hook Credibility — Replace "one trick" with specific strategy name
   — Improves audience trust and engagement
2. CTA Revision — "MILLIONAIRE" → "INVEST" — More appropriate action
```

### Pass Criteria
- [ ] ≥3 counter-arguments generated and documented
- [ ] At least one score revised based on challenges
- [ ] Challenge documentation shows impact on specific dimensions
- [ ] Revised scores calculated with full breakdown
- [ ] Revision recommendations prioritized by severity
- [ ] Policy violations flagged with specific guidance
- [ ] Performance classification reflects significant score changes

---

## Scenario 5: Roadmap-Only Request

### Setup
**User Request:**
```
"I've already made my video. Just tell me what I should improve first.
Skip the full analysis, just give me the prioritized roadmap."
```

**Input Script:**
```
[Any complete script - using Scenario 1 script]
```

### Expected Behavior

**Streamlined Output:**
```
# Prioritized Improvement Roadmap

Based on retention scoring analysis, here are your improvements ranked
by impact (H/M/L) and effort (H/M/L):

## Tier 1: High Impact, Low Effort (Immediate Wins)

| # | Recommendation | Impact | Effort | Framework Basis |
|---|----------------|--------|--------|-----------------|
| 1 | Strengthen CTA clarity: Change "Comment 'HOOKS'" to "Comment
   'HOOKS' below and check your notifications in 5 minutes" | H | L | CTA Clarity
   dimension, Actionability sub-dimension |
| 2 | Add pattern break at 25s: Quick cut to B-roll or visual change
   to reset attention | M | L | Retention Architecture,
   Pattern Break Frequency research |

## Tier 2: High Impact, Medium Effort (Significant Gains)

| # | Recommendation | Impact | Effort | Framework Basis |
|---|----------------|--------|--------|-----------------|
| 3 | Enhance shareability: Add "Save this for your next video" line
   at 50s to drive save behavior | H | M | Shareability/Saveability
   dimension, Save Utility research |
| 4 | Improve value density: Add specific example or case study at
   35s to reduce content lull | M | M | Retention Architecture,
   Value Distribution framework |

## Tier 3: Medium Impact, Medium Effort (Future Iterations)

| # | Recommendation | Impact | Effort | Framework Basis |
|---|----------------|--------|--------|-----------------|
| 5 | Optimize for Reels: Create Instagram-specific version with
   slightly slower pacing | M | M | Platform-Fit & Format,
   algorithm optimization research |

[Additional tiers as needed...]

Quick Stats:
- Your video scores: 4.23/5 (Strong, top 25% of platform content)
- Highest priority fix addresses: CTA Actionability (3/5 → 5/5)
- Expected improvement: +0.15 overall score, +10-15% engagement rate

⚠️ This roadmap is based on full analysis. For detailed scoring and
framework applications, request complete evaluation report.
```

### Pass Criteria
- [ ] Output is roadmap-only format (not full report)
- [ ] Roadmap items ranked by impact × effort priority
- [ ] Each item includes specific, actionable recommendation
- [ ] Framework basis cited for each recommendation
- [ ] Clear tier structure (immediate wins → long-term improvements)
- [ ] Impact/effort ratings consistent with full analysis
- [ ] Traceable to underlying dimensional scores
- [ ] No fabrication of analysis not supported by scoring

---

## Regression Checklist

**Run after any code changes to ensure consistency:**

- [ ] All 6 dimensions appear in every scoring table
- [ ] At least one named framework cited per run (HRP, AIDA, etc.)
- [ ] Evidence tiers labeled on every external claim
- [ ] Roadmap items ranked by impact × effort (not just impact alone)
- [ ] Challenge phase generates ≥3 counter-arguments
- [ ] Quality gates checked before final output in every scenario
- [ ] Fallback mode labeled when research unavailable
- [ ] Platform-specific adjustments applied correctly
- [ ] Score calculations consistent across multiple runs (±0.5)
- [ ] Dimension weights applied consistently from Stage 2 to Stage 4
- [ ] All sub-skills complete without errors in happy path
- [ ] Error handling graceful in edge cases

---

## Test Execution Protocol

**How to Run These Tests:**

1. **Automated Testing (when available):**
   ```bash
   npm run test:scenarios
   # Or
   python tests/run_scenarios.py
   ```

2. **Manual Testing:**
   - Copy each scenario's input exactly as provided
   - Run the skill with the input
   - Compare output against expected behavior
   - Document any deviations or issues

3. **Regression Testing:**
   - Run full scenario suite after any code changes
   - Verify regression checklist items pass
   - Document any score variations beyond ±0.5 tolerance

**Test Result Documentation:**
For each scenario test, document:
- Date run
- Skill version
- Pass/fail for each criterion
- Score values achieved vs. expected
- Deviations noted and their impact
- Calibration needs identified

**Continuous Improvement:**
Use scenario results to:
- Calibrate scoring rubrics for accuracy
- Refine framework application logic
- Improve quality gate enforcement
- Enhance error handling and edge cases
- Strengthen research validation processes
