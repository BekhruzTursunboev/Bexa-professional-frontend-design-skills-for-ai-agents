# FORGE Design Skills

**Stop building generic UIs. Start shipping interfaces that belong in a portfolio.**

FORGE is a collection of agentic design skills that reprogram how AI coding assistants think about frontend design. Every rule is engineered to override the statistical bias LLMs have toward predictable, generic output.

[![License: MIT](https://img.shields.io/badge/License-MIT-black?style=flat-square)](LICENSE)
[![Skills: 4](https://img.shields.io/badge/Skills-4-white?style=flat-square&color=0f172a)](skills/)
[![Agent Compatible](https://img.shields.io/badge/Agent-Cursor_%7C_Claude_%7C_Windsurf_%7C_Copilot-black?style=flat-square)](#install)

---

## What FORGE Is

Most AI-generated UIs suffer from the same fingerprints:

- Centered hero with a purple gradient
- Three equal feature cards with emoji icons
- Inter font at 700 weight, full saturation blue buttons
- `h-screen` that breaks on iOS Safari
- `z-50` sprinkled everywhere
- Generic names like "John Doe" and numbers like "99.9%"

FORGE is a set of opinionated instruction files (SKILL.md) that your AI coding agent reads and follows. Once installed, the agent operates as a **Senior Design Engineer** — not a code monkey.

---

## Skills

| Skill | Use When | SKILL.md |
|---|---|---|
| **forge** | All-purpose. Start here for any web project. | [skills/forge/](skills/forge/SKILL.md) |
| **forge-mobile** | React Native / Expo apps. Native-grade gestures and physics. | [skills/forge-mobile/](skills/forge-mobile/SKILL.md) |
| **forge-dashboard** | SaaS admin panels and data-dense analytics UIs. | [skills/forge-dashboard/](skills/forge-dashboard/SKILL.md) |
| **forge-motion** | Cinematic scroll-storytelling, GSAP, Three.js, Framer choreography. | [skills/forge-motion/](skills/forge-motion/SKILL.md) |

You do not need all four at once. Start with `forge` and add specialized skills as needed.

---

## Install

Works with all major AI coding agents:

```bash
# Via npx (recommended)
npx skills add https://github.com/YOUR_USERNAME/forge-design-skills

# Or manually — copy the SKILL.md for the skill you want into your project root
# Your AI agent detects and follows it automatically
```

Or paste the contents of any `SKILL.md` directly into your AI chat context.

---

## The 3-Dial System

`forge` (the core skill) is driven by three adjustable dials:

| Dial | Range | Effect |
|---|---|---|
| `SPATIAL_TENSION` | 1–10 | 1 = Zen gallery whitespace · 10 = Maximum editorial density |
| `MOTION_DEPTH` | 1–10 | 1 = CSS hover only · 10 = GSAP / Three.js physics |
| `STRUCTURE_CHAOS` | 1–10 | 1 = Symmetric grid · 10 = Organic asymmetric composition |

Default values are set to `7 / 7 / 6` — opinionated but not extreme. The agent adapts dials based on your prompts. Say "clean and minimal" and SPATIAL_TENSION drops. Say "cinematic" and MOTION_DEPTH rises.

---

## What Makes FORGE Different

### vs. taste-skill
taste-skill is excellent for general design variance. FORGE adds:
- A **typed font pairing matrix** by context (SaaS, editorial, luxury, dashboard, mobile)
- **Mobile-specific skill** with gesture physics, haptics, and platform motion rules
- **Dashboard skill** with data visualization standards, chart anti-patterns, and command palette patterns
- **Motion skill** with documented spring configurations, GSAP cleanup patterns, and Three.js GPU memory management

### vs. ui-ux-pro-max
ui-ux-pro-max is a powerful searchable database approach. FORGE is different:
- No Python runtime required — just a Markdown file
- Opinionated dials instead of query-based lookup
- Physics spring reference table built-in
- Specific `prefers-reduced-motion` implementation guidance

---

## Design Principles

**1. Override, don't decorate.**
Every rule exists to override a known LLM bias. If a rule doesn't override something specific, it's cut.

**2. Dials over modes.**
Three continuous dials produce more nuance than named style presets. Real designs exist on a spectrum.

**3. Performance is a design decision.**
Motion rules include GPU cost and cleanup. A beautiful animation that drops to 30fps on mobile failed the design.

**4. Content realism.**
Generic names and fake numbers break the spell. FORGE enforces realistic content standards.

**5. Dark mode is not optional.**
Every project output must support dark mode. It is 2026.

---

## Skill Combinations

```
forge                               # Any web project, safe baseline
forge + forge-motion                # Marketing sites, landing pages, scrolltelling
forge-dashboard                     # Admin panels, analytics, SaaS internals
forge-dashboard + forge-motion      # Live dashboards with real-time animations
forge-mobile                        # React Native / Expo apps
```

---

## Contributing

Open a Pull Request. Requirements:
- Every new rule must override a *specific, named* LLM bias pattern
- Rules must be testable (pass/fail) against output
- No vague rules like "make it look good"

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## License

MIT — free to use, modify, and distribute. See [LICENSE](LICENSE).
