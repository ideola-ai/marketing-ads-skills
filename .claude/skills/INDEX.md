# Marketing OS - Skills Index

Complete reference for all Marketing OS skills and their relationships.

## Workflow Overview

```
brand-voice → content-brief → content-planning → content-creation
                                          ↓
                                        marketing-campaign
                                          ↓
                                          ads-audit
```

## Skills

| # | Skill | Command | Input From | Output To | Description |
|---|-------|---------|------------|-----------|-------------|
| 1 | [brand-voice](./brand-voice/SKILL.md) | `/brand-voice` | User input | All skills | Define brand voice, style guide, and messaging pillars |
| 2 | [content-brief](./content-brief/SKILL.md) | `/brief` | brand-voice, user | content-planning, marketing-campaign | Create social media content brief with research-backed strategy |
| 3 | [content-planning](./content-planning/SKILL.md) | `/content-plan` | brand-voice, content-brief | content-creation | Plan content calendar & organize tasks in ClickUp |
| 4 | [content-creation](./content-creation/SKILL.md) | `/content-create` | brand-voice, content-brief, content-planning | Direct use, ads-audit | Create social media content assets with copy and visual direction |
| 5 | [marketing-campaign](./marketing-campaign/SKILL.md) | `/campaign` | brand-voice, content-brief | ads-audit | Plan comprehensive ad campaign with strategy, angles, and creative briefs |
| 6 | [ads-audit](./ads/SKILL.md) | `/ads audit` | marketing-campaign, content-creation | Optimization loop | Audit ad performance across all platforms |

## Quick Reference

### For New Brands
```
1. /brand-voice     (one-time setup)
2. /brief           (per campaign)
3. /content-plan    (per campaign)
4. /content-create  (per content asset)
```

### For Paid Campaigns
```
1. /brand-voice     (one-time setup)
2. /brief           (per campaign)
3. /campaign        (per campaign)
4. /ads audit       (ongoing optimization)
```

### For Ads Audit Only
```
/ads audit          (standalone - no brief needed)
/ads meta           (Meta Ads only)
/ads google         (Google Ads only)
```

## File Structure

```
.claude/skills/
├── INDEX.md                  # This file
├── brand-voice/
│   └── SKILL.md
├── content-brief/
│   └── SKILL.md
├── content-planning/
│   └── SKILL.md
├── content-creation/
│   ├── SKILL.md
│   └── rules/
│       ├── formats.md
│       ├── copywriting.md
│       ├── visuals.md
│       └── platforms/
│           ├── instagram.md
│           ├── tiktok.md
│           ├── linkedin.md
│           └── twitter.md
├── marketing-campaign/
│   ├── SKILL.md
│   └── rules/
│       ├── architecture.md
│       ├── audience.md
│       ├── creative.md
│       ├── testing.md
│       └── measurement.md
└── ads/
    ├── SKILL.md
    ├── rules/
    │   ├── workflow.md
    │   ├── diagnosis.md
    │   └── priority.md
    └── references/
        ├── benchmarks.md
        ├── testing.md
        ├── checklist.md
        ├── google.md
        ├── meta.md
        ├── youtube.md
        ├── linkedin.md
        ├── tiktok.md
        ├── microsoft.md
        ├── creative.md
        ├── landing.md
        └── budget.md
```

## Commands Summary

| Command | Trigger Words |
|---------|---------------|
| `/brand-voice` | "brand voice", "style guide", "brand guidelines", "define brand voice" |
| `/brief` | "buat brief", "brief social media", "content strategy", "research konten" |
| `/content-plan` | "content plan", "jadwal konten", "content calendar" |
| `/content-create` | "buat konten", "content create", "buat caption" |
| `/campaign` | "campaign planning", "ads strategy", "iklan" |
| `/ads audit` | "audit ads", "ad review", "performance audit", "why are my ads underperforming" |
| `/ads google` | "google ads audit", "audit google ads" |
| `/ads meta` | "meta ads audit", "facebook ads audit", "instagram ads audit" |
| `/ads youtube` | "youtube ads audit" |
| `/ads tiktok` | "tiktok ads audit" |
| `/ads linkedin` | "linkedin ads audit" |
| `/ads microsoft` | "bing ads audit", "microsoft ads audit" |
| `/ads creative` | "creative audit", "ad creative review" |
| `/ads landing` | "landing page audit", "lp audit" |
| `/ads budget` | "budget audit", "bidding strategy review" |
