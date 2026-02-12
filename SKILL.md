---
name: ads-content-os
description: Complete AI agent system for social media content marketing workflow. Use when user wants to create content briefs, plan content calendars, generate social media content assets, or plan ad campaigns. Includes 4 integrated skills: brief (research-backed strategy), content-plan (calendar + ClickUp tasks), content-create (ready-to-use content), and campaign (paid media strategy).
version: 1.0.0
author: ideola
tags: [social-media, marketing, content-creation, ads, workflow]
repository: https://github.com/wahyudesu/ideola-ai-stack-3
---

# Ads Content OS - AI Agent System

Complete integrated AI agent system for content marketing workflow - from research brief, content planning, asset creation, to campaign planning.

## Overview

Ads Content OS is a collection of 4 specialized AI skills that work independently but connect through outputs that become inputs for other agents. This creates a seamless workflow from strategy to execution.

## Workflow

```
brief → content-plan → content-create
                    ↓
                  campaign
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
```

## Installation

To use these skills in your project:

```bash
# Clone the repository
git clone https://github.com/wahyudesu/ideola-ai-stack-3.git

# Copy skills to your project
cp -r ideola-ai-stack-3/.claude/skills/* your-project/.claude/skills/
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
└── campaign/                 # /campaign - Ad campaign planning
    ├── SKILL.md
    └── rules/
        ├── architecture.md   # Campaign structure frameworks
        ├── audience.md       # Targeting strategies
        ├── creative.md       # Ad creative frameworks
        ├── testing.md        # A/B testing strategies
        └── measurement.md    # KPI and analytics setup
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