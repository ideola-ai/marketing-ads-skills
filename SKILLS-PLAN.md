# Ads Content OS - Custom Commands

Daftar custom command yang tersedia untuk Claude Code dan integrasi dengan tools.

## Available Commands

### `/brief` - Social Media Brief Research
Membuat brief konten social media yang komprehensif dengan research-backed strategy.

**Usage:**
```
/brief
```

**Output:**
- Content strategy summary
- Target audience profile
- Platform-specific guidelines
- Content angles (3-5 variations)
- Key messages per angle
- Visual direction

---

### `/content-plan` - Content Calendar & Task Planning
Membuat jadwal konten dan mengorganisir task di ClickUp.

**Usage:**
```
/content-plan
```

**Requirements:**
- Brief harus sudah dibuat sebelumnya (idealnya dari `/brief`)
- ClickUp MCP configuration untuk auto-create tasks

**Output:**
- Weekly content structure
- Content pillars (3-5)
- Content queue table
- ClickUp tasks (jika diaktifkan)

---

### `/content-create` - Content Creation Assistant
Membuat aset konten social media siap pakai dengan copy dan visual direction.

**Usage:**
```
/content-create
```

**Supported Formats:**
- Static posts (image/graphic)
- Carousels
- Videos/Reels
- LinkedIn/Twitter threads

**Output:**
- Copy/Script siap pakai
- Visual direction
- Metadata (hashtags, alt text)

---

### `/campaign` - Ad Campaign Planning
Merancang kampanye iklan komprehensif dengan strategi, angles, dan creative briefs.

**Usage:**
```
/campaign
```

**Output:**
- Campaign architecture
- Audience segmentation
- Messaging strategy
- Creative angles (5-7)
- Ad specifications by platform
- Campaign calendar
- Testing framework
- Measurement plan

---

## Workflow Example

### Step 1: Create Brief
```
/brief
```
Jawab pertanyaan tentang brand, audience, goals, dan platform.

### Step 2: Plan Content
```
/content-plan
```
Gunakan brief dari step 1 untuk membuat calendar dan ClickUp tasks.

### Step 3: Create Content
```
/content-create
```
Buat konten spesifik berdasarkan plan yang sudah dibuat.

### Step 4: Launch Campaign (Optional)
```
/campaign
```
Untuk paid ads campaign dengan strategi lengkap.

---

## Integration dengan Tools

### ClickUp MCP
Tambahkan ke `.mcp.json`:
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

### Nano Banana / Meta Ads Tools
Tambahkan ke `.mcp.json`:
```json
{
  "mcpServers": {
    "nano-banana": {
      "command": "node",
      "args": ["/path/to/nano-banana-mcp/index.js"]
    }
  }
}
```

---

## File Structure

```
.
├── .claude/
│   └── commands/
│       ├── brief.md           # /brief command
│       ├── content-plan.md    # /content-plan command
│       ├── content-create.md  # /content-create command
│       └── campaign.md        # /campaign command
├── prompts/
│   └── (additional prompt templates)
└── COMMANDS.md                # This file
```
