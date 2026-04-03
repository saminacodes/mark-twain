Create a new changelog or release notes from git history.

## What to do

$ARGUMENTS

Arguments can be:
- A version number (e.g. `1.2.0`) — generate release notes for that version's tag range
- A commit range (e.g. `v1.1.0..HEAD`) — generate entries for that range
- A version number + description (e.g. `2.0.0 "major auth refactor"`) — use as context

**Before writing, ask the user:**

1. **Where should the file be saved?**
   - If a `CHANGELOG.md` already exists, default to prepending to it — but confirm first.
   - Otherwise, ask for the output path (e.g. `CHANGELOG.md`, `docs/changelog.md`, `docs/releases/2.0.md`).

2. **Which documentation library is used, if any?**
   - None / plain Markdown
   - [Docusaurus](https://docusaurus.io) — uses MDX, admonitions (`:::note`), and front matter
   - [Nextra](https://nextra.site) — uses MDX with `Callout`, `Steps`, `Tabs` components
   - [Mintlify](https://mintlify.com) — uses MDX with `Note`, `Warning`, `Tip` callout components
   - [VitePress](https://vitepress.dev) — uses Markdown with custom containers (`::: info`)
   - [MkDocs](https://www.mkdocs.org) — uses Markdown with admonition syntax (`!!! note`)
   - [Starlight](https://starlight.astro.build) — uses MDX with `<Aside>` component
   - [GitBook](https://www.gitbook.com) — uses Markdown with `{% hint style="info" %}` blocks
   - Other — ask what component or callout syntax to use

   Adapt all callouts, notes, and warnings to the correct syntax for the chosen library.

---

## Writing Style & Guidelines

> Fill in this section with your preferences. Delete any headings that don't apply.

**Voice & Tone**
<!-- e.g. "Concise and matter-of-fact. No marketing spin." -->

**Audience**
<!-- Who reads this changelog? e.g. "End users" / "Internal developers" -->

**Categorization rules**
<!-- e.g. "Add a 'Security' category for CVE fixes." -->
<!-- e.g. "Skip the 'Internal' category — this is a public-facing changelog." -->

**Entry format**
<!-- e.g. "Each entry must start with an imperative verb: Add, Fix, Remove, Update." -->
<!-- e.g. "Include the affected component in brackets: [API] Fix rate limiting bug." -->

**What to omit**
<!-- e.g. "Skip test-only and docs-only commits." -->
<!-- e.g. "Omit dependency bump commits." -->

---

## Instructions

1. **Read the git log.**
   Run: `!git log --oneline --no-merges $(git describe --tags --abbrev=0 2>/dev/null || git rev-list --max-parents=0 HEAD)..HEAD`
   Also run: `!git log --stat --no-merges $(git describe --tags --abbrev=0 2>/dev/null || git rev-list --max-parents=0 HEAD)..HEAD`

   If a specific range was given in $ARGUMENTS, use that range instead.

2. **Apply the writing style guidelines above.** If none are set, write concise user-facing prose grouped by impact.

3. **Group changes into categories** (use only categories that have entries):
   - **Breaking Changes** — anything backwards-incompatible
   - **New Features** — user-visible additions
   - **Bug Fixes** — defects corrected
   - **Performance** — measurable improvements
   - **Deprecations** — features that will be removed in a future version
   - **Internal / Developer** — refactors, tests, tooling

4. **Rewrite commit messages as user-facing prose.** Translate technical shorthand into plain English. Focus on what changed and why it matters, not what files were touched.

5. **Format as [Keep a Changelog](https://keepachangelog.com) style**, adapted to the chosen documentation library's syntax for callouts and formatting.

6. **Write to the confirmed output path.** If prepending to an existing file, preserve all existing content.
