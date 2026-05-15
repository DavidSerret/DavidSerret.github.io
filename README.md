<div align="center">

# davidserret.github.io

**Personal portfolio — [davidserret.github.io](https://davidserret.github.io)**

![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![WebGL](https://img.shields.io/badge/WebGL2-990000?style=flat&logo=webgl&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=flat&logo=github&logoColor=white)

</div>

---

<!-- Replace with actual screenshot: screenshots/portfolio.png -->
<!-- ![Portfolio screenshot](screenshots/portfolio.png) -->

## Overview

Static portfolio site with no build step or dependencies. Features a WebGL2 black hole renderer in the hero — a port of the [Gargantua shader](https://www.shadertoy.com/view/lstSRS) with a 4-pass HDR bloom pipeline and temporal anti-aliasing, running entirely in the browser.

## Stack

- **Rendering** — WebGL2, GLSL ES 3.0, 4 framebuffer passes, RGBA16F HDR
- **Bloom** — Mipmap tree + separable Gaussian blur + HDR composite (`color *= 200.0`)
- **TAA** — Temporal anti-aliasing via ping-pong framebuffers
- **Layout** — Vanilla HTML/CSS, CSS custom properties, `clamp()` fluid typography
- **Font** — DM Mono + Inter via Google Fonts
- **Hosting** — GitHub Pages, zero CI needed

## Deploy

```bash
# 1. Push index.html to main
git add index.html && git commit -m "update" && git push

# 2. GitHub Pages auto-deploys from main → / (root)
# Live at https://davidserret.github.io in ~60 seconds
```

## Add avatar

Save a photo as `avatar.png` in the repo root — the `<img>` tag loads it automatically with an `onerror` fallback placeholder. No code changes needed.

```
repo root/
├── index.html
├── avatar.png     ← drop here
└── screenshots/   ← optional, for README
```

---

<div align="center">
  <a href="https://davidserret.github.io">Live ↗</a> · <a href="https://github.com/DavidSerret">@DavidSerret</a>
</div>
