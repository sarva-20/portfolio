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

1. Push this repo to GitHub
2. Import in Vercel → New Project
3. Set Framework Preset to **Other**
4. Set Build Command: `zola build`
5. Set Output Directory: `public`
6. Deploy

### vercel.json (already included):
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

## Add certifications later

Edit `templates/about.html` — there's a commented section ready for certifications.

## Project structure

```
sarva-portfolio/
├── config.toml          # Site config
├── sass/
│   └── main.scss        # All styles
├── templates/
│   ├── base.html        # Layout with sidebar
│   ├── index.html       # Home page
│   ├── posts.html       # Posts page (Medium links)
│   ├── projects.html    # Projects page
│   ├── about.html       # About page
│   └── resume.html      # Resume page
├── content/
│   ├── _index.md
│   ├── about.md
│   ├── resume.md
│   ├── posts/
│   │   └── _index.md
│   └── projects/
│       └── _index.md
└── static/
    └── resume.pdf       # ← drop your PDF here
```
