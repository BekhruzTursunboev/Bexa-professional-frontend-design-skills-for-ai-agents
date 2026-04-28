# Bexa — Professional Frontend Design Skills for AI Agents

<p align="center">
  <strong>Stop shipping generic UIs. Start building interfaces that belong in a portfolio.</strong><br/>
  Drop one file. Your AI agent becomes a Senior Design Engineer.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.1.0-0f172a?style=flat-square" />
  <img src="https://img.shields.io/badge/skills-4-0f172a?style=flat-square" />
  <img src="https://img.shields.io/badge/license-MIT-22c55e?style=flat-square" />
  <img src="https://img.shields.io/badge/agents-Cursor_%7C_Claude_%7C_Windsurf_%7C_Copilot_%7C_Aider-1e293b?style=flat-square" />
  <img src="https://img.shields.io/badge/framework-agnostic-1e293b?style=flat-square" />
</p>

---

## The Problem

Every AI-generated UI has the same fingerprints:

- Centered hero. Centered H1. Purple-blue gradient.
- Three equal feature cards with emoji icons.
- Inter font. Full-saturation blue buttons.
- `h-screen` that breaks on iOS Safari.
- `#000` backgrounds. Broken Unsplash image links.
- *"Elevate your seamless next-gen workflow."*

**Bexa eliminates all of it.** Every rule overrides a specific, documented LLM design bias.

---

## Install

### Option 1 — curl (fastest)

```bash
# Core skill — start here for any web project
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md

# Dashboard / admin panel
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-dashboard/SKILL.md

# React Native / Expo mobile
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-mobile/SKILL.md

# Cinematic motion — GSAP, Three.js, Framer
curl -o SKILL.md https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-motion/SKILL.md
```

### Option 2 — Manual Download

1. Click the skill file you need from the table below
2. Copy the raw content
3. Paste into a new file called `SKILL.md` in your project root

**Done.** Your agent detects and follows it automatically. No config. No CLI. No setup.

---

## Skills

