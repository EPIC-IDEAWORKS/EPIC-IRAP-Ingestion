# EPIC IRAP Website

A single-page marketing site for EPIC's IRAP program, hosted on GitHub Pages. Styled per Mohawk College brand guidelines.

The site provides program information and directs interested visitors to an application/contact form. Currently a template with placeholder content — real copy will be filled in later.

**Stack:** Static HTML/CSS/JS. No build tools, no frameworks.

---

## Styling Rules

**Brand reference:** All visual decisions (colors, fonts, spacing, logo usage) must follow `docs/mohawk-brand-style-guide.md`. The CSS custom properties in `epic-theme.css` are derived from values in that guide.

All cards and embeddable components must follow these rules so they look intentional when embedded in external platforms and coherent standalone:

- `background: transparent` on `html`/`body` — no white box behind embedded cards
- No fixed pixel widths — fluid layout (`%`, `max-width`, `rem`)
- No fixed height — each card is one bounded unit, no internal scrolling
- Minimal chrome — thin border, single accent-colored left rule; no shadows, no branded backgrounds beyond the one accent
- Embeddable card templates: **no site header, nav, or footer**
- Four CSS variables at the top of every card/component file, pulled from `epic-theme.css`:
  - `--epic-accent`
  - `--epic-accent-soft`
  - `--epic-font-display`
  - `--epic-font-body`

Token values are **hardcoded, not dynamic.** Update `epic-theme.css` periodically when the external platform theme changes.

---

## Git Workflow

**Remote:** `git@github.com:EPIC-IDEAWORKS/EPIC-IRAP-Ingestion.git`

### Branch Naming

```
feature/<short-description>
fix/<short-description>
chore/<short-description>
```

### Commit Message Format

Conventional Commits: `feat:` / `fix:` / `test:` / `chore:` / `refactor:`

Commit attribution: **"Created and reviewed by Gord Bond"** — do not mention Claude in any commit message or PR.

### Rules

- Only push when explicitly asked by the user. Never push to `main`.
- PRs are handled manually by the user — do not open them.
- Never sign a commit or PR as Claude. All commits are attributed to Gord Bond.
- Before any push: lint clean, no broken links, content clearance confirmed.

---

## Behavioral Guidelines

### 1. Think Before Coding

Don't assume. Don't hide confusion. Surface tradeoffs.

Before implementing:
- State assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them — don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what's confusing. Ask.

### 2. Simplicity First

Minimum code that solves the problem. Nothing speculative.

- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

### 3. Surgical Changes

Touch only what you must. Clean up only your own mess.

When editing existing code:
- Don't "improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it — don't delete it.

When your changes create orphans:
- Remove imports/variables/functions that **your** changes made unused.
- Don't remove pre-existing dead code unless asked.

Every changed line should trace directly to the user's request.

### 4. Goal-Driven Execution

Define success criteria. Loop until verified.

Transform tasks into verifiable goals:
- "Add a new card type" → "Build the HTML/CSS, verify it renders standalone and at narrow widths"
- "Fix layout bug" → "Identify the broken state, fix it, verify at 320px and 960px"

For multi-step tasks, state a brief plan:
```
1. [Step] → verify: [check]
2. [Step] → verify: [check]
3. [Step] → verify: [check]
```

---

## IMPORTANT

- **Build one phase at a time.** Do not start the next until the current is complete and the user approves.
- **Never hardcode secrets.** No credentials, keys, or private partner data in the repo.
- **Content clearance is a gate, not a suggestion.** Nothing with partner data or unreleased results merges without review.
- **Tradeoff:** These guidelines bias toward caution over speed. For trivial tasks, use judgment.
