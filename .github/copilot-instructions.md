# Project Guidelines

## Stack

- Use Zola, pinned to `0.19.2` in `vercel.json`.
- Use hand-written SCSS in `sass/main.scss`.
- Use vanilla JavaScript inline in the templates.
- Do not add JavaScript frameworks, dependencies, or build tooling.

## Design

- Use the existing CSS variables in `sass/main.scss`: `--bg` for the background, `--accent` for the primary accent, `--accent-text` for accent text, `--muted` for muted text, `--font-mono` (`'Geist Mono', 'Courier New', monospace`) for body text, and `--font-serif` (`'Instrument Serif', Georgia, serif`) for headings. Reuse other existing variables such as `--text`, `--border`, `--surface-pill`, `--surface-soft`, `--surface-hover`, and `--border-hover` where applicable.
- Never hardcode colours or font stacks; use the existing CSS variables.
- Use Geist Mono for body text and Instrument Serif for headings.
- Preserve the text-first design.
- Do not change the visual design unless the task explicitly says to.
- Do not add cards, icons, or colours unless the task explicitly names them.

## Content and data

- Pages are `templates/*.html` plus `content/*.md` front matter containing `title` and `description`.
- Projects and posts are hardcoded in their templates.
- Read emails, social links, coordinates, and the OG image path from `config.extra`; never hardcode them in templates.
- Read the production URL from `config.base_url`, currently `https://thesarvatarshan.vercel.app`.

## Workflow

- Create one branch per task, named `type/short-name` using `feat/`, `fix/`, or `chore/`.
- Never commit to `main`.
- Start every task with `git fetch --prune`, then branch from `origin/main`.
- Make one commit per task with a clear message.
- Before finishing, run `zola build` with the local Zola version and with Zola `0.19.2` downloaded to `/tmp`; never add the downloaded binary to the repository.
- Fix build errors and warnings before finishing.
- Stay in scope. Report problems outside the task in the final report instead of fixing them.

## Quality

- Maintain WCAG AA contrast: at least 4.5:1 for normal text.
- Provide a visible `:focus-visible` outline on every interactive element.
- Respect `prefers-reduced-motion`.
- Ensure layouts work at 375px, 600px, 768px, and 1280px without horizontal scrolling.
- The sidebar becomes the top bar at 600px.
- Rendered pages cannot be viewed in this workflow. For visual changes, state exactly what to eyeball on the Vercel preview and at which widths; never claim a visual check that was not performed.

## Report format

- Report files changed.
- Report what was verified and how.
- Report what was skipped and why.
- Report anything that needs a decision.
