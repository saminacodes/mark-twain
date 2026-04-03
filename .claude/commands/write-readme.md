Generate a README for the current project.

## What to do

$ARGUMENTS

Arguments can be:
- *(no arguments)* — generate a full README for the current project with file name `README.md`
- A specific section (e.g. `"installation"`, `"api reference"`) — write only that section
- A file path + section (e.g. `docs/getting-started.md introduction`) — write to a specific file

**Before writing, check if a `README.md` already exists at the root. If it does, ask whether to overwrite it or save the new file elsewhere. Otherwise, default to `README.md` at the project root.**

---

## Writing Style & Guidelines

> Fill in this section with your preferences. Delete any headings that don't apply.

**Voice & Tone**
<!-- e.g. "Direct and professional. No marketing language." -->

**Audience**
<!-- Who is the primary reader? e.g. "Backend engineers new to this library" -->

**Terminology**
<!-- Preferred terms or terms to avoid. -->

**Prohibited phrases**
<!-- e.g. "Never use 'simply', 'just', 'easy', 'straightforward'" -->

**Format preferences**
<!-- e.g. "Sentence case headings. Oxford comma. Numbered lists for steps." -->

---

## Instructions

1. **Understand the project first.** Read the codebase structure, existing docs, and package files before writing. Check for `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`, or equivalent to understand the project name, description, and dependencies.

2. **Apply the writing style guidelines above.** If none are set, default to clear, direct prose for an experienced developer who is new to this project.

3. **Follow this structure:**
   - One-line description (what it does)
   - Why it exists / problem it solves (2–4 sentences)
   - Quick start / installation (the minimum to get something working)
   - Usage with real, runnable examples
   - Configuration / options (if applicable)
   - Contributing (if applicable)
   - License

4. **Write to the confirmed output path.** If improving an existing file, edit it rather than replacing it wholesale.
