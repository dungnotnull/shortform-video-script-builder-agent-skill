---
name: sub-quality-reviewer
description: (shortform-video-script-builder) Devil's-advocate pass: check originality, claim safety, platform policy fit and CTA strength before final output.
---

# Sub-skill: quality-reviewer

## Purpose
Devil's-advocate pass: check originality, claim safety, platform policy fit, and CTA strength before final output. This stage challenges all previous conclusions, surfaces potential weaknesses, validates safety and compliance, and ensures the analysis is robust enough to withstand real-world deployment.

## When the Harness Calls This
Stage 5 of the `shortform-video-script-builder` main workflow, following retention scoring. This is the final analytical stage before synthesis and must complete before deliverable assembly.

## Inputs
- **Primary:** User's video script and all previous stage outputs
- **From Stage 1:** Audience profile with psychology assumptions
- **From Stage 2:** Hook selection and framework application
- **From Stage 3:** Research evidence and sources
- **From Stage 4:** Retention scores and dimensional analysis
- **Framework Reference:** All applied frameworks, quality standards, platform policies

## Procedure

### 1. Challenge Framework Setup
Establish systematic challenge areas to test the robustness of all prior conclusions:

**Challenge Categories:**
| Category | Purpose | Failure Impact |
|----------|---------|----------------|
| **Originality Verification** | Ensure content isn't derivative or plagiarized | Legal/Reputation risk |
| **Claim Safety Audit** | Validate factual claims and avoid misinformation | Credibility/Policy risk |
| **Platform Policy Compliance** | Verify content follows platform guidelines | Takedown/Suspension risk |
| **CTA Strength & Clarity** | Ensure calls-to-action are effective and appropriate | Conversion performance |
| **Scoring Robustness** | Challenge retention scoring assumptions | Analysis reliability |
| **Audience Assumptions** | Stress-test audience profile conclusions | Targeting accuracy |

**Challenge Methodology:**
For each category, generate 3-5 specific challenges with:
- **Challenge statement:** What weakness or assumption is being questioned
- **Impact assessment:** What happens if this challenge is valid
- **Evidence requirement:** What proof is needed to dismiss the challenge
- **Revision implication:** How scoring/recommendations would change if validated

### 2. Originality Verification
Systematically check for originality concerns across multiple dimensions:

**Plagiarism Risk Assessment:**

| Originality Dimension | Risk Indicators | Validation Method | Failure Threshold |
|-----------------------|-----------------|-------------------|-------------------|
| **Script Uniqueness** | Phrasing matches existing viral content | WebSearch exact phrase matching | >3 consecutive identical phrases |
| **Concept Novelty** | Core idea identical to recent trends | Cross-reference trending content databases | Exact concept match within 30 days |
| **Hook Originality** | Hook matches recent viral hooks | Hook pattern database search | Identical hook structure within 60 days |
| **Value Proposition** | Claims identical to competitors | Competitive content analysis | No differentiated value |
| **Visual Uniqueness** | Staging/cinematography duplicates existing | Visual reference comparison | Exact visual setup match |

**Derivative Content Detection:**
```
1. Extract key phrases from script (sentences, hooks, CTA)
2. WebSearch each phrase + "short-form video" + platform name
3. Analyze top 10 results for structural matches
4. Flag any content with >70% structural similarity
5. Assess whether similarity is coincidental or derivative
```

**Originality Enhancement Recommendations:**
- **For detected derivatives:** Suggest specific rephrasing or angle differentiation
- **For concept overlaps:** Recommend unique value addition or distinctive framing
- **For hook similarities:** Propose alternative hooks from unused strategies
- **For visual duplicates:** Advise staging/format modifications

**Challenge Generation:**
```
Challenge #1: "This hook is structurally identical to [viral example] from [date]. 
Why would this perform differently given algorithm deduplication?"
Impact: If valid, hook score should be reduced by 2 points for lack of originality.
Evidence needed: Demonstrate distinct value proposition or execution difference.
```

### 3. Claim Safety Audit
Validate all factual, scientific, and expert claims for accuracy and support:

**Claim Classification System:**

