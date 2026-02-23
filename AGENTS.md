# Marketing OS - Agent Architecture

## Overview

Sistem AI agent terintegrasi untuk marketing workflow - dari research brief, content planning, asset creation, sampai campaign planning. Setiap agent independen tapi saling terhubung melalui output yang menjadi input bagi agent lain.

Open-source system yang dapat digunakan oleh agency, marketing team, atau content creator mana pun.

## Workflow

```
brief → content-plan → content-create
                    ↓
                  campaign
```

---

## Agents

### 1. `/brief` - Social Media Brief Research

Membuat brief konten social media yang komprehensif dengan research-backed strategy.

**Trigger:** `/brief`, "buat brief", "brief social media", "content strategy"

**Input:**
- Brand/product info
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

**Skills:** `brief`

**Tools:**
- Web search (optional - untuk competitive research)

---

### 2. `/content-plan` - Content Calendar & Task Planning

Membuat jadwal konten dan mengorganisir task di ClickUp berdasarkan brief yang sudah dibuat.

**Trigger:** `/content-plan`, "content plan", "jadwal konten", "content calendar"

**Input:**
- Output dari `/brief` (audience, angles, platforms)
- Durasi campaign (1 minggu, 1 bulan, dll)
- Posting frequency target

**Output:**
- Weekly content structure
- Content pillars (3-5)
- Content queue table
- ClickUp tasks (auto-created via MCP)

**Skills:** `content-plan`

**Tools:**
- ClickUp MCP - untuk create tasks, lists, folders

---

### 3. `/content-create` - Content Creation Assistant

Membuat aset konten social media siap pakai dengan copy dan visual direction.

**Trigger:** `/content-create`, "buat konten", "content creation", "buat caption"

**Input:**
- Output dari `/content-plan` (content queue spesifik)
- Format yang dibutuhkan (static post, carousel, video, thread)

**Output:**
- Copy/Script siap pakai
- Visual direction untuk designer
- Metadata (hashtags, alt text, CTA)

**Skills:** `content-create`

**Tools:**
- Image generation (optional)

---

### 4. `/campaign` - Ad Campaign Planning

Merancang kampanye iklan komprehensif dengan strategi, angles, dan creative briefs.

**Trigger:** `/campaign`, "campaign planning", "ads strategy", "iklan"

**Input:**
- Output dari `/brief` (audience, angles)
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

**Skills:** `campaign`

**Tools:**
- Web search (optional - untuk competitor ads research)

---

## Usage Example

### Complete Workflow

```bash
# Step 1: Buat brief
/brief

# Step 2: Plan content dengan brief tsb
/content-plan

# Step 3: Buat konten spesifik
/content-create

# Step 4: (Optional) Buat campaign strategy
/campaign
```

---

## Skills Directory

```
.claude/skills/
├── brief/                    # /brief - Social media brief research
│   └── SKILL.md
├── content-plan/             # /content-plan - Calendar + ClickUp tasks
│   └── SKILL.md
├── content-create/           # /content-create - Content asset creation
│   ├── SKILL.md
│   └── rules/
│       ├── formats.md        # Format specifications (static, carousel, video, etc.)
│       ├── copywriting.md    # Hook formulas, CTA templates, storytelling
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

---

## MCP Integration

### ClickUp MCP

Untuk auto-create tasks di ClickUp dari `/content-plan`:

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

| Skill | Status | Rules/Files | File Location |
|-------|--------|-------------|---------------|
| `brief` | ✅ Complete | SKILL.md | `.claude/skills/brief/` |
| `content-plan` | ✅ Complete | SKILL.md | `.claude/skills/content-plan/` |
| `content-create` | ✅ Complete | SKILL.md + 7 rule files | `.claude/skills/content-create/` |
| `campaign` | ✅ Complete | SKILL.md + 5 rule files | `.claude/skills/campaign/` |
