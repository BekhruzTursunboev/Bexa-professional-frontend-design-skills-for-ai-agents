# Bexa — Frontend Design Skills for AI Coding Agents

<p align="center">
  <strong>The SKILL.md pack that makes AI agents stop building generic UIs.</strong><br/>
  Drop one file. Your agent becomes a Senior Design Engineer.
</p>

<p align="center">
  <a href="https://github.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/stargazers">
    <img src="https://img.shields.io/github/stars/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents?style=flat-square&color=0f172a" />
  </a>
  <img src="https://img.shields.io/badge/version-1.1.0-0f172a?style=flat-square" />
  <img src="https://img.shields.io/badge/skills-4-0f172a?style=flat-square" />
  <img src="https://img.shields.io/badge/license-MIT-22c55e?style=flat-square" />
  <img src="https://img.shields.io/badge/framework-agnostic-1e293b?style=flat-square" />
</p>

<p align="center">
  Works with · <b>Cursor</b> · <b>Antigravity</b> · <b>Claude Code</b> · <b>Windsurf</b> · <b>GitHub Copilot</b> · <b>Codex</b> · <b>Aider</b> · <b>Amp</b> · <b>Cline</b> · <b>Gemini CLI</b> · <b>Warp</b> · <b>OpenCode</b>
</p>

---

## Install

```bash
npx skills add https://github.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents
```

Works on **Windows, macOS, and Linux**. Requires Node.js.

<details>
<summary>Manual install (curl / PowerShell)</summary>

**macOS / Linux**
```bash
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md
```

**Windows (PowerShell)**
```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md" -OutFile "SKILL.md"
```

Drop `SKILL.md` into your project root. Done.

</details>

---

## What Is This

**Bexa** is a collection of `SKILL.md` instruction files for AI coding agents (Cursor, Claude Code, Windsurf, Copilot, and more). When placed in your project root, these files instruct the agent to follow a strict set of design engineering rules — overriding the generic, repetitive UI patterns that AI models produce by default.

**Without Bexa:** Your agent generates a centered hero, purple gradient, three equal feature cards, Inter font, and broken Unsplash images.

**With Bexa:** Your agent produces intentional layouts, curated font pairings, HSL-calibrated color systems, proper dark mode, animation with physics, and accessible, production-ready components.

No runtime. No config. No build step. Just a Markdown file your agent reads.

---

## Skills

| Skill | Best For | Install |
|---|---|---|
| **forge** | Any web project — the default | [View](skills/forge/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md) |
| **forge-dashboard** | SaaS admin panels, analytics, data-dense UIs | [View](skills/forge-dashboard/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-dashboard/SKILL.md) |
| **forge-mobile** | React Native / Expo — native gestures & haptics | [View](skills/forge-mobile/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-mobile/SKILL.md) |
| **forge-motion** | Scroll-storytelling, GSAP, Three.js, Framer Motion | [View](skills/forge-motion/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-motion/SKILL.md) |

**Combine skills** for advanced setups:
```bash
# Landing page with cinematic scroll
curl -o SKILL.md        .../skills/forge/SKILL.md
curl -o SKILL-MOTION.md .../skills/forge-motion/SKILL.md

# Animated SaaS dashboard
curl -o SKILL.md        .../skills/forge-dashboard/SKILL.md
curl -o SKILL-MOTION.md .../skills/forge-motion/SKILL.md
```

---

## The 3-Dial System

Every skill has three adjustable dials. You never edit the file — just describe what you want in your prompt.

```
SPATIAL_TENSION:  7   (1 = Zen whitespace  →  10 = Max editorial density)
MOTION_DEPTH:     7   (1 = CSS hover only  →  10 = GSAP + Three.js physics)
STRUCTURE_CHAOS:  6   (1 = Symmetric grid  →  10 = Organic asymmetric layout)
```

Say **"minimal"** → SPATIAL_TENSION drops. Say **"cinematic"** → MOTION_DEPTH rises. Say **"editorial"** → STRUCTURE_CHAOS rises.

---

## What Changes in Your Output

### Typography

Bexa ships a **context-specific font pairing matrix** — no more Inter at default weight.

