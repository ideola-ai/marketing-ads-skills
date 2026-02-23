# Marketing OS - Agent Architecture

## Overview

Sistem AI agent terintegrasi untuk marketing workflow - dari brand voice definition, social media brief, content planning, asset creation, campaign planning, sampai ads audit. Setiap agent independen tapi saling terhubung melalui output yang menjadi input bagi agent lain.

Open-source system yang dapat digunakan oleh agency, marketing team, atau content creator mana pun.

## Workflow

```
brand-voice → content-brief → content-planning → content-creation
                                          ↓
                                        marketing-campaign
                                          ↓
                                          ads-audit
```

---

## Agents

### 1. `/brand-voice` - Brand Voice Definition

Menetapkan brand voice, style guide, dan messaging pillars yang akan menjadi foundation untuk seluruh konten.

**Trigger:** `/brand-voice`, "define brand voice", "brand voice guidelines", "style guide"

**Input:**
- Brand personality and values
- Target audience
- Communication goals
- Industry context

**Output:**
- Voice attributes (3-5 key attributes)
- Tone spectrum per channel
- Style rules (grammar, formatting, punctuation)
- Terminology guidelines
- Messaging pillars

**Skills:** `brand-voice`

**Tools:**
- None (framework-based)

---

### 2. `/content-brief` - Social Media Brief Research

Membuat brief konten social media yang komprehensif dengan research-backed strategy.

**Trigger:** `/brief`, "buat brief", "brief social media", "content strategy"

**Input:**
- Brand/product info
- Brand voice output (jika sudah didefinisikan)
- Campaign objective
- Target audience
- Target platforms
- Geographic target

**Output:**
- Audience profile (demographics, psychographics, pain points)
- Platform-specific guidelines
- Content angles (3-5 variations)
- Key messages per angle
- Visual direction

**Skills:** `content-brief`

**Tools:**
- Web search (optional - untuk competitive research)

---

### 3. `/content-planning` - Content Calendar & Task Planning

Membuat jadwal konten dan mengorganisir task di ClickUp berdasarkan brief yang sudah dibuat.

**Trigger:** `/content-plan`, "content plan", "jadwal konten", "content calendar"

**Input:**
- Output dari `/content-brief` (audience, angles, platforms)
- Brand voice output (untuk tone consistency)
- Durasi campaign (1 minggu, 1 bulan, dll)
- Posting frequency target

**Output:**
- Weekly content structure
- Content pillars (3-5)
- Content queue table
- ClickUp tasks (auto-created via MCP)

**Skills:** `content-planning`

**Tools:**
- ClickUp MCP - untuk create tasks, lists, folders

---

### 4. `/content-creation` - Content Creation Assistant

Membuat aset konten social media siap pakai dengan copy dan visual direction.

**Trigger:** `/content-create`, "buat konten", "content creation", "buat caption"

**Input:**
- Output dari `/content-planning` (content queue spesifik)
- Brand voice output (untuk tone consistency)
- Format yang dibutuhkan (static post, carousel, video, thread)

**Output:**
- Copy/Script siap pakai
- Visual direction untuk designer
- Metadata (hashtags, alt text, CTA)

**Skills:** `content-creation`

**Tools:**
- Image generation (optional)

---

### 5. `/campaign` - Ad Campaign Planning

Merancang kampanye iklan komprehensif dengan strategi, angles, dan creative briefs.

**Trigger:** `/campaign`, "campaign planning", "ads strategy", "iklan"

**Input:**
- Output dari `/content-brief` (audience, angles)
- Brand voice output (untuk messaging consistency)
- Budget target
- Campaign objective

**Output:**
- Campaign architecture
- Audience segmentation
- Messaging strategy
- Creative angles (5-7)
- Ad specifications by platform
- Campaign calendar
- Testing framework
- Measurement plan

**Skills:** `marketing-campaign`

**Tools:**
- Web search (optional - untuk competitor ads research)

---

### 6. `/ads-audit` - Ads Performance Audit

Melakukan audit komprehensif terhadap performa iklan di berbagai platform.

**Trigger:** `/ads audit`, `/ads google`, `/ads meta`, `/ads youtube`, `/ads tiktok`, `/ads linkedin`, `/ads creative`, `/ads landing`, "audit ads", "ad review", "performance audit"

**Input:**
- Campaign data dari platform ads
- Performance metrics
- Creative assets
- Landing page URL (jika ada)

**Output:**
- Performance vs benchmarks comparison
- Issues identification (critical, moderate, low)
- Prioritized action items
- A/B test recommendations
- Optimization roadmap

**Skills:** `ads`

**Tools:**
- Platform-specific references
- Benchmark data

---

## Usage Example

### Complete Workflow