| Claim Type | Risk Level | Verification Required | Consequences of False Claims |
|------------|------------|------------------------|------------------------------|
| **Scientific/Research** | Critical | Peer-reviewed sources | Credibility damage, policy violation |
| **Statistical/Data** | High | Original data sources | Misinformation penalties |
| **Expert Testimonial** | Medium | Expert credentials verification | Expertise questioning |
| **Industry Benchmark** | Medium | Industry reports/studies | Comparative accuracy questions |
| **Platform Performance** | Low | Platform official guidance | Strategy accuracy questions |
| **Audience Psychology** | Low | Research validation | Strategic misalignment |

**Claim Verification Protocol:**
```
For each claim identified in the script:
1. Classify claim type and risk level
2. Extract specific claim statement
3. WebSearch for authoritative validation
4. Assess source quality against evidence hierarchy
5. Note any discrepancies or缺乏 support
6. Calculate claim confidence score
```

**Claim Confidence Scoring (0-5):**
- **5:** Supported by systematic review or meta-analysis
- **4:** Supported by multiple high-quality single studies
- **3:** Supported by expert consensus or industry standards
- **2:** Supported by single study or expert opinion
- **1:** Anecdotally supported but not verified
- **0:** Unsupported or contradicted by evidence

**Unsafe Claim Identification:**
Flag claims that could trigger:
- Platform misinformation policies
- Legal liability (defamation, false advertising)
- Professional credibility damage
- Audience trust erosion

**Challenge Generation:**
```
Challenge #2: "The claim '[specific claim]' is not supported by current research. 
What evidence validates this, and could this be flagged as misinformation?"
Impact: If unsupported, claim must be removed or qualified. Score reduction: 1 point.
Evidence needed: Peer-reviewed sources or platform-acceptable authoritative sources.
```

### 4. Platform Policy Compliance
Verify content against platform content policies and community guidelines:

**Platform Policy Framework:**

| Policy Area | TikTok | YouTube Shorts | Instagram Reels |
|-------------|--------|----------------|-----------------|
| **Misinformation** | Strict | Strict | Moderate |
| **Medical/Health Claims** | Very Strict | Strict | Strict |
| **Financial Advice** | Strict | Strict | Moderate |
| **Controversial Content** | Moderate | Strict | Moderate |
| **Intellectual Property** | Very Strict | Strict | Strict |
| **Harassment/Bullying** | Very Strict | Strict | Strict |
| **Hate Speech** | Very Strict | Very Strict | Very Strict |
| **Sexual Content** | Strict | Strict | Moderate |
| **Dangerous Acts** | Strict | Strict | Strict |

**Compliance Checking Protocol:**
```
1. Identify policy-relevant content areas in script
2. Cross-reference with platform policy documentation
3. Assess content against specific policy language
4. Flag borderline or potentially problematic content
5. Recommend modifications for compliance assurance
```

**Policy Risk Categories:**
- **Critical Risk:** Content that could trigger immediate removal
- **High Risk:** Content that could trigger demonetization or shadowban
- **Medium Risk:** Content that could trigger warning or limited distribution
- **Low Risk:** Content with minimal policy concerns
- **No Risk:** Content fully compliant with all policies

**Platform-Specific Considerations:**

**TikTok-Specific Risks:**
- Rapid policy enforcement with minimal appeals
- Aggressive stance on misinformation and health claims
- Strict IP enforcement with automated detection
- Sensitive to "dangerous acts" even with disclaimers

**YouTube Shorts-Specific Risks:**
- Medical/health claims require qualified expert attribution
- Financial advice requires clear disclaimer language
- Misinformation can trigger entire channel penalties
- Strong enforcement on controversial public interest topics

**Instagram Reels-Specific Risks:**
- Aesthetic standards can affect distribution
- Commercial content requires proper disclosure
- IP enforcement particularly aggressive for music/visuals
- Community standards applied inconsistently

**Challenge Generation:**
```
Challenge #3: "The content discussing [topic] may violate [platform] [policy] policy. 
What modifications ensure full compliance while maintaining effectiveness?"
Impact: If non-compliant, content faces removal risk. Priority fix: Critical.
Evidence needed: Platform policy documentation and compliance examples.
```

