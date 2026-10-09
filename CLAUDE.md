# Standing rules

- Stack: Zola 0.19.2, hand-written SCSS (`sass/main.scss`), vanilla JS. No JS frameworks, no new dependencies, no build tooling additions.
- Design tokens: bg `#f9f9f7`, accent `#e85c2c`, Geist Mono body, Instrument Serif headings. Do not change visual design unless the task says so.
- Every task:
  - Work on its own branch. Never commit directly to main.
  - Run `zola build` and fix any warnings/errors before finishing.
  - Check layouts at 375px, 768px and 1280px widths.
  - One commit per task, with a clear message.
- Do not touch files outside the task's scope. If you notice other problems, list them in your final report instead of fixing them.
- Final report format: files changed, what was verified, anything skipped and why.
