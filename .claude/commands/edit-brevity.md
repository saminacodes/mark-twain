Edit documentation files within this repo for consistency, clarity, and style.

## What to do

$ARGUMENTS

**Argument forms:**
- *(no arguments)* — ask the user which files to edit before proceeding
- `all` — edit every `.md` and `.mdx` file in the repo (excluding `node_modules`, `.git`, `.claude`)
- A file path (e.g. `README.md`, `docs/api.md`) — edit that specific file
- A glob pattern (e.g. `docs/**/*.md`) — edit all matching files
- A file path + instruction (e.g. `README.md fix the link text`) — edit that file with a specific focus

If no arguments are given, ask: "Which files should I edit — all docs, or specific ones?"

---

## Editing Rules

1. 