| Skill | Best For | Quick Install |
|---|---|---|
| **forge** | Any web project — the default starting point | [View](skills/forge/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge/SKILL.md) |
| **forge-dashboard** | SaaS admin panels, analytics, data-dense UIs | [View](skills/forge-dashboard/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-dashboard/SKILL.md) |
| **forge-mobile** | React Native / Expo — native gestures & haptics | [View](skills/forge-mobile/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-mobile/SKILL.md) |
| **forge-motion** | Scroll-storytelling, GSAP, Three.js, Framer | [View](skills/forge-motion/SKILL.md) · [Raw](https://raw.githubusercontent.com/BekhruzTursunboev/Bexa-professional-frontend-design-skills-for-ai-agents/main/skills/forge-motion/SKILL.md) |

---

## Agent Setup

| Agent | What to do |
|---|---|
| **Cursor** | Drop `SKILL.md` in project root — auto-detected |
| **Claude Code** | Drop `SKILL.md` in root, or append to `CLAUDE.md` |
| **Windsurf** | Drop `SKILL.md` in project root — auto-detected |
| **GitHub Copilot** | Paste content into `.github/copilot-instructions.md` |
| **Aider** | `aider --read SKILL.md` |
| **ChatGPT / Codex** | Paste content at the top of your conversation |
| **API (any model)** | Pass as the `system` message |

> Full copy-paste commands for every agent → [INTEGRATE.md](INTEGRATE.md)

---

## Combining Skills

```bash
# Marketing site / landing page
curl -o SKILL.md       .../skills/forge/SKILL.md
curl -o SKILL-MOTION.md .../skills/forge-motion/SKILL.md

# SaaS dashboard with live animation
curl -o SKILL.md       .../skills/forge-dashboard/SKILL.md
curl -o SKILL-MOTION.md .../skills/forge-motion/SKILL.md

# React Native app
curl -o SKILL.md .../skills/forge-mobile/SKILL.md
```

Stack multiple `SKILL-*.md` files in your root — agents read all of them.

---

## The 3-Dial System

Every skill runs on three dials. **You never edit the file.** Just talk to your agent naturally.

```
SPATIAL_TENSION:  7   (1 = Zen gallery whitespace  →  10 = Max editorial density)
MOTION_DEPTH:     7   (1 = CSS hover only          →  10 = GSAP + physics)
STRUCTURE_CHAOS:  6   (1 = Symmetric 12-col grid   →  10 = Organic asymmetric)
```

| Say this in your prompt | What changes |
|---|---|
| "keep it clean and minimal" | SPATIAL_TENSION drops — more whitespace |
| "make it cinematic / animated" | MOTION_DEPTH rises — springs, scroll effects |
| "editorial / asymmetric style" | STRUCTURE_CHAOS rises — offset layouts |
| "no animations, CSS only" | MOTION_DEPTH = 2 |
| "data-dense / cockpit mode" | SPATIAL_TENSION rises — tight, packed UI |

---

## What Changes

### Typography

Instead of Inter at default weight, Bexa uses a **context-specific font pairing matrix**:

| Context | Display | Body | Mono |
|---|---|---|---|
| SaaS / Product | Geist | Geist | Geist Mono |
| Editorial / Blog | Fraunces | Plus Jakarta Sans | JetBrains Mono |
| Portfolio / Agency | Cabinet Grotesk | Outfit | Fira Code |
| Dashboard / Data | Satoshi | Inter | Geist Mono |
| Luxury / Brand | Cormorant Garamond | Jost | — |
| Developer Tool | Space Grotesk | DM Sans | JetBrains Mono |
| Mobile App | Sora | DM Sans | — |

### Color

Instead of hardcoded hex values, Bexa enforces an **HSL token system**:

```css
:root {
  --surface-0:      hsl(0 0% 98%);        /* page background   */
  --surface-1:      hsl(0 0% 100%);       /* card / panel      */
  --accent:         hsl(221 70% 52%);     /* one accent color  */
  --accent-dim:     hsl(221 70% 52% / 0.12);
  --text-primary:   hsl(220 20% 10%);
  --text-secondary: hsl(220 10% 38%);
  --border:         hsl(220 13% 91%);
}
```

### Motion

Instead of `useState` for cursor effects, Bexa uses proper **Framer Motion physics**:

```jsx
// Outside render cycle — never useState for animations
const x = useMotionValue(0)
const y = useMotionValue(0)
const sx = useSpring(x, { stiffness: 200, damping: 20 })
const sy = useSpring(y, { stiffness: 200, damping: 20 })
```

---

## Before & After

| AI Default | Bexa Output |
|---|---|
| Centered hero + centered H1 | Left-anchored or split-screen hero |
| 3 equal feature cards in a row | Zigzag, masonry, or 70/30 asymmetric |
| AI purple / full-saturation blue gradient | Single HSL-calibrated accent ≤ 75% sat |
| `Inter` font at default weight | Context-specific pairing from matrix |
| Outer glow `box-shadow` on cards | Diffusion shadow + inner refraction border |
| `#000` / `#fff` backgrounds | Off-black `hsl(220 20% 8%)` / off-white `hsl(0 0% 98%)` |
| Generic circular spinner | Layout-matched shimmer skeleton |
| *"Elevate your seamless workflow"* | Concrete product-specific verbs |
| `h-screen` (breaks on iOS Safari) | `min-h-[100dvh]` |
| `useState` for cursor animations | `useMotionValue` + `useSpring` |
| Broken Unsplash links | `picsum.photos/seed/{word}/w/h` |
| "John Doe" placeholder names | Culturally varied realistic names |
| No dark mode | `[data-theme="dark"]` + `prefers-color-scheme` |
| Missing accessibility | WCAG AA + ARIA labels + keyboard nav |

---

## Verify It's Working

After your first generation with Bexa active, check:

- [ ] Font is NOT Inter/Roboto/Open Sans used as a display font
- [ ] No centered hero + centered H1 (at default dial settings)
- [ ] Colors defined as `hsl()` tokens in `:root`, not hardcoded hex
- [ ] Full-height sections use `min-h-[100dvh]` not `h-screen`
- [ ] Buttons have hover AND active/press states
- [ ] Loading states use skeleton matching the layout — not a spinner
- [ ] Dark mode implemented

---

## FAQ

**Does it work with React, Vue, Svelte, Astro, vanilla HTML?**
Yes. Skills are framework-agnostic. The rules focus on design decisions. Stack defaults (Next.js, Tailwind) yield to whatever you specify.

**What is a SKILL.md file?**
A portable instruction file that AI agents detect and follow automatically when placed in the project root. Like `.cursorrules` or `CLAUDE.md`, but purpose-built for design quality.

**Will it conflict with my existing `CLAUDE.md` or `.cursorrules`?**
No. Append the skill content to your existing file. Design rules and project rules coexist fine.

**Can I adjust output without editing the file?**
Yes. Say "minimal", "cinematic", "editorial", "no animations", or "cockpit mode" in your prompt. The agent maps these to dial adjustments automatically.

**What agents are supported?**
Cursor, Claude Code, Windsurf, GitHub Copilot, Aider, ChatGPT, Codex, and any LLM API via system prompt.

---

## Roadmap

> Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md)

- [ ] `forge-editorial` — Long-form article and blog design rules
- [ ] `forge-brutalist` — Swiss typography, raw structure, sharp contrast  
- [ ] `forge-luxury` — Cormorant Garamond, generous whitespace, muted palette
- [ ] `forge-stitch` — Google Stitch / `DESIGN.md` compatible output
- [ ] `forge-3d` — Three.js product showcase patterns

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for full version history.

**v1.1.0** — Framer Motion code examples, accessibility section (WCAG AA, ARIA, keyboard nav), expanded content realism standards, developer-tool font pairing, CSS dark mode token structure, 12-point quality gate, INTEGRATE.md agent setup guide.

**v1.0.0** — Initial release. forge, forge-dashboard, forge-mobile, forge-motion.

---

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md). In short:
- Every rule must override a **specific, named** LLM bias pattern
- Rules must be pass/fail testable against real output
- No vague rules — "make it look premium" is not a rule

---

## License

MIT — free to use, modify, and distribute. See [LICENSE](LICENSE).