### 5. CTA Strength & Clarity Assessment
Evaluate calls-to-action for effectiveness and appropriateness:

**CTA Effectiveness Framework:**

| CTA Dimension | Evaluation Criteria | Scoring (0-5) | Performance Impact |
|---------------|---------------------|---------------|-------------------|
| **Clarity** | Unambiguous action specified | 0-5 | Direct conversion impact |
| **Actionability** | Minimal friction to execute | 0-5 | Immediate action rate |
| **Relevance** | Connected to content value | 0-5 | Audience response quality |
| **Urgency** | Motivates timely action | 0-5 | Action prompt effectiveness |
| **Specificity** | Precise next step identified | 0-5 | Follow-through clarity |
| **Value Exchange** | Clear benefit for action | 0-5 | Motivation strength |

**CTA Type Analysis:**

**Follow/Sub CTA Requirements:**
- Clear value proposition for following
- Specific reason to follow (not just "follow me")
- Content preview for future value
- Low-friction follow mechanism

**Engagement CTA Requirements:**
- Specific engagement action (like, comment, share)
- Reason for engagement (helps algorithm, etc.)
- Easy-to-execute engagement request
- Social proof or reciprocity trigger

**Conversion CTA Requirements:**
- Clear conversion destination
- Strong value exchange
- Minimal steps to conversion
- Urgency or scarcity element

**Save CTA Requirements:**
- Clear save value (reference content)
- Specific when-to-save scenario
- Future-use case articulated
- Save motivation established

**Challenge Generation:**
```
Challenge #4: "The CTA '[current CTA]' lacks [specific dimension]. 
What specific improvement would increase conversion by [estimated] %?"
Impact: Improved CTA could increase conversion by 2-5X. Priority: High.
Evidence needed: CTA best practices research and platform guidance.
```

### 6. Scoring Robustness Challenge
Stress-test retention scoring assumptions and conclusions:

**Challenge Areas for Each Dimension:**

**Dimension 1 (Hook Strength) Challenges:**
- Is pattern interrupt actually distinctive or blend into platform noise?
- Does value signal truly register in first 1.5s or is score optimistic?
- Are audio-visual elements realistically achievable in production?
- Platform fit assessment based on current trends or outdated norms?

**Dimension 2 (Retention Architecture) Challenges:**
- Pattern break frequency too conservative for actual attention spans?
- Value distribution analysis assumes ideal viewer focus level?
- Transition strength overestimates production execution quality?
- Length optimization fails to account for content complexity?

**Dimension 3 (Payoff & Value) Challenges:**
- Hook-payoff alignment assumes perfect viewer memory of hook?
- Value clarity assessment overestimates viewer comprehension?
- Timing satisfaction ignores individual variation in payoff preference?
- Value magnitude assumes viewer needs match content value proposition?

**Dimension 4 (Shareability/Saveability) Challenges:**
- Social currency potential overestimates audience sharing motivations?
- Conversation starter value assumes topic is socially acceptable to discuss?
- Save utility overestimates rewatch value for一次性 content?
- Emotional resonance assumes homogenous audience emotional response?

**Dimension 5 (Platform-Fit) Challenges:**
- Format optimization assumes ideal vertical framing in production?
- Algorithm optimization based on current or outdated algorithm signals?
- Length optimization fails to account for niche-specific optimal durations?
- Native styling assumes consistent aesthetic across full 60s?

**Dimension 6 (CTA Clarity) Challenges:**
- CTA presence scoring assumes CTA won't be edited out in production?
- CTA clarity overestimates audience comprehension of action steps?
- Actionability assessment ignores platform-specific friction?
- CTA relevance assumes CTA timing aligns with viewer decision moment?

**Score Revision Protocol:**
For each validated challenge:
1. Identify which dimension scores are affected
2. Quantify score reduction based on challenge severity
3. Recalculate overall score with revised dimensions
4. Assess whether performance classification changes
5. Note revision implications for prioritized roadmap

### 7. Audience Assumptions Challenge
Stress-test audience profile assumptions from Stage 1:

**Challenge Framework:**

**Platform Expertise Assumptions:**
- Challenge: What if audience expertise level is misidentified?
- Impact: Hook sophistication, pacing tolerance, and format expectations all misaligned
- Revision: Provide alternative strategies for multiple expertise levels

**Content Intent Assumptions:**
- Challenge: What if viewers are in different intent state than assumed?
- Impact: Value delivery timing, payoff structure, and CTA appropriateness all affected
- Revision: Design content to work across multiple intent states

**Niche Sophistication Assumptions:**
- Challenge: What if niche expertise assessment is inaccurate?
- Impact: Credibility requirements, complexity thresholds, and value expectations misaligned
- Revision: Include complexity leveling and credential signaling

**Attention Allocation Assumptions:**
- Challenge: What if attention level is lower than assumed?
- Impact: Hook immediacy, value density, and payoff pacing all too optimistic
- Revision: Strengthen early value delivery and reduce mid-content lulls

**Assumption Validation Protocol:**
```
1. Identify critical audience assumptions driving key recommendations
2. For each assumption, generate "wrong assumption" scenario
3. Assess impact magnitude if assumption is incorrect
4. Develop contingency strategies for high-impact assumption failures
5. Recommend audience validation testing when assumptions are uncertain
```

### 8. Challenge Synthesis and Revision
Compile all validated challenges and determine necessary revisions:

**Challenge Impact Classification:**

| Impact Level | Score Effect | Revision Required | Priority |
|--------------|--------------|-------------------|----------|
| **Critical** | -1.0 to -2.0 points | Immediate revision required | P0 - Fix before deployment |
| **High** | -0.5 to -1.0 points | Strong revision recommended | P1 - Fix in next iteration |
| **Medium** | -0.2 to -0.5 points | Moderate revision recommended | P2 - Address when feasible |
| **Low** | -0.1 to -0.2 points | Minor revision beneficial | P3 - Optional improvement |
| **Negligible** | < -0.1 points | Acknowledgement only | P4 - Note for future |

**Revised Score Calculation:**
```
Original Overall Score: X.XX / 5.00
Challenge Adjustments:
  - Challenge #[#]: -X.X points ([dimension])
  - Challenge #[#]: -X.X points ([dimension])
  [... additional validated challenges ...]
Revised Overall Score: X.XX / 5.00
Performance Classification: [Original] → [Revised]
```

**Revision Recommendations by Priority:**

**P0 - Critical (Fix Before Deployment):**
- [Specific revisions required for critical challenges]
- [Why these are non-negotiable for safe/effective deployment]
- [Exact changes needed to resolve critical issues]

**P1 - High (Strongly Recommended):**
- [Specific revisions for high-priority challenges]
- [Performance impact if not addressed]
- [Recommended modifications with expected improvement]

**P2 - Medium (Address When Feasible):**
- [Specific revisions for medium-priority challenges]
- [Incremental performance benefits]
- [Timeline for addressing these improvements]

### 9. Final Quality Gate Validation
Before passing to synthesis, confirm all challenge areas addressed:

**Completeness Check:**
- [ ] Originality verification completed with plagiarism assessment
- [ ] Claim safety audit performed with confidence scoring
- [ ] Platform policy compliance checked across all platforms
- [ ] CTA effectiveness evaluated with specific recommendations
- [ ] Scoring robustness challenged across all 6 dimensions
- [ ] Audience assumptions stress-tested with contingency strategies

**Validation Check:**
- [ ] Minimum 3 challenges generated and evaluated
- [ ] At least 1 challenge resulted in score revision
- [ ] All critical challenges identified with P0 priority
- [ ] Revised scores calculated and documented
- [ ] Revision recommendations prioritized by impact

**Safety Check:**
- [ ] No policy-violating content remains unflagged
- [ ] All high-risk claims identified with disclaimers
- [ ] Originality concerns addressed or acknowledged
- [ ] Production feasibility constraints noted

