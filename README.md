# FORGE Design Skills

<p align="center">
  <strong>Stop shipping generic UIs. Start building interfaces that belong in a portfolio.</strong>
</p>

<p align="center">
  FORGE is a pack of <code>SKILL.md</code> files that reprogram how AI coding agents think about frontend design.<br/>
  Drop one file. Your agent becomes a Senior Design Engineer.
</p>

<p align="center">
  <a href="skills/forge/SKILL.md"><img src="https://img.shields.io/badge/skill-forge-0f172a?style=flat-square" /></a>
  <a href="skills/forge-dashboard/SKILL.md"><img src="https://img.shields.io/badge/skill-forge--dashboard-0f172a?style=flat-square" /></a>
  <a href="skills/forge-mobile/SKILL.md"><img src="https://img.shields.io/badge/skill-forge--mobile-0f172a?style=flat-square" /></a>
  <a href="skills/forge-motion/SKILL.md"><img src="https://img.shields.io/badge/skill-forge--motion-0f172a?style=flat-square" /></a>
  <img src="https://img.shields.io/badge/agents-Cursor_%7C_Claude_%7C_Windsurf_%7C_Copilot_%7C_Aider-1e293b?style=flat-square" />
  <img src="https://img.shields.io/badge/license-MIT-22c55e?style=flat-square" />
</p>

---

## The Problem

Every AI-generated UI has the same fingerprints:

- Centered hero. Centered H1. Purple-blue gradient.
- Three equal feature cards with emoji icons.
- Inter font. Full-saturation blue buttons.
- `h-screen` that breaks on iOS Safari.
- `#000` backgrounds. Broken Unsplash links.
- "Elevate your seamless next-gen workflow."

**FORGE eliminates all of it.** Every rule overrides a documented LLM bias pattern.

---

## Install in 30 Seconds

```bash
# Copy the skill you need into your project root
curl -o SKILL.md https://raw.githubusercontent.com/YOUR_USERNAME/forge-design-skills/main/skills/forge/SKILL.md
```

Or manually download and drop `SKILL.md` into your project root.
Your agent detects and follows it automatically. No config. No CLI. No setup.

> See [INTEGRATE.md](INTEGRATE.md) for Cursor, Claude Code, Windsurf, Copilot, Aider, and API setup.

---

## Skills

| Skill | Best For | File |
|---|---|---|
| **forge** | Any web project. Start here. | [skills/forge/SKILL.md](skills/forge/SKILL.md) |
| **forge-dashboard** | SaaS admin panels, analytics UIs, data-dense layouts | [skills/forge-dashboard/SKILL.md](skills/forge-dashboard/SKILL.md) |
| **forge-mobile** | React Native / Expo apps — native gestures, haptics | [skills/forge-mobile/SKILL.md](skills/forge-mobile/SKILL.md) |
| **forge-motion** | Scroll-storytelling, GSAP, Three.js, Framer choreography | [skills/forge-motion/SKILL.md](skills/forge-motion/SKILL.md) |

---

## The 3-Dial System

`forge` runs on three continuously adjustable dials. You never edit the file — just talk to your agent normally.

```
SPATIAL_TENSION:  7   (1 = Zen gallery whitespace  →  10 = Max editorial density)
MOTION_DEPTH:     7   (1 = CSS hover only          →  10 = GSAP + physics)
STRUCTURE_CHAOS:  6   (1 = Symmetric 12-col grid   →  10 = Organic asymmetric)
```

**Dial overrides happen in your prompt:**

| What you say | What changes |
|---|---|
| "keep it clean and minimal" | SPATIAL_TENSION drops — more whitespace |
| "make it cinematic" | MOTION_DEPTH rises — springs, scroll effects |
| "editorial style" | STRUCTURE_CHAOS rises — asymmetric layouts |
| "no animations" | MOTION_DEPTH = 2 — CSS hover only |
| "data-dense, cockpit mode" | SPATIAL_TENSION rises — tight, packed UI |

---

## What FORGE Changes

### Typography
Instead of Inter at default weight, FORGE uses a **context-specific font pairing matrix**:

| Context | Display | Body | Mono |
|---|---|---|---|
| SaaS / Product | Geist | Geist | Geist Mono |
| Editorial / Blog | Fraunces | Plus Jakarta Sans | JetBrains Mono |
| Portfolio / Agency | Cabinet Grotesk | Outfit | Fira Code |
| Dashboard / Data | Satoshi | Inter | Geist Mono |
| Luxury / Brand | Cormorant Garamond | Jost | — |
| Developer Tool | Space Grotesk | DM Sans | JetBrains Mono |

### Color
Instead of hardcoded hex values, FORGE enforces an **HSL token system**:

```css
:root {
  --surface-0:  hsl(0 0% 98%);       /* page background */
  --accent:     hsl(221 70% 52%);    /* one accent, calibrated saturation */
  --accent-dim: hsl(221 70% 52% / 0.12);
  --text-primary:   hsl(220 20% 10%);
  --text-secondary: hsl(220 10% 38%);
  --border:     hsl(220 13% 91%);
}
```

