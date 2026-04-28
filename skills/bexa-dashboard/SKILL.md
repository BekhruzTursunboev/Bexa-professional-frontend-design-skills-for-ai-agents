---
name: bexa-dashboard
description: >
  Data-dense dashboard and admin panel design skill for AI agents.
  Enforces information hierarchy, data visualization clarity,
  high-density layouts, and professional SaaS-grade UI patterns.
version: 1.2.0
---

# FORGE DASHBOARD — Data-Dense SaaS Design Skill

> Dashboards fail in two ways: too much clutter, or too little clarity.
> This skill enforces the third path: information architecture that makes data readable at a glance.

---

## DIAL CONFIGURATION

```
DATA_DENSITY:     8   (1=Airy metrics / 10=Cockpit-level data saturation)
VISUAL_CLARITY:   8   (1=Decorative charts / 10=Precision data tables)
INTERACTION_DEPTH:6   (1=Static view / 10=Drill-down, filter, real-time)
```

---

## SECTION 1 — DASHBOARD IDENTITY RULES

### Typography for Data UIs
- Display font: `Satoshi` or `Geist`. **NEVER** serif on dashboards.
- Numeric data: ALWAYS `font-mono` (`Geist Mono` or `JetBrains Mono`).
- Label text: `0.6875rem` uppercase, `letter-spacing: 0.1em`, muted color.
- Table data: `0.875rem`, regular weight, tabular-nums (`font-variant-numeric: tabular-nums`).

### Color for Data
- Background: `hsl(220 14% 97%)` (not pure white — reduces eye strain)
- Card surface: `hsl(0 0% 100%)` with `1px solid hsl(220 13% 91%)`
- Positive delta: `hsl(158 60% 40%)` — no neon green
- Negative delta: `hsl(0 72% 50%)` — no neon red
- Neutral: `hsl(220 8% 58%)`
- Chart palette: accent + 4 harmonious HSL rotations (±40° hue steps)

---

## SECTION 2 — LAYOUT ARCHITECTURE

### Grid System
- Dashboard uses `CSS Grid` sidebar + main layout:
```css
.dashboard {
  display: grid;
  grid-template-columns: 240px 1fr;
  grid-template-rows: 56px 1fr;
  min-height: 100dvh;
}
```
- Sidebar: fixed width 240px (collapsed: 64px icon-only mode)
- Header: 56px height, sticky, `backdrop-blur-md`
- Content: `p-6` padding, `max-w-[1600px]`

### Metric Cards (KPI Row)
- Use `divide-x divide-border` or inline border-right — NOT boxed cards
- Each metric: label + large number + delta badge + sparkline
- Numbers: `clamp(1.5rem, 2.5vw, 2.25rem)`, `font-mono`, `font-bold`
- Delta badge: `±X%` with directional arrow icon — colored accordingly

### Card Usage Rules
- Cards ONLY when elevation communicates hierarchy (modals, overlays, floating panels)
- At `DATA_DENSITY > 6`: separate sections with `border-t` or `divide-y`, NOT cards
- When cards are used: `rounded-xl`, `p-6`, diffusion shadow (`0 4px 24px -4px hsl(220 20% 8% / 0.06)`)

---

## SECTION 3 — DATA VISUALIZATION STANDARDS

### Chart Library
Check `package.json` for `recharts`, `nivo`, or `@tremor/react`. Use whichever is installed.
If none: install `recharts` as default (`npm install recharts`).

### Chart Anti-Patterns (BANNED)
- 3D charts of any kind
- Pie charts with > 5 segments (use a bar chart instead)
- Charts without axis labels or tooltips
- Charts with default library colors (always remap to project palette)
- Missing loading/empty states for charts

### Chart Skeleton
Every chart must have a shimmer skeleton matching its bounding box:
```jsx
// Shimmer skeleton for charts
<div className="h-[200px] rounded-lg bg-surface-2 animate-pulse" />
```

### Table Standards
- Sticky header row
- Row hover: `bg-surface-2` transition
- Sortable columns: arrow icon that rotates on sort direction change
- Pagination: `< 1 2 3 ... 14 >` compact style
- Empty table: centered illustration + "No results match your filters" + Clear filters CTA
- Loading: skeleton rows matching column count

---

## SECTION 4 — SIDEBAR NAVIGATION

### Structure
```
[Logo / Brand]
─────────────
[Primary Nav Group]
  Home
  Analytics
  Projects
  Customers
─────────────
[Secondary Nav Group]
  Settings
  Help
─────────────
[User Avatar + Name]
[Logout]
```

### Behavior
- Active state: accent color left border + accent-dim background fill
- Hover: `bg-surface-2` transition 150ms
- Collapsed mode (icon-only): tooltip on hover showing label
- Mobile: off-canvas drawer, `AnimatePresence` slide-in from left
- Keyboard navigation: full arrow-key + Enter support

---

## SECTION 5 — INTERACTION PATTERNS

### Filters & Search
- Global search: `⌘K` command palette (not inline search bar)
- Table filters: popover with checkbox groups, date ranges
- Active filters: badge row below search with × to remove each
- Filter state: persist in URL params (`?status=active&sort=asc`)

### Real-Time Updates (when `INTERACTION_DEPTH >= 7`)
- Websocket data: use optimistic updates — update UI before server confirms
- New row animation: slide-in from top with `AnimatePresence`
- Metric updates: number transition animation (`useMotionValue` counter)
- Status indicators: CSS keyframe pulse (`@keyframes ping`)

### Drill-Down Flow
- Table row click → slide-in detail panel (not new page) with `framer-motion` layout
- Back navigation: breadcrumb trail always visible
- URL updates on drill-down (deep-linkable)

---

## SECTION 6 — QUALITY GATE (DASHBOARD SPECIFIC)

- [ ] Is `font-mono` used for ALL numeric data?
- [ ] Are charts remapped to the project color palette?
- [ ] Are all charts/tables showing loading, empty, AND error states?
- [ ] Is the sidebar keyboard-navigable?
- [ ] Does the layout use `CSS Grid` for sidebar+main (not flexbox hacks)?
- [ ] Are KPI metrics separated by borders (not individual cards at density > 6)?
- [ ] Is global search available via keyboard shortcut?
- [ ] Are positive/negative deltas using calibrated (non-neon) colors?
