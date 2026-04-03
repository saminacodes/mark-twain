# mark-tw(ai)n

Your technical writing co-pilot.

## Skills

### Write

| Command | What it does |
|---|---|
| `/write-readme` | Generate a README for the current project |
| `/write-changelog` | Write a changelog or release notes from git history |
| `/write-tutorial` | Write a step-by-step tutorial or how-to guide |

### Edit

| Command | What it does |
|---|---|
| `/edit` | Edit docs for clarity, link quality, and style |
| `/edit-accessibility` | Edit docs for device-agnostic language, alt text, and heading hierarchy |
| `/edit-brevity` | Edit docs to remove filler words and tighten prose |

## Setup

1. Copy this repo's `.claude/` directory into your project root (or [symlink it](https://www.man7.org/linux/man-pages/man1/ln.1.html)).
2. Open the project in Claude Code — skills are available immediately as slash commands.

## Customizing writing style

Each skill file contains a **Writing Style & Guidelines** section with placeholder comments. Replace the comments with your own voice, tone, audience, and formatting rules. (Placeholders use HTML comment syntax (`<!-- ... -->`), so they have no effect until you fill them in.)

## Credits

Inspiration for this project is sourced from:

- [Auth0 writing guidelines](https://auth0.com/docs/customize/integrations/marketplace-partners/writing-tips-for-installation-guides)
- [Strategic Writing for UX](https://www.oreilly.com/library/view/strategic-writing-for/9781492049388/)
- [The Product is Docs]()
