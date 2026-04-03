Write a step-by-step tutorial or how-to guide.

## What to do

$ARGUMENTS

Arguments can be:
- A topic or title (e.g. `"how to set up authentication"`)
- A topic + audience (e.g. `"deploying to AWS for first-time users"`)
- A file path + topic (e.g. `docs/tutorials/auth.md "setting up OAuth"`)

If no arguments are given, ask: "What is the tutorial about, and who is the audience?"

**Before writing, ask the user:**

1. **Where should the file be saved?**
   - If a path was provided in $ARGUMENTS, confirm it.
   - Otherwise ask for the output path (e.g. `docs/tutorials/getting-started.md`).

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

   Adapt all callouts, steps, tabs, and code blocks to the correct syntax for the chosen library.

---

## Writing Style & Guidelines

> Fill in this section with your preferences. Delete any headings that don't apply.

**Voice & Tone**
<!-- e.g. "Encouraging and clear. Written for beginners." -->
<!-- e.g. "Direct and efficient. Assume the reader is experienced." -->

**Audience**
<!-- Who is this tutorial for? What should they already know going in? -->

**Terminology**
<!-- Preferred terms or terms to avoid. -->

**Prohibited phrases**
<!-- e.g. "Never use 'simply', 'just', 'easy', 'straightforward'" -->

**Format preferences**
<!-- e.g. "Each step must have a code example. Use numbered lists for steps." -->
<!-- e.g. "End with a 'Next steps' section linking to related docs." -->

---

## Instructions

1. **Understand the topic first.** Read any relevant source files, existing docs, or examples in the codebase before writing. Run `!find . -name "*.md" -not -path "*/node_modules/*" -not -path "*/.git/*"` to discover existing docs that may provide context.

2. **Apply the writing style guidelines above.** If none are set, write in clear, direct prose — device-agnostic language, no filler words, no assumptions about mouse or keyboard input.

3. **Follow this structure:**
   - Title (imperative verb: "Set up X", "Deploy to Y", "Configure Z")
   - Introduction: what the reader will accomplish and what they need to know beforehand (prerequisites)
   - Steps: numbered, each with a clear action, code example, and expected result
   - Verification: how to confirm it worked
   - Troubleshooting: 2–4 common errors and how to fix them (if applicable)
   - Next steps: links to related tutorials or reference docs

4. **Use device-agnostic language.** Prefer: Select, Choose, Navigate to, Enter, Open. Avoid: Click, Type, Press, Tap, Hover.

5. **Adapt formatting to the chosen documentation library.** Use that library's component syntax for steps, callouts, code tabs, and warnings.

6. **Write to the confirmed output path.**
