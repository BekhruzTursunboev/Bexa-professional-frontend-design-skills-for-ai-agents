# FORGE — Integration Guide

Get up and running in under 2 minutes with any AI coding agent.

---

## Method 1 — Drop the File (Works Everywhere)

Copy the `SKILL.md` you need into your project root. That's it.
Your agent detects and follows it automatically.

```
your-project/
├── SKILL.md          ← paste forge/SKILL.md here
├── src/
├── package.json
└── ...
```

For multiple skills, merge the files or stack them:
```
SKILL.md              ← forge (core, always first)
SKILL-MOTION.md       ← forge-motion (add-on)
SKILL-DASHBOARD.md    ← forge-dashboard (add-on)
```

---

## Method 2 — Agent-Specific Setup

### Cursor
Place `SKILL.md` in project root. Cursor reads it as a context rule automatically.

To apply globally (all projects):
```
~/.cursor/rules/SKILL.md
```

### Claude Code (claude.ai/code)
```bash
# In your project root
cp path/to/forge/SKILL.md ./SKILL.md
```
Or paste contents into `CLAUDE.md` if you already have one — append at the bottom.

### Windsurf
Place `SKILL.md` in project root. Windsurf picks it up as a workspace rule.

Global rules: Settings → AI → Rules → paste content.

### GitHub Copilot (VS Code)
Create `.github/copilot-instructions.md` and paste the SKILL.md contents inside.

```
your-project/
└── .github/
    └── copilot-instructions.md   ← paste skill content here
```

### Aider
```bash
aider --read skills/forge/SKILL.md
```

### OpenAI Codex / ChatGPT
Paste the SKILL.md content at the top of your conversation, then give your task.

---

## Method 3 — System Prompt (API / Custom Agents)

If you're building with the API directly, prepend SKILL.md as a system message:

```python
with open("skills/forge/SKILL.md") as f:
    skill = f.read()

response = client.messages.create(
    model="claude-opus-4-5",
    system=skill,
    messages=[{"role": "user", "content": "Build me a SaaS landing page"}]
)
```

---

## Which Skill to Use

| Building | Use |
|---|---|
| Any web project | `forge` |
| Marketing / landing page | `forge` + `forge-motion` |
| Admin panel / SaaS dashboard | `forge-dashboard` |
| React Native / Expo app | `forge-mobile` |
| Scroll-storytelling site | `forge` + `forge-motion` |
| Live data dashboard | `forge-dashboard` + `forge-motion` |

---

## Dial Overrides (In Your Prompt)

You never need to edit the SKILL.md file. Just tell the agent in plain language:

| Say this | Effect |
|---|---|
| "keep it clean and minimal" | SPATIAL_TENSION drops → more whitespace |
| "make it cinematic / animated" | MOTION_DEPTH rises → springs, scroll effects |
| "editorial / editorial style" | STRUCTURE_CHAOS rises → asymmetric layouts |
| "data-dense / cockpit mode" | SPATIAL_TENSION rises → tight, packed UI |
| "simple, no animations" | MOTION_DEPTH drops → CSS hover only |

---

## Verifying It Worked

After your first generation with FORGE active, check:

- [ ] Font is NOT Inter/Roboto/Open Sans by default
- [ ] No centered hero with centered H1 (at default dials)
- [ ] Colors use `hsl()` tokens, not hardcoded hex
- [ ] Full-height sections use `min-h-[100dvh]`
- [ ] Buttons have hover AND active/press states
- [ ] Loading skeleton matches the layout shape
- [ ] Dark mode is implemented

If any of these fail, paste the failing output as a GitHub Issue.

---

## Troubleshooting

**Agent ignores the skill?**
→ Some agents need explicit activation. Start your prompt with:
`"Follow the FORGE design skill rules strictly. Build me..."`

**Too many animations?**
→ Add to your prompt: `"MOTION_DEPTH: 3"` or `"no animations, CSS only"`

**Layout too complex for the project?**
→ Add to your prompt: `"STRUCTURE_CHAOS: 2, keep it symmetric"`

**Tailwind v3 vs v4 conflicts?**
→ The skill checks `package.json` automatically. If it doesn't, add to your prompt:
`"We are using Tailwind v3"` or `"Tailwind v4"`
