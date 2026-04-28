# Changelog

All notable changes to Bexa are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [1.1.0] — 2026-04-28

### Added
- `INTEGRATE.md` — full agent setup guide for Cursor, Claude Code, Windsurf, Copilot, Aider, ChatGPT, and direct API usage with copy-paste commands and troubleshooting
- `forge/SKILL.md` — Framer Motion code examples (page transitions, stagger, magnetic button)
- `forge/SKILL.md` — Accessibility section: WCAG AA contrast, ARIA labels, keyboard navigation requirements
- `forge/SKILL.md` — Developer Tool font pairing (`Space Grotesk` + `DM Sans` + `JetBrains Mono`)
- `forge/SKILL.md` — CSS dark mode token structure (`[data-theme="dark"]`) with full variable set
- `forge/SKILL.md` — GSAP `gsap.context()` + `ctx.revert()` cleanup pattern
- `forge/SKILL.md` — `prefers-reduced-motion` CSS implementation + Framer `useReducedMotion()`
- `forge/SKILL.md` — Hero pattern reference table (5 non-default options)
- `forge/SKILL.md` — 12-point pre-output quality gate (expanded from 8-point)
- `forge/SKILL.md` — Content realism table: names, numbers, money, phones, brand names, copy
- GitHub Issue templates: Bug Report and Rule Proposal

### Changed
- `README.md` — rewritten with real repo URLs, curl install commands, version badges, before/after table, agent compatibility table, FAQ, and verification checklist
- `forge/SKILL.md` — Section 4 color system expanded with full light + dark token set, accent palette reference table, and feedback color tokens (success, warning, error)
- `forge/SKILL.md` — Section 5 layout expanded with hero pattern options and section anatomy diagram
- `forge/SKILL.md` — Section 6 motion depth scale expanded with Framer code patterns

---

## [1.0.0] — 2026-04-28

### Added
- `forge/SKILL.md` — Core all-purpose web design skill with 3-dial system (SPATIAL_TENSION / MOTION_DEPTH / STRUCTURE_CHAOS), font pairing matrix, HSL color token system, layout anti-pattern bans, motion depth scale, component quality standards, and pre-output quality gate
- `forge-dashboard/SKILL.md` — Data-dense SaaS admin panel skill: information architecture, chart standards, command palette, KPI metric layout, sidebar navigation, keyboard accessibility
- `forge-mobile/SKILL.md` — React Native / Expo skill: thumb zone architecture, touch targets, safe areas, gesture physics with Reanimated 3 spring configs, platform-specific motion (iOS vs Android), haptic feedback taxonomy, performance mandates (FlashList, JS-thread ban)
- `forge-motion/SKILL.md` — Cinematic animation skill: motion philosophy hierarchy, 5 named spring configurations, Framer Motion patterns (page transitions, stagger, magnetic, shared element), GSAP scrolltelling with cleanup, Three.js WebGL setup with GPU memory management, CSS animation primitives
- `README.md`, `LICENSE` (MIT), `CONTRIBUTING.md`, `.gitignore`
- `.github/ISSUE_TEMPLATE/` — Bug report and rule proposal templates