### 10. Structured Output Generation
```markdown
## Quality Review & Challenge Report

### Challenge Summary
**Total Challenges Generated:** X
**Validated Challenges:** X (resulting in score revisions)
**Critical Issues Identified:** X
**Overall Score Impact:** -X.X points

### Originality Verification

**Plagiarism Risk Assessment:**
- Script Uniqueness: [Low/Medium/High] — [Specific findings]
- Concept Novelty: [Low/Medium/High] — [Specific findings]
- Hook Originality: [Low/Medium/High] — [Specific findings]
- Value Proposition: [Low/Medium/High] — [Specific findings]
- Visual Uniqueness: [Low/Medium/High] — [Specific findings]

**Derivative Content Findings:**
[Specific instances of potential derivative content with source comparisons]

**Originality Enhancement Recommendations:**
[Specific recommendations for improving originality]

**Challenge Generated:**
[Challenge #1 from Section 2 with full details]

### Claim Safety Audit

**Claims Identified:** X total
- Critical Risk: X claims
- High Risk: X claims
- Medium Risk: X claims
- Low Risk: X claims
- No Risk: X claims

**Claim Confidence Scores:**
| Claim Statement | Type | Confidence (0-5) | Validation Status | Action Required |
|-----------------|------|------------------|-------------------|-----------------|
| [Claim text] | [Type] | X.X | [Validated/Unvalidated] | [Action if needed] |

**Unsafe Claim Flags:**
[Specific claims requiring removal, qualification, or attribution]

**Challenge Generated:**
[Challenge #2 from Section 3 with full details]

### Platform Policy Compliance

**Policy Risk Assessment by Platform:**
- **TikTok:** [Critical/High/Medium/Low/No Risk] — [Specific policy areas]
- **YouTube Shorts:** [Critical/High/Medium/Low/No Risk] — [Specific policy areas]
- **Instagram Reels:** [Critical/High/Medium/Low/No Risk] — [Specific policy areas]

**Specific Policy Concerns:**
[Policy-relevant content with specific platform policy citations]

**Compliance Recommendations:**
[Specific modifications needed for policy compliance]

**Challenge Generated:**
[Challenge #3 from Section 4 with full details]

### CTA Strength & Clarity Assessment

**Current CTA Analysis:**
- CTA Type: [Follow/Engagement/Conversion/Save]
- Clarity: X/5 — [Specific assessment]
- Actionability: X/5 — [Specific assessment]
- Relevance: X/5 — [Specific assessment]
- Urgency: X/5 — [Specific assessment]
- Specificity: X/5 — [Specific assessment]
- Value Exchange: X/5 — [Specific assessment]

**CTA Effectiveness Score:** X.X / 5.00

**CTA Enhancement Recommendations:**
[Specific improvements to increase CTA effectiveness]

**Challenge Generated:**
[Challenge #4 from Section 5 with full details]

### Scoring Robustness Challenge

**Dimension-Specific Challenges:**

**Dimension 1 (Hook Strength):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

**Dimension 2 (Retention Architecture):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

**Dimension 3 (Payoff & Value Delivery):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

**Dimension 4 (Shareability/Saveability):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

**Dimension 5 (Platform-Fit & Format):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

**Dimension 6 (Call-to-Action Clarity):**
- Challenge #[#]: [Specific challenge] — [Impact if valid] — [Score adjustment if validated]

### Audience Assumptions Challenge

**Critical Assumptions Identified:**
1. [Assumption #1] — [Impact if wrong] — [Contingency strategy]
2. [Assumption #2] — [Impact if wrong] — [Contingency strategy]
3. [Additional assumptions...]

### Challenge Synthesis and Score Revision

**Validated Challenges with Score Impact:**
| Challenge # | Affected Dimension | Score Reduction | Revised Score |
|-------------|---------------------|-----------------|---------------|
| #[#] | [Dimension] | -X.X | X.X/5 |
| #[#] | [Dimension] | -X.X | X.X/5 |

**Score Revision Summary:**
```
Original Overall Score: X.XX / 5.00
Total Challenge Adjustments: -X.XX points
Revised Overall Score: X.XX / 5.00
Performance Classification: [Original] → [Revised]
Platform Percentile: [Original] → [Revised]
```

### Revision Recommendations by Priority

**P0 - Critical (Fix Before Deployment):**
1. [Issue] — [Why critical] — [Exact change needed] — [Expected impact]
2. [Additional critical issues...]

**P1 - High (Strongly Recommended):**
1. [Issue] — [Performance impact] — [Recommended modification] — [Expected improvement]
2. [Additional high-priority issues...]

**P2 - Medium (Address When Feasible):**
1. [Issue] — [Incremental benefits] — [Timeline recommendation]
2. [Additional medium-priority issues...]

**P3 - Low (Optional Improvement):**
1. [Issue] — [Minor benefits] — [Future consideration]
2. [Additional low-priority issues...]

### Integration Notes for Final Synthesis
- [How challenge findings should inform final deliverable]
- [Which recommendations should be prioritized in roadmap]
- [Any caveats or disclaimers needed in final report]
- [Confidence level in revised scores and recommendations]

### Research Sources
1. [Source] — [Evidence Tier] — [Policy/Claim/CTA validation]
2. [Additional sources...]

### Fallback Mode Label
[If research unavailable, explicit degradation label]
```

