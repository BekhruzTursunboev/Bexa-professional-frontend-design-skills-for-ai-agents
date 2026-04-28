# Contributing to FORGE Design Skills

Thank you for helping make AI-generated frontends less generic.

---

## What We're Building

FORGE is a collection of instruction files (SKILL.md) for AI coding agents.
The goal is not to add more rules — it is to add *the right* rules.

Every rule must:
1. Override a **specific, named, documented** LLM bias pattern
2. Be **testable** — you can look at AI output and say pass/fail
3. Be **framework-agnostic** unless it belongs in a specialized skill

We are not building a style guide for humans. We are building a bias correction layer for AI models.

---

## How to Contribute

### Adding a Rule to an Existing Skill

1. Fork the repo and create a branch: `git checkout -b feat/rule-name`
2. Edit the target `SKILL.md`
3. Add your rule to the appropriate section
4. In your PR description, explain:
   - What LLM bias pattern does this override?
   - What does good output look like?
   - What does bad output look like?

### Creating a New Skill Variant

Valid reasons to create a new skill:
- A distinctly different use-case with conflicting rules (e.g., mobile vs. web)
- A visual direction not covered by existing skills (e.g., brutalist, editorial)
- A platform-specific constraint set (e.g., Electron, VSCode extension)

Invalid reasons:
- Minor preference differences (just adjust the dials)
- Framework-specific wrappers (skills are framework-agnostic)

### What We Won't Merge

- Vague rules ("make it look premium")
- Rules that duplicate existing ones
- Rules requiring specific proprietary tools
- Rules that conflict with the core identity principles in forge/SKILL.md

---

## Code Style

SKILL.md files follow this structure:
```
--- (frontmatter)
# Heading
## SECTION N — NAME
### Subsection
- Rule or table
```

Use tables for reference data. Use bullet lists for rules. Use code blocks for patterns.
Keep sections under 30 lines where possible. Be surgical.

---

## Issues

Use GitHub Issues for:
- Reporting an LLM bias that FORGE doesn't cover
- Requesting a new skill variant
- Discussing a rule that conflicts or is ambiguous

Please include: what agent you're using, what the bad output was, and what good output would look like.
