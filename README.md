# Bexa — Frontend Design Skills for AI Coding Agents

<p align="center">
  <strong>Drop one file into your project. Your AI agent stops building generic UIs.</strong>
</p>

<p align="center">
  <a href="https://github.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/stargazers">
    <img src="https://img.shields.io/github/stars/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents?style=flat-square&color=0f172a" />
  </a>
  <img src="https://img.shields.io/badge/version-1.2.0-0f172a?style=flat-square" />
  <img src="https://img.shields.io/badge/license-MIT-22c55e?style=flat-square" />
  <img src="https://img.shields.io/badge/framework-agnostic-1e293b?style=flat-square" />
</p>

<p align="center">
  Cursor · Antigravity · Claude Code · Windsurf · GitHub Copilot · Codex · Aider · Amp · Cline · Gemini CLI · Warp
</p>

---

## How It Works

Bexa is a set of **design instruction files** (`SKILL.md`) that you place in your project root. Your AI coding agent reads the file automatically and follows its rules every time it writes frontend code.

**The result:** instead of producing the same centered hero, purple gradient, and Inter font it always defaults to, your agent produces a deliberate, professional, non-generic UI — with proper typography, calibrated colors, real dark mode, and physics-based animations.

No npm package. No runtime. No config. Just a Markdown file.

---

## Install

```bash
npx skills add https://github.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents
```

Works on Windows, macOS, and Linux. Requires Node.js.

<details>
<summary>Manual install — macOS / Linux</summary>

| Skill | Best For | Install |
|---|---|---|
| **bexa** | Any website, landing page, or SaaS product | [View](skills/bexa/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa/SKILL.md) |
| **bexa-landing** | Agency landing pages — brand identity, high-conversion, animated | [View](skills/bexa-landing/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-landing/SKILL.md) |
| **bexa-dashboard** | SaaS admin panels, analytics, data-dense UIs | [View](skills/bexa-dashboard/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-dashboard/SKILL.md) |
| **bexa-mobile** | React Native / Expo — native gestures & haptics | [View](skills/bexa-mobile/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-mobile/SKILL.md) |
| **bexa-motion** | Scroll-storytelling, GSAP, Three.js, Framer Motion | [View](skills/bexa-motion/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-motion/SKILL.md) |

</details>

<details>
<summary>Manual install — Windows (PowerShell)</summary>

```powershell
# Web projects
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa/SKILL.md" -OutFile "SKILL.md"

# SaaS dashboards & admin panels
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-dashboard/SKILL.md" -OutFile "SKILL.md"

# React Native & Expo apps
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-mobile/SKILL.md" -OutFile "SKILL.md"

# Cinematic animations (GSAP, Framer Motion, Three.js)
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/bexa-motion/SKILL.md" -OutFile "SKILL.md"
```

> **Tip:** `Shift` + right-click your project folder → *"Open PowerShell window here"*

</details>

---

## Which Skill Do I Need?

| I am building... | Use this skill |
|---|---|
| A website, landing page, or general product UI | **bexa** |
| An agency landing page, brand site, or high-conversion page | **bexa-landing** |
| An admin panel, dashboard, or analytics UI | **bexa-dashboard** |
| A React Native or Expo mobile app | **bexa-mobile** |
| A site with heavy animations, GSAP, or Three.js | **bexa** + **bexa-motion** |
| A conversion-focused landing page with cinematic scroll | **bexa-landing** + **bexa-motion** |

Install the skill that matches your project. If you're unsure, start with **bexa**.

---

## What Changes in Your AI's Output

### Before Bexa
- Centered hero section with a centered headline
- Three equal feature cards in a row
- Purple or blue gradient on everything
- Inter font at default weight
- `h-screen` that breaks on iOS Safari
- No dark mode
- Generic circular loading spinner
- *"Elevate your seamless next-gen workflow"*

### After Bexa
- Left-anchored or split-screen hero
- Zigzag, masonry, or asymmetric card layout
- One HSL-calibrated accent color (≤75% saturation)
- Context-matched font pairing (Geist, Satoshi, Fraunces, etc.)
- `min-h-[100dvh]` — works everywhere
- Full dark mode with proper token system
- Layout-matched shimmer skeleton
- Concrete, product-specific copy

---

## The 3 Dials

Every Bexa skill has three settings you control through your prompt — you never edit the file.

| Dial | What it controls | Example prompts |
|---|---|---|
| **SPATIAL_TENSION** | Whitespace vs. density | *"airy and minimal"* or *"data-dense, cockpit mode"* |
| **MOTION_DEPTH** | Animation complexity | *"no animations"* or *"cinematic, physics-based"* |
| **STRUCTURE_CHAOS** | Layout symmetry | *"clean, centered"* or *"asymmetric, editorial"* |

Just describe what you want. The agent adjusts automatically.

---

## Agent Setup

After running `npx skills add`, Bexa is installed for the agents you selected. If you prefer manual setup:

| Agent | What to do |
|---|---|
| Cursor, Antigravity, Windsurf, Amp, Cline, Warp | Drop `SKILL.md` in your project root |
| Claude Code | Drop `SKILL.md` in root, or append to `CLAUDE.md` |
| GitHub Copilot | Add content to `.github/copilot-instructions.md` |
| Codex / ChatGPT | Paste content at the top of your conversation |
| Aider | `aider --read SKILL.md` |
| Any LLM API | Pass as the `system` message |

Full setup guide with copy-paste commands → [INTEGRATE.md](INTEGRATE.md)

---

## FAQ

**Does it work with React, Vue, Svelte, Astro, or plain HTML?**
Yes. Bexa is framework-agnostic.

**Do I need to configure anything?**
No. Drop the file in your project root and start building.

**Will it conflict with my existing `.cursorrules` or `CLAUDE.md`?**
No. Append Bexa content to your existing file if needed.

**Can I use multiple skills at once?**
Yes. Name them `SKILL.md` and `SKILL-MOTION.md` in your root — agents read both.

---

## Roadmap

- [ ] `bexa-editorial` — Blog and long-form article design
- [ ] `bexa-brutalist` — Swiss typography, raw grid, high contrast
- [ ] `bexa-luxury` — Premium whitespace, serif display, muted palette

---

## Contributing

Every rule must override a specific, documented AI design bias.
See [CONTRIBUTING.md](CONTRIBUTING.md) · [CHANGELOG.md](CHANGELOG.md)

## License

MIT — [LICENSE](LICENSE)