## Outputs
- **Primary:** Comprehensive challenge report with all 6 challenge areas addressed
- **Secondary:** Validated challenges with score revisions and impact assessment
- **Tertiary:** Prioritized revision recommendations by impact and urgency
- **Quaternary:** Integration notes for final synthesis stage

## Quality Gate
**ALL conditions must be TRUE before passing to synthesis:**

- [ ] Minimum 3 challenges generated across different categories
- [ ] At least 1 challenge resulted in measurable score revision
- [ ] All critical challenges (P0) identified with specific fix recommendations
- [ ] Originality verification completed with specific findings
- [ ] Claim safety audit performed with confidence scoring for all claims
- [ ] Platform policy compliance checked with risk classification
- [ ] CTA analysis completed with specific enhancement recommendations
- [ ] Revised scores calculated with full impact documentation
- [ ] Revision recommendations prioritized by P0-P3 framework
- [ ] Research validation includes minimum 2 sources or explicit fallback

## Failure Modes and Recovery

**Challenge Generation Failure Recovery:**
If unable to generate substantive challenges:
1. Review prior stages for overlooked assumptions or weaknesses
2. Apply standard challenge templates for each category
3. Consider whether analysis is genuinely robust or confirmation bias present
4. Flag low challenge count as potential quality concern

**Over-Challenging Recovery:**
If too many challenges generated (analysis paralysis):
1. Prioritize challenges by impact magnitude and likelihood
2. Focus on challenges with measurable score impact (>0.2 points)
3. Consolidate related challenges into broader challenge categories
4. Maintain minimum 3 challenges while avoiding excessive challenges

**Research Tool Failure Recovery:**
If WebSearch/WebFetch unavailable for validation:
1. Rely on established policy and claim evaluation frameworks
2. Apply conservative standards (assume higher risk when uncertain)
3. Explicitly label degraded mode with increased uncertainty
4. Recommend additional validation when research tools available

## Framework Application Notes

**Devil's-Advocate Role:**
This stage intentionally assumes content will fail and seeks evidence to support that assumption. Only by surviving this aggressive challenge phase can the analysis be considered robust enough for real-world deployment.

**Evidence Hierarchy in Claims:**
- Systematic Reviews > Meta-Analyses > RCTs > Cohort Studies > Expert Opinion > Blog/Anecdotal
- Lower-tier evidence requires stronger disclaimers and conservative scoring

**Platform Policy Precaution:**
When in doubt about policy compliance, assume stricter interpretation. Platform penalties are asymmetric: false positives are rare, but false negatives can destroy accounts.

**Originality Standard:**
Perfect originality is impossible and unnecessary. The goal is meaningful differentiation, not complete novelty. Focus on unique value proposition rather than avoiding all similarities.

## Tools Required
- **Read:** Ingest all prior stage outputs and user's script
- **WebSearch:** Validate claims, check platform policies, research best practices
- **WebFetch:** Retrieve detailed policy documentation and claim sources
- **Write:** Generate comprehensive quality review and challenge report
