# Short-form Video Script Builder (YouTube/TikTok/Reels)

<div align="center">

**A Production-Grade AI Skill for Optimizing Short-Form Video Content**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Production Ready](https://img.shields.io/badge/Status-Production--Ready-green.svg)](https://github.com/dungnotnull/shortform-video-script-builder-agent-skill)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-purple.svg)](https://claude.com/claude-code)

**Idea #69** • **Cluster:** Marketing, Content & Branding

*Engineers scripts for hook strength, retention curve, payoff and shareability, then scores them against proven creative frameworks.*

</div>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Skill Components](#skill-components)
- [Frameworks & Methodologies](#frameworks--methodologies)
- [Testing](#testing)
- [Knowledge Pipeline](#knowledge-pipeline)
- [Cluster Integration](#cluster-integration)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The **Short-form Video Script Builder** is a sophisticated AI skill designed for content creators, marketers, and strategists who need to optimize short-form video content for YouTube Shorts, TikTok, and Instagram Reels. It uses a research-first, evidence-based approach to analyze scripts, score them across six critical dimensions, and provide prioritized improvement roadmaps.

### What It Does

- Analyzes video scripts against proven creative frameworks
- Scores content across six dimensions: hook strength, retention architecture, payoff delivery, shareability, platform fit, and CTA clarity
- Generates prioritized improvement roadmaps with impact/effort ratings
- Validates claims and ensures platform policy compliance
- Provides research-backed recommendations with evidence citations

### Who It's For

- Content creators seeking to improve video performance
- Marketing professionals optimizing social media content
- Strategists analyzing competitor content
- Agencies producing client video campaigns
- Researchers studying short-form video effectiveness

---

## Features

### Core Capabilities

- **Research-First Analysis**: All recommendations backed by citable frameworks and evidence
- **6-Dimension Scoring System**: Comprehensive evaluation across critical success factors
- **Platform-Specific Optimization**: Tailored analysis for TikTok, YouTube Shorts, Instagram Reels
- **Hook Engineering**: Generate and score multiple hook options using proven templates
- **Retention Prediction**: Second-by-second retention curve analysis
- **Quality Gates**: Mandatory validation before any output delivery
- **Challenge Phase**: Devil's-advocate review to prevent overconfidence
- **Graceful Degradation**: Functions even when research tools unavailable

### Advanced Features

- **Audience Profiling**: 4-dimensional analysis of target viewers
- **Framework Application**: 7 named methodologies systematically applied
- **Evidence Hierarchy**: 6-tier evidence grading for all claims
- **Policy Compliance**: Platform content policy verification
- **Originality Verification**: Plagiarism and derivative content detection
- **CTA Optimization**: Call-to-action effectiveness analysis
- **Roadmap Generation**: Prioritized recommendations with impact/effort ratings

---

## Architecture

### System Overview

The skill uses a 6-stage harness workflow:

```
User Input
    ↓
[Stage 1] Audience Analysis → Platform psychology, 4D profiling
    ↓
[Stage 2] Hook Engineering → Hook generation, 3-Second Rule scoring
    ↓
[Stage 3] Research → WebSearch/WebFetch evidence gathering
    ↓
[Stage 4] Retention Scoring → 6-dimension analysis, retention curve
    ↓
[Stage 5] Quality Review → Challenge phase, validation
    ↓
[Stage 6] Synthesis → Final report with prioritized roadmap
```

### Quality Enforcement

Each stage includes mandatory quality gates that must pass before advancing. The skill refuses to emit output if any gate fails, ensuring all analysis meets professional standards.

---

## Installation

### Prerequisites

- Python 3.8 or higher
- Claude Code (for skill integration)
- Git (for version control)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/dungnotnull/shortform-video-script-builder-agent-skill.git
cd shortform-video-script-builder-agent-skill
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Verify installation:
```bash
python -c "import skills; print('Skill ready')"
```

### Claude Code Integration

For Claude Code integration, place the skill directory in your local skills folder:

```bash
# Copy to your Claude skills directory
cp -r . ~/.claude/skills/shortform-video-script-builder
```

---

## Usage

### Basic Usage

Invoke the skill with a video script or content concept:

```
"Evaluate my short-form video script for TikTok about creator growth tips"

"Score this YouTube Shorts script against retention best practices"

"Analyze this Instagram Reel concept and provide improvement roadmap"
```

### Advanced Usage

**Hook-Specific Analysis:**
```
"Generate and score 5 hooks for my TikTok video about fitness tips"
```

**Retention Analysis:**
```
"Map my script to a second-by-second retention curve and score it"
```

**Platform Comparison:**
```
"Analyze how this script would perform on TikTok vs YouTube Shorts"
```

**Roadmap-Only Output:**
```
"Just give me the prioritized improvement roadmap, skip the full analysis"
```

### Input Requirements

For best results, provide:

1. **Platform**: TikTok, YouTube Shorts, or Instagram Reels
2. **Script**: Full script with timing/visual cues
3. **Target Audience**: Who you're trying to reach
4. **Goals**: What you want viewers to do (follow, comment, save, etc.)

---

## Skill Components

### Main Harness

The orchestrator that coordinates all sub-skills through a 6-stage workflow.

**Location:** `skills/main.md`

### Sub-Skills

#### 1. Audience Analysis (`sub-audience-analysis.md`)

Profiles target viewers across platform psychology, expertise level, content intent, niche sophistication, and attention allocation.

**Key Outputs:**
- 4-dimensional audience profile
- Platform psychology mapping
- Hook-pacing recommendations
- Integration notes for hook engineering

#### 2. Hook Engineer (`sub-hook-engineer.md`)

Generates and scores opening hooks against the 3-Second Hook Rule, curiosity gap theory, and pattern-interrupt principles.

**Key Outputs:**
- 6+ hook options with detailed scoring
- 3-Second Rule analysis (5 sub-dimensions)
- Curiosity gap evaluation
- Pattern interrupt assessment
- Framework lock and dimension weights

#### 3. Retention Scorer (`sub-retention-scorer.md`)

Maps scripts to second-by-second retention curves and scores against the Hook-Retention-Payoff (HRP) model.

**Key Outputs:**
- Predicted retention curve with platform benchmarks
- 6-dimension scoring with sub-dimension analysis
- Composite score calculation
- Performance classification (percentile ranking)
- Strengths/weaknesses analysis

#### 4. Quality Reviewer (`sub-quality-reviewer.md`)

Devil's-advocate pass checking originality, claim safety, platform policy fit, and CTA strength.

**Key Outputs:**
- Originality verification report
- Claim safety audit with confidence scoring
- Platform policy compliance assessment
- CTA effectiveness evaluation
- Score revisions based on validated challenges
- Prioritized fix recommendations

---

## Frameworks & Methodologies

The skill systematically applies 7 world-renowned frameworks:

| Framework | Application | Evidence Base |
|-----------|-------------|---------------|
| **Hook-Retention-Payoff (HRP) Model** | Core methodology for scoring retention | Attention research, platform analytics |
| **AIDA (Attention-Interest-Desire-Action)** | Content flow and value delivery | Classic marketing framework |
| **StoryBrand SB7** | Narrative structure and storytelling | Brand storytelling research |
| **Open Loops / Curiosity Gap Theory** | Hook effectiveness and retention | Information gap psychology |
| **3-Second Hook Rule** | Initial attention capture | Platform attention research |
| **Pattern Interrupt Theory** | Breaking scroll patterns | Cognitive attention studies |
| **Platform Retention Analytics** | Benchmarking and optimization | Platform official data |

### Scoring Dimensions

Each video is scored across six dimensions (0-5 scale):

1. **Hook Strength (First 3s)** - Pattern interrupt, value signal, audio-visual sync
2. **Retention Architecture** - Pattern breaks, value distribution, transitions
3. **Payoff & Value Delivery** - Hook alignment, clarity, timing, magnitude
4. **Shareability/Saveability** - Social currency, conversation value, save utility
5. **Platform-Fit & Format** - Format optimization, native styling, algorithm fit
6. **Call-to-Action Clarity** - Presence, clarity, actionability, relevance

---

## Testing

### Test Scenarios

Comprehensive test suite with 5 detailed scenarios:

**Location:** `tests/test-scenarios.md`

1. **Happy Path** - Full script evaluation with detailed expected outputs
2. **Ambiguous Input** - Intake clarification path validation
3. **Offline Mode** - Graceful degradation when research unavailable
4. **Challenge Phase** - Score revision and policy compliance
5. **Roadmap-Only** - Streamlined output validation

### Running Tests

```bash
# Manual testing - run each scenario
# Detailed expected outputs provided in test-scenarios.md
```

### Quality Assurance

- Regression checklist for consistent scoring
- Evidence tier validation for all claims
- Cross-skill integration testing
- Production readiness verification

---

## Knowledge Pipeline

### Self-Improving Knowledge Base

The skill maintains a living knowledge base updated weekly through automated crawling.

**Location:** `SECOND-KNOWLEDGE-BRAIN.md`

### Knowledge Sources

- **ArXiv Categories**: cs.HC (Human-Computer Interaction), cs.MM (Multimedia), cs.SI (Social and Information Networks)
- **Platform Official**: YouTube Creator Academy, TikTok Creative Center, Meta for Creators
- **Research**: Think with Google video research, attention studies

### Update Tool

**Location:** `tools/knowledge_updater.py`

Automated knowledge pipeline with:
- ArXiv API integration
- WebSearch integration structure
- Entry scoring algorithms
- Deduplication logic
- Production-grade error handling
- Logging and monitoring

### Running Updates

```bash
# Manual knowledge update
python tools/knowledge_updater.py

# Dry run (no changes written)
python tools/knowledge_updater.py --dry-run

# Verbose output
python tools/knowledge_updater.py --verbose
```

---

## Cluster Integration

### Marketing, Content & Branding Cluster

This skill is part of a larger cluster of marketing-focused AI skills designed to work together.

**Location:** `docs/phase-5-cross-skill-wiring.md`

### Shared Components

The cluster shares standardized components:

- **shared-audience-analysis** - Universal audience profiling
- **shared-research-validator** - Evidence grading and citation
- **shared-quality-reviewer** - Challenge-phase validation
- **shared-roadmap-generator** - Prioritized recommendation synthesis

### Future Cluster Skills

Planned integration with:
- Content Strategy Planner
- Social Media Campaign Architect
- Brand Voice Designer
- Audience Persona Builder
- Marketing Analytics Interpreter

### Integration Patterns

Three defined patterns for skill coordination:
- Sequential Pipeline (stage-by-stage processing)
- Parallel Analysis (simultaneous multi-track)
- Iterative Refinement (improvement cycles)

---

## Development

### Project Status

All 5 development phases complete:

- Phase 0: Research & Architecture
- Phase 1: Core Sub-Skills
- Phase 2: Main Harness + Quality Gates
- Phase 3: Knowledge Pipeline
- Phase 4: Testing & Validation
- Phase 5: Integration & Cross-Skill Wiring

**Location:** `PROJECT-DEVELOPMENT-PHASE-TRACKING.md`

### Code Quality

- Production-grade implementation
- Comprehensive documentation
- Zero technical debt
- Professional error handling
- Extensive logging and monitoring

### File Structure

```
shortform-video-script-builder/
├── README.md                          # This file
├── CLAUDE.md                          # Project instructions
├── PROJECT-detail.md                  # Technical specification
├── PROJECT-DEVELOPMENT-PHASE-TRACKING.md  # Development progress
├── COMPLETION-SUMMARY.md              # Final verification
├── SECOND-KNOWLEDGE-BRAIN.md          # Knowledge base
├── skills/                            # Skill implementations
│   ├── main.md                        # Main harness
│   ├── sub-audience-analysis.md       # Audience profiling
│   ├── sub-hook-engineer.md           # Hook generation
│   ├── sub-retention-scorer.md        # Retention scoring
│   └── sub-quality-reviewer.md        # Quality review
├── tools/                             # Supporting tools
│   └── knowledge_updater.py           # Knowledge pipeline
├── tests/                             # Test suite
│   └── test-scenarios.md              # Test scenarios
└── docs/                              # Documentation
    └── phase-5-cross-skill-wiring.md  # Cluster integration
```

---

## Contributing

We welcome contributions to improve the skill!

### Contribution Areas

- Additional framework integrations
- Platform-specific optimizations
- New hook generation templates
- Enhanced test scenarios
- Documentation improvements
- Knowledge source additions

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch
3. Make your changes with comprehensive documentation
4. Test thoroughly using provided test scenarios
5. Submit a pull request with clear description

### Quality Standards

All contributions must:
- Maintain production-grade code quality
- Include comprehensive documentation
- Pass all test scenarios
- Follow existing code patterns
- Preserve evidence-based approach

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

**MIT License Summary:**
- Commercial use allowed
- Modification allowed
- Distribution allowed
- Private use allowed
- License and copyright notice required

---

## Attribution

**Developed by:** dungnotull
**Idea:** #69 in Marketing, Content & Branding cluster
**Framework:** Based on established research in attention psychology, content strategy, and platform analytics

**Key Research Areas:**
- Human-Computer Interaction (cs.HC)
- Multimedia Studies (cs.MM)
- Social and Information Networks (cs.SI)

---

## Support & Community

### Documentation

- **Technical Spec:** `PROJECT-detail.md`
- **Development Tracking:** `PROJECT-DEVELOPMENT-PHASE-TRACKING.md`
- **Test Documentation:** `tests/test-scenarios.md`
- **Cluster Integration:** `docs/phase-5-cross-skill-wiring.md`

### Issues & Questions

For bug reports, feature requests, or questions:
- Open an issue on GitHub
- Check existing documentation first
- Provide detailed context and examples

### Acknowledgments

Built with research and best practices from:
- YouTube Creator Academy
- TikTok Creative Center
- Meta for Creators
- Academic research in attention and multimedia
- The Claude Code community

---

## Quick Start

1. Clone the repo
2. Review `PROJECT-detail.md` for technical overview
3. Check `tests/test-scenarios.md` for usage examples
4. Integrate with Claude Code or use standalone
5. Run your first script analysis

**Ready to optimize your short-form video content? Start now!**

---

<div align="center">

**Built with research-first principles and production-grade standards**

[⬆ Back to Top](#short-form-video-script-builder-youtubetiktokreels)

</div>
