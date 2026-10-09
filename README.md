# sarva-portfolio

Personal portfolio built with [Zola](https://www.getzola.org) — a Rust-based static site generator.

## Setup

### 1. Install Zola

**macOS (Homebrew):**
```bash
brew install zola
```

**Windows:**
Download the binary from https://github.com/getzola/zola/releases and add to PATH.

**Linux:**
```bash
# Snap
snap install zola --edge

# Or download binary from GitHub releases
```

### 2. Run locally

```bash
zola serve
```

Visit http://127.0.0.1:1111

### 3. Build for production

```bash
zola build
```

Output goes into the `public/` directory.

## Deploy to Vercel

Settings in the Vercel dashboard:

- Framework Preset: **Other**
- Build Command: `zola build`
- Output Directory: `public`
- Zola version: pinned by `ZOLA_VERSION` in `vercel.json` (currently 0.19.2)

`vercel.json`:
```json
{
  "build": {
    "env": {
      "ZOLA_VERSION": "0.19.2"
    }
  }
}
```

## Add your resume PDF

Place your resume PDF at:
```
static/resume.pdf
```

It will be served at `/resume.pdf`.

## Project structure

```
sarva-portfolio/
├── config.toml          # Site config
├── vercel.json          # Pins ZOLA_VERSION
├── CLAUDE.md            # Standing rules for contributors / AI agents
├── sass/
│   └── main.scss        # All styles
├── templates/           # base, index, posts, projects, about, resume
├── content/             # Front matter only; each page picks its template
└── static/
    ├── resume.pdf       # Served at /resume.pdf
    └── photos/          # About-page carousel (slide1-10.jpg)
```

## Conventions

See [CLAUDE.md](CLAUDE.md) for stack constraints, design tokens and the per-task workflow.
