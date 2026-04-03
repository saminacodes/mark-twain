Edit documentation files within this repo for accessibility.

## What to do

$ARGUMENTS

**Argument forms:**
- *(no arguments)* — ask the user which files to edit before proceeding
- `all` — edit every `.md` and `.mdx` file in the repo (excluding `node_modules`, `.git`, `.claude`)
- A file path (e.g. `README.md`, `docs/api.md`) — edit that specific file
- A glob pattern (e.g. `docs/**/*.md`) — edit all matching files

If no arguments are given, ask: "Which files should I edit — all docs, or specific ones?"

---

## Accessibility Rules

1. Make sure all instructions or directions are device agnostic.

    **Use:**
    - Select
    - Switch
    - Locate
    - Choose
    - Open
    - Close
    - Navigate to
    - View
    - Enter (text)
    - Search
    - Confirm
    - Cancel

    **Avoid (replace with the above):**
    - Click
    - Right-click
    - Double-click
    - Hover / Mouse over
    - Drag
    - Scroll
    - Swipe
    - Pinch / Spread
    - Tap
    - Long-press
    - Press
    - Type
    - Key in

2. Make sure all images have descriptive alternative text.

3. Make sure each page has at least one H1 or `#` at the beginning of the text for page hierarchy. Make sure all following headers use logical heading hierarchy and do not skip levels (h1 → h2 → h3).

4. 