| Project type | Display font | Body font | Code font |
|---|---|---|---|
| SaaS / Product | Geist | Geist | Geist Mono |
| Editorial / Blog | Fraunces | Plus Jakarta Sans | JetBrains Mono |
| Portfolio / Agency | Cabinet Grotesk | Outfit | Fira Code |
| Dashboard / Data | Satoshi | Inter | Geist Mono |
| Luxury / Brand | Cormorant Garamond | Jost | — |
| Developer Tool | Space Grotesk | DM Sans | JetBrains Mono |

### Color

HSL design tokens instead of hardcoded hex values. One accent. Maximum 75% saturation.

```css
:root {
  --surface-0:      hsl(0 0% 98%);
  --accent:         hsl(221 70% 52%);   /* calibrated, not AI purple */
  --accent-dim:     hsl(221 70% 52% / 0.12);
  --text-primary:   hsl(220 20% 10%);
  --border:         hsl(220 13% 91%);
}
```

### Motion

Spring physics instead of `linear`/`ease`. `useMotionValue` instead of `useState`. Proper cleanup. `prefers-reduced-motion` respected.

```jsx
// Magnetic button — outside render cycle, never useState
const x = useMotionValue(0)
const sx = useSpring(x, { stiffness: 200, damping: 20 })
```

---

## Before & After

| AI default output | With Bexa |
|---|---|
| Centered hero + centered H1 | Left-anchored or split-screen hero |
| 3 equal feature cards | Zigzag, masonry, or 70/30 asymmetric grid |
| AI purple gradient | HSL-calibrated single accent |
| Inter font everywhere | Context-matched font pairing |
| Outer glow `box-shadow` | Diffusion shadow + inner refraction border |
| `h-screen` (iOS Safari bug) | `min-h-[100dvh]` |
| Circular spinner | Layout-matched shimmer skeleton |
| *"Elevate your workflow"* | Concrete product-specific copy |
| `useState` for cursor effects | `useMotionValue` + `useSpring` |
| No dark mode | `[data-theme="dark"]` + `prefers-color-scheme` |
| Missing accessibility | WCAG AA + ARIA + keyboard navigation |

---

## Agent Setup

| Agent | Method |
|---|---|
| Cursor | Drop `SKILL.md` in project root |
| Antigravity | Drop `SKILL.md` in project root |
| Claude Code | Drop `SKILL.md` in root, or append to `CLAUDE.md` |
| Windsurf | Drop `SKILL.md` in project root |
| GitHub Copilot | Add content to `.github/copilot-instructions.md` |
| Codex / ChatGPT | Paste content at top of conversation |
| Aider | `aider --read SKILL.md` |
| Amp, Cline, Warp, Gemini CLI, OpenCode | Drop `SKILL.md` in project root |
| Any LLM API | Pass as the `system` message |

→ Full setup with copy-paste commands: [INTEGRATE.md](INTEGRATE.md)

---

## FAQ

**Does it work with React, Next.js, Vue, Svelte, Astro, or vanilla HTML?**
Yes. Bexa is framework-agnostic. Design rules apply regardless of stack.

**What is a SKILL.md file?**
A portable instruction file that AI coding agents detect and follow automatically from the project root. Like `.cursorrules` or `CLAUDE.md`, but focused entirely on design quality.

**Will it conflict with my existing rules file?**
No. Append Bexa content to your existing `CLAUDE.md` or `.cursorrules`.

**Do I need to edit the file to change the output style?**
No. Tell the agent in plain language: "minimal", "cinematic", "no animations", "data-dense". Dials adjust automatically.

---

## Roadmap

- [ ] `forge-editorial` — Long-form content, editorial grids
- [ ] `forge-brutalist` — Swiss type, raw structure, high contrast
- [ ] `forge-luxury` — Premium whitespace, muted palette, serif display
- [ ] `forge-stitch` — Google Stitch / `DESIGN.md` format

---

## Contributing

Every rule must override a **specific, documented LLM bias**. No vague rules.
See [CONTRIBUTING.md](CONTRIBUTING.md) · [CHANGELOG.md](CHANGELOG.md)

## License

MIT — [LICENSE](LICENSE)
