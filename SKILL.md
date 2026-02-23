---
name: marketing-os
description: Complete AI agent system for social media content marketing workflow. Use when user wants to create content briefs, plan content calendars, generate social media content assets, plan ad campaigns, or audit existing ad performance. Includes 5 integrated skills: brief (research-backed strategy), content-plan (calendar + ClickUp tasks), content-create (ready-to-use content), campaign (paid media strategy), and ads-audit (comprehensive ads audit).
version: 1.0.0
tags: [social-media, marketing, content-creation, ads, workflow, audit]
---

# Marketing OS - AI Agent System

Complete integrated AI agent system for content marketing workflow - from research brief, content planning, asset creation, campaign planning, to performance auditing.

## Overview

Marketing OS is a collection of 5 specialized AI skills that work independently but connect through outputs that become inputs for other agents. This creates a seamless workflow from strategy to execution to optimization.

## Workflow

```
brand voice → social-media-brief → content-plan → content-creation
                                          ↓
                                        campaign
                                          ↓
                                      ads-audit
```

## Included Skills

### 1. `/brief` - Social Media Brief Research

Creates comprehensive social media content briefs with research-backed strategy.

**Use when:**
- Creating content brief
- Developing social media strategy
- Researching content foundation
- "buat brief", "brief social media", "content strategy"

**Output:**
- Audience profile (demographics, psychographics, pain points)
- Platform-specific guidelines
- Content angles (3-5 variations)
- Key messages per angle
- Visual direction

### 2. `/content-plan` - Content Calendar & Task Planning

Creates content calendars and organizes tasks in ClickUp based on brief outputs.

**Use when:**
- Creating content plan
- Building content calendar
- Scheduling posts
- "content plan", "jadwal konten", "content calendar"

**Output:**
- Weekly content structure
- Content pillars (3-5)
- Content queue table
- ClickUp tasks (auto-created via MCP)

### 3. `/content-create` - Content Creation Assistant

Generates ready-to-publish social media content with copy and visual direction.

**Use when:**
- Creating content assets
- Writing captions
- Making posts
- "buat konten", "content create", "buat caption"

**Output:**
- Copy/Script ready to use
- Visual direction for designer
- Metadata (hashtags, alt text, CTA)

### 4. `/campaign` - Ad Campaign Planning

Designs comprehensive ad campaigns with strategy, angles, and creative briefs.

**Use when:**
- Creating ad campaign
- Planning paid media strategy
- "campaign planning", "ads strategy", "iklan"

**Output:**
- Campaign architecture
- Audience segmentation
- 5-7 creative angles
- Ad specifications by platform
- Testing framework
- Measurement plan

### 5. `/ads-audit` - Ads Campaign Audit

Comprehensive ad campaign audit with platform-specific analysis and optimization recommendations.

**Commands:**
- `/ads audit` - Full multi-platform audit
- `/ads google` - Google Ads analysis
- `/ads meta` - Meta Ads analysis
- `/ads youtube` - YouTube Ads analysis
- `/ads linkedin` - LinkedIn Ads analysis
- `/ads tiktok` - TikTok Ads analysis
- `/ads microsoft` - Microsoft/Bing Ads analysis
- `/ads creative` - Creative quality audit
- `/ads landing` - Landing page audit
- `/ads budget` - Budget & bidding review

**Use when:**
- Auditing existing ad campaigns
- Analyzing ad performance
- Identifying optimization opportunities
- "audit ads", "ad review", "performance audit"

**Output:**
- Performance analysis vs. benchmarks
- Issue identification (creative, targeting, budget)
- Optimization recommendations
- A/B test ideas
- Prioritized action plan

## Complete Workflow Example

```bash
# Step 1: Create brief
/brief

# Step 2: Plan content with brief output
/content-plan

# Step 3: Create specific content
/content-create

# Step 4: (Optional) Create campaign strategy
/campaign

# Step 5: Audit and optimize existing campaigns
/ads audit

# Step 6: (Optional) Platform-specific audit
/ads google | /ads meta | /ads youtube | etc.
```

## Installation

To use these skills in your project:

```bash
# Clone the repository
git clone https://github.com/wahyudesu/marketing-os.git

# Copy skills to your project
cp -r marketing-os/.claude/skills/* your-project/.claude/skills/
```

## Skill Structure

```
.claude/skills/
├── brief/                    # /brief - Social media brief research
│   └── SKILL.md
├── content-plan/             # /content-plan - Calendar + ClickUp tasks
│   └── SKILL.md
├── content-create/           # /content-create - Content asset creation
│   ├── SKILL.md
│   └── rules/
│       ├── formats.md        # Format specifications
│       ├── copywriting.md    # Hook formulas, CTA templates
│       ├── visuals.md        # Visual direction guidelines
│       └── platforms/
│           ├── instagram.md  # Instagram-specific guidelines
│           ├── tiktok.md     # TikTok-specific guidelines
│           ├── linkedin.md   # LinkedIn-specific guidelines
│           └── twitter.md    # Twitter/X-specific guidelines
├── campaign/                 # /campaign - Ad campaign planning
│   ├── SKILL.md
│   └── rules/
│       ├── architecture.md   # Campaign structure frameworks
│       ├── audience.md       # Targeting strategies
│       ├── creative.md       # Ad creative frameworks
│       ├── testing.md        # A/B testing strategies
│       └── measurement.md    # KPI and analytics setup
└── ads-audit/               # /ads-audit - Comprehensive ads audit
    ├── SKILL.md
    ├── rules/               # Workflow & diagnosis procedures (low freedom)
    │   ├── workflow.md    # Step-by-step audit process
    │   ├── diagnosis.md   # Root cause identification
    │   └── priority.md    # Prioritization framework
    └── references/          # Platform guides & data (high freedom)
        ├── benchmarks.md    # Industry KPI benchmarks
        ├── testing.md        # A/B testing frameworks
        ├── checklist.md      # Complete audit checklist
        ├── google.md        # Google Ads specific guide
        ├── meta.md          # Meta Ads specific guide
        ├── youtube.md        # YouTube Ads specific guide
        ├── linkedin.md      # LinkedIn Ads specific guide
        ├── tiktok.md        # TikTok Ads specific guide
        ├── microsoft.md      # Microsoft Ads specific guide
        ├── creative.md       # Creative audit framework
        ├── landing.md       # Landing page audit framework
        └── budget.md        # Budget & bidding framework
```

## Best Practices

1. **Start with brief** - Everything flows from audience insights
2. **Use outputs as inputs** - Each skill's output becomes input for the next
3. **Platform-native** - Adapt content for each platform's unique format
4. **Iterate quickly** - Test and refine based on performance

## Contributing

Found a way to improve a skill? Have a new skill to suggest? PRs and issues welcome!

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding or improving skills.

## License

MIT License - see LICENSE file for details