### Motion
Instead of `useState` for cursor effects, FORGE uses proper **Framer Motion physics**:

```jsx
// Magnetic button — outside render cycle, never useState
const x = useMotionValue(0)
const y = useMotionValue(0)
const sx = useSpring(x, { stiffness: 200, damping: 20 })
const sy = useSpring(y, { stiffness: 200, damping: 20 })
```

### Layout
Instead of 3 equal cards and centered heroes, FORGE enforces **asymmetric, intentional composition**:

```css
/* Fractional grid (STRUCTURE_CHAOS 5-6) */
grid-template-columns: 3fr 2fr;

/* Asymmetric padding (STRUCTURE_CHAOS 7-8) */
padding-left: clamp(2rem, 12vw, 14rem);
```

---

## Before & After

| AI Default | FORGE Output |
|---|---|
| Centered hero + centered H1 | Left-anchored or split-screen hero |
| 3 equal feature cards in a row | Zigzag, masonry, or 70/30 asymmetric |
| AI purple / full-saturation blue gradient | Single HSL-calibrated accent ≤ 75% saturation |
| `Inter` font at default weight | Context-specific pairing from matrix |
| Outer glow `box-shadow` on cards | Diffusion shadow + inner refraction border |
| `#000` / `#fff` backgrounds | Off-black `hsl(220 20% 8%)` / off-white `hsl(0 0% 98%)` |
| Generic circular spinner | Layout-matched shimmer skeleton |
| "Elevate your seamless workflow" | Concrete product-specific verbs |
| `h-screen` | `min-h-[100dvh]` |
| `useState` for cursor animations | `useMotionValue` + `useSpring` |
| Broken Unsplash links | `picsum.photos/seed/{word}/w/h` |
| "John Doe" placeholder names | Culturally varied realistic names |
| No dark mode | `[data-theme="dark"]` + `prefers-color-scheme` |
| Missing accessibility | WCAG AA contrast + ARIA + keyboard nav |

---

## Skill Combinations

```
forge                             # All web projects — safe default
forge + forge-motion              # Marketing sites, landing pages, scrolltelling
forge-dashboard                   # Admin panels, SaaS internals, analytics
forge-dashboard + forge-motion    # Live dashboards with real-time animation
forge-mobile                      # React Native / Expo apps
```

---

## Agent Compatibility

| Agent | Method |
|---|---|
| **Cursor** | Drop `SKILL.md` in project root. Auto-detected. |
| **Claude Code** | Drop `SKILL.md` in root, or append to `CLAUDE.md`. |
| **Windsurf** | Drop `SKILL.md` in root. Auto-detected. |
| **GitHub Copilot** | Add to `.github/copilot-instructions.md`. |
| **Aider** | `aider --read SKILL.md` |
| **ChatGPT / Codex** | Paste content at top of conversation. |
| **API (Claude/GPT)** | Pass as `system` message. |

Full instructions with copy-paste commands → [INTEGRATE.md](INTEGRATE.md)

---

## FAQ

**Does it work with React, Vue, Svelte, Astro?**
Yes. FORGE is framework-agnostic. The rules focus on design decisions, not framework-specific patterns. Stack conventions in Section 2 default to Next.js but yield to whatever the user specifies.

**What is a SKILL.md file?**
A portable instruction file that AI coding agents detect and follow automatically when placed in the project root. Think of it as a `CLAUDE.md` or `cursor-rules` file, but for design quality.

**Will it conflict with my existing `CLAUDE.md` or `.cursorrules`?**
No. Append the SKILL.md content to your existing file. Design rules and project-specific instructions coexist fine.

**How is this different from taste-skill?**
taste-skill is excellent for general design variance. FORGE adds: a typed font pairing matrix by context, a mobile-native skill with gesture physics and haptics, a dashboard skill with data visualization standards and command palette patterns, a motion skill with named spring configs and GPU cleanup patterns, and a full accessibility baseline.

**Can I adjust the output without editing the file?**
Yes. Say "minimal", "cinematic", "editorial", "no animations", or "cockpit mode" in your prompt. The agent maps these to dial values automatically.

---

## Roadmap

> Community contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md)

- [ ] `forge-editorial` — Long-form article and blog design rules
- [ ] `forge-brutalist` — Swiss typography, raw structure, sharp contrast
- [ ] `forge-luxury` — Cormorant Garamond, generous whitespace, muted palette
- [ ] `forge-stitch` — Google Stitch / `DESIGN.md` compatible output
- [ ] `forge-3d` — Three.js product showcase and WebGL patterns

---

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md). In short:
- Every new rule must override a **specific, named** LLM bias
- Rules must be pass/fail testable against real output
- No vague rules. "Make it look premium" is not a rule.

---

## License

MIT — [LICENSE](LICENSE)
