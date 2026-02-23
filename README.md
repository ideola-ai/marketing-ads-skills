# Marketing OS

**An AI-powered planning and production system for marketing teams and agencies.** Streamline your content strategy—from brief to scheduling to production—without starting from scratch every time.

---

## Why Marketing OS?

AI generates content fast, but the output often feels **generic** and off-target. Weak hooks. Off tone. Unclear CTAs. You spend as much time revising as creating from scratch.

**Core problem**: We ask AI to handle strategy AND production in one step. No brief. No message architecture. No shared understanding of the end goal.

**Solution**: Marketing OS guides you through a structured creative process. You + AI working together through clear steps:

---

## The Workflow

```
1. BRIEF           → Research & define content strategy
2. CONTENT PLAN    → Schedule & organize tasks in ClickUp
3. CONTENT CREATE  → Produce content assets (copy + visual)
4. CAMPAIGN        → (Optional) Plan paid ad campaigns
```

Each step is a focused conversation. AI asks, you direct—together producing content that aligns with your strategy, not random outputs.

---

## Available Skills

| Skill | Description |
|-------|-------------|
| `/brief` | Create social media content brief with research-backed strategy |
| `/content-plan` | Plan content calendar & organize tasks in ClickUp |
| `/content-create` | Create social media content assets with copy and visual direction |
| `/campaign` | Plan comprehensive ad campaign with strategy, angles, and creative briefs |

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
# Step 1: Create a brief first
/brief

# Step 2: Plan your content calendar
/content-plan

# Step 3: Create specific content
/content-create

# Step 4: (Optional) Plan paid campaign
/campaign
```

**Recommended flow**:
1. Start with `/brief` to define objectives & audience
2. Use `/content-plan` to map your schedule
3. Run `/content-create` to produce each asset
4. Use `/campaign` for paid ads if needed

---

## Created by

**Wahyu Ikbal** — AI-powered marketing workflow system

Based on [Design OS](https://buildermethods.com) by Brian Casel

---

## Support & Updates

- Check [CHANGELOG.md](CHANGELOG.md) for latest updates
- Star the repo to show support
- Open issues for bugs or feature requests
