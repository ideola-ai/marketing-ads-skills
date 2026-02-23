# Marketing OS

**An AI-powered planning and production system for marketing teams and agencies.** Streamline your content strategy—from brand voice to brief to scheduling to production to campaign to ads audit—without starting from scratch every time.

---

## Why Marketing OS?

AI generates content fast, but the output often feels **generic** and off-target. Weak hooks. Off tone. Unclear CTAs. You spend as much time revising as creating from scratch.

**Core problem**: We ask AI to handle strategy AND production in one step. No brand voice. No brief. No message architecture. No shared understanding of the end goal.

**Solution**: Marketing OS guides you through a structured creative process. You + AI working together through clear steps:

---

## The Workflow

```
1. BRAND VOICE     → Define brand voice, style guide, and messaging pillars
2. CONTENT BRIEF   → Research & define content strategy
3. CONTENT PLAN    → Schedule & organize tasks in ClickUp
4. CONTENT CREATE  → Produce content assets (copy + visual)
5. CAMPAIGN        → (Optional) Plan paid ad campaigns
6. ADS AUDIT       → (Optional) Audit and optimize ad performance
```

Each step is a focused conversation. AI asks, you direct—together producing content that aligns with your strategy, not random outputs.

---

## Available Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Brand Voice | `/brand-voice` | Define brand voice, style guide, and messaging pillars |
| Content Brief | `/brief` | Create social media content brief with research-backed strategy |
| Content Plan | `/content-plan` | Plan content calendar & organize tasks in ClickUp |
| Content Create | `/content-create` | Create social media content assets with copy and visual direction |
| Marketing Campaign | `/campaign` | Plan comprehensive ad campaign with strategy, angles, and creative briefs |
| Ads Audit | `/ads audit` | Audit ad performance across platforms (Google, Meta, TikTok, LinkedIn, YouTube, etc.) |

---

## Installation

### Option 1: Clone and Copy

Clone the repo and copy the skills folder:

```bash
git clone https://github.com/wahyudesu/marketing-os.git
cp -r marketing-os/.claude/skills/* your-project/.claude/skills/
```

### Option 2: Git Submodule

Add as a submodule for easy updates:

```bash
git submodule add https://github.com/wahyudesu/marketing-os.git .claude/marketing-os
```

Then reference skills from `.claude/marketing-os/skills/`.

### Option 3: Fork and Customize

1. Fork this repository
2. Customize skills for your agency's needs
3. Clone your fork into your projects

## How to Use

```bash
# Step 0: Define brand voice (one-time setup)
/brand-voice

# Step 1: Create a brief for your campaign
/brief

# Step 2: Plan your content calendar
/content-plan

# Step 3: Create specific content
/content-create

# Step 4: (Optional) Plan paid campaign
/campaign

# Step 5: (Optional) Audit and optimize ads
/ads audit
```

**Recommended flow**:
1. Start with `/brand-voice` to define your brand's communication style (do this once)
2. Use `/brief` to define objectives & audience for each campaign
3. Use `/content-plan` to map your schedule
4. Run `/content-create` to produce each asset
5. Use `/campaign` for paid ads if needed
6. Use `/ads audit` to optimize existing ad performance

---

## Platform-Specific Audit Commands

The ads audit system supports platform-specific commands:

| Command | Description |
|---------|-------------|
| `/ads google` | Google Ads audit (Search, PMax, Display, YouTube, Demand Gen) |
| `/ads meta` | Meta Ads audit (Facebook, Instagram, Messenger) |
| `/ads youtube` | YouTube Ads audit |
| `/ads tiktok` | TikTok Ads audit |
| `/ads linkedin` | LinkedIn Ads audit |
| `/ads microsoft` | Microsoft/Bing Ads audit |
| `/ads creative` | Cross-platform creative audit |
| `/ads landing` | Landing page quality audit |
| `/ads budget` | Budget and bidding review |

---

## Created by

**Wahyu Ikbal** — AI-powered marketing workflow system

Based on [Design OS](https://buildermethods.com) by Brian Casel

---

## Support & Updates

- Check [CHANGELOG.md](CHANGELOG.md) for latest updates
- Star the repo to show support
- Open issues for bugs or feature requests
