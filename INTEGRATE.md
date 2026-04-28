# Bexa — Integration Guide

Get up and running in under 2 minutes with any AI coding agent.
Open your terminal, `cd` into your project folder, and run the command for your OS.

---

## Quick Install

### macOS / Linux (Terminal)

```bash
# Core skill — works for any web project
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md

# Dashboard / admin panel
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-dashboard/SKILL.md

# React Native / Expo mobile
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-mobile/SKILL.md

# Cinematic motion — GSAP, Three.js, Framer
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-motion/SKILL.md
```

### Windows (PowerShell)

```powershell
# Core skill — works for any web project
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md" -OutFile "SKILL.md"

# Dashboard / admin panel
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-dashboard/SKILL.md" -OutFile "SKILL.md"

# React Native / Expo mobile
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-mobile/SKILL.md" -OutFile "SKILL.md"

# Cinematic motion — GSAP, Three.js, Framer
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-motion/SKILL.md" -OutFile "SKILL.md"
```

> **Windows tip:** Open PowerShell inside your project folder by holding `Shift` + right-clicking the folder → *"Open PowerShell window here"*

---

## Method 1 — Drop the File (Works Everywhere)

Copy the `SKILL.md` you need into your project root. That's it.

```
your-project/
├── SKILL.md          ← drop it here
├── src/
├── package.json
└── ...
```

For multiple skills, stack them in your root:
```
SKILL.md              ← forge (core, always first)
SKILL-MOTION.md       ← forge-motion (add-on)
SKILL-DASHBOARD.md    ← forge-dashboard (add-on)
```

---

## Method 2 — Agent-Specific Setup

### Cursor

Drop `SKILL.md` in project root — auto-detected.

Global (applies to all projects):
```
~/.cursor/rules/SKILL.md
```

### Claude Code

```bash
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md
```

Or append to an existing `CLAUDE.md`:
```bash
curl https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md >> CLAUDE.md
```

### Windsurf

Drop `SKILL.md` in project root — auto-detected.

Global rules: Settings → AI → Rules → paste content.

### GitHub Copilot (VS Code)

```bash
mkdir -p .github
curl -o .github/copilot-instructions.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md
```

### Aider

```bash
aider --read SKILL.md
```

Or inline:
```bash
curl -s https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md | aider --read /dev/stdin
```

### ChatGPT / OpenAI Codex

Paste the raw file content at the top of your conversation, then give your task.

---

## Method 3 — System Prompt (API / Custom Agents)

```python
import anthropic, httpx

skill_url = "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md"
skill = httpx.get(skill_url).text

client = anthropic.Anthropic()
response = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=8096,
    system=skill,
    messages=[{"role": "user", "content": "Build me a SaaS landing page"}]
)
```

```js
// OpenAI Node.js
const skill = await fetch(
  "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md"
).then(r => r.text());

const response = await openai.chat.completions.create({
  model: "gpt-4o",
  messages: [
    { role: "system", content: skill },
    { role: "user",   content: "Build me a SaaS landing page" }
  ]
});
```

---

## Which Skill to Use

| Building | Use |
|---|---|
| Any web project | `forge` |
| Marketing / landing page | `forge` + `forge-motion` |
| Admin panel / SaaS dashboard | `forge-dashboard` |
| React Native / Expo app | `forge-mobile` |
| Scroll-storytelling / cinematic site | `forge` + `forge-motion` |
| Live data dashboard with animation | `forge-dashboard` + `forge-motion` |

---

## Dial Overrides (In Your Prompt)

Never edit the SKILL.md file. Just say it in plain language:

| Say this | Effect |
|---|---|
| "keep it clean and minimal" | SPATIAL_TENSION drops → more whitespace |
| "make it cinematic / animated" | MOTION_DEPTH rises → springs, scroll effects |
| "editorial / asymmetric style" | STRUCTURE_CHAOS rises → offset layouts |
| "no animations, CSS only" | MOTION_DEPTH = 2 |
| "data-dense / cockpit mode" | SPATIAL_TENSION rises → tight, packed UI |
| "symmetric, centered layout" | STRUCTURE_CHAOS = 2 |

---

## Verify It's Working

After your first generation, check:

- [ ] Font is NOT Inter/Roboto/Open Sans as the display font
- [ ] No centered hero + centered H1 (at default dials)
- [ ] Colors are `hsl()` tokens defined in `:root`, not hardcoded hex
- [ ] Full-height sections use `min-h-[100dvh]` — not `h-screen`
- [ ] Buttons have hover AND active/press states
- [ ] Loading state is a shimmer skeleton matching the layout shape
- [ ] Dark mode is implemented

---

## Troubleshooting

**Agent ignores the skill?**
Start your prompt with: `"Follow the Bexa design skill rules in SKILL.md strictly. Now build me..."`

**Too many animations?**
Add to your prompt: `"MOTION_DEPTH: 2"` or `"no animations, CSS transitions only"`

**Layout too complex?**
Add to your prompt: `"STRUCTURE_CHAOS: 2, keep it symmetric and centered"`

**Tailwind version conflict?**
Add to your prompt: `"We are using Tailwind v3"` or `"Tailwind v4"`

**Want to stack two skills?**
Name them `SKILL.md` and `SKILL-MOTION.md` (or any name). Most agents read all `SKILL*.md` files in root.