```bash
# Step 1: Define brand voice (one-time setup)
/brand-voice

# Step 2: Buat brief untuk campaign spesifik
/brief

# Step 3: Plan content dengan brief tsb
/content-plan

# Step 4: Buat konten spesifik
/content-create

# Step 5: Buat campaign strategy
/campaign

# Step 6: Audit dan optimasi ads
/ads audit
```

### Shortcuts

```bash
# Langsung ke brief jika brand voice sudah ada
/brief

# Langsung ke content creation jika plan sudah ada
/content-create

# Langsung audit ads tanpa planning
/ads meta
```

---

## Skills Directory

```
.claude/skills/
├── brand-voice/              # /brand-voice - Brand voice & style guide
│   └── SKILL.md
├── content-brief/            # /brief - Social media brief research
│   └── SKILL.md
├── content-planning/         # /content-plan - Calendar + ClickUp tasks
│   └── SKILL.md
├── content-creation/         # /content-create - Content asset creation
│   ├── SKILL.md
│   └── rules/
│       ├── formats.md        # Format specifications
│       ├── copywriting.md    # Hook formulas, CTA templates
│       ├── visuals.md        # Visual direction guidelines
│       └── platforms/
│           ├── instagram.md
│           ├── tiktok.md
│           ├── linkedin.md
│           └── twitter.md
├── marketing-campaign/       # /campaign - Ad campaign planning
│   ├── SKILL.md
│   └── rules/
│       ├── architecture.md   # Campaign structure
│       ├── audience.md       # Targeting strategies
│       ├── creative.md       # Ad creative frameworks
│       ├── testing.md        # A/B testing strategies
│       └── measurement.md    # KPI and analytics
└── ads/                      # /ads* - Ads audit system
    ├── SKILL.md
    ├── rules/
    │   ├── workflow.md       # Audit workflow
    │   ├── diagnosis.md      # Issue diagnosis
    │   └── priority.md       # Prioritization framework
    └── references/
        ├── benchmarks.md     # KPI benchmarks
        ├── testing.md        # A/B testing
        ├── checklist.md      # Audit checklist
        ├── google.md         # Google Ads guide
        ├── meta.md           # Meta Ads guide
        ├── youtube.md        # YouTube Ads guide
        ├── linkedin.md       # LinkedIn Ads guide
        ├── tiktok.md         # TikTok Ads guide
        ├── microsoft.md      # Microsoft Ads guide
        ├── creative.md       # Creative audit
        ├── landing.md        # Landing page audit
        └── budget.md         # Budget & bidding
```

---

## MCP Integration

### ClickUp MCP

Untuk auto-create tasks di ClickUp dari `/content-planning`:

```json
{
  "mcpServers": {
    "clickup": {
      "command": "npx",
      "args": ["@composible/composible-mcp-clickup"]
    }
  }
}
```

---

## Status

| Skill | Command | Status | Rules/Files | File Location |
|-------|---------|--------|-------------|---------------|
| `brand-voice` | `/brand-voice` | ✅ Complete | SKILL.md | `.claude/skills/brand-voice/` |
| `content-brief` | `/brief` | ✅ Complete | SKILL.md | `.claude/skills/content-brief/` |
| `content-planning` | `/content-plan` | ✅ Complete | SKILL.md | `.claude/skills/content-planning/` |
| `content-creation` | `/content-create` | ✅ Complete | SKILL.md + 7 rule files | `.claude/skills/content-creation/` |
| `marketing-campaign` | `/campaign` | ✅ Complete | SKILL.md + 5 rule files | `.claude/skills/marketing-campaign/` |
| `ads` | `/ads*` | ✅ Complete | SKILL.md + 13 reference files | `.claude/skills/ads/` |

---

## Workflow Relationships

```
┌─────────────┐
│ brand-voice │ ───────┐
└─────────────┘        │
                       │
                       ▼
┌─────────────┐     ┌──────────────┐
│             │     │content-brief │ ──────┐
│   (Direct)  │     └──────────────┘       │
│             │                            │
└─────────────┘                            │
       │                                   │
       │        ┌───────────────────┐      │
       └───────▶│ content-planning  │◀─────┘
                 └───────────────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ content-creation │
                 └──────────────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │marketing-campaign│
                 └──────────────────┘
                          │
                          ▼
                    ┌─────────┐
                    │ads-audit│
                    └─────────┘
```

**Key:**
- Solid arrows: Primary workflow (output becomes input)
- `brand-voice` feeds into all downstream skills for consistency
- `content-brief` is the primary input for `content-planning` and `marketing-campaign`
- `content-creation` uses output from `content-planning`
- `marketing-campaign` can be accessed independently or after brief
- `ads-audit` is independent but uses campaign data as input
