# os-guide

A beginner-to-interview study guide for **Operating Systems** — foundational concepts, worked examples, and a 50-question interview Q&A set — published as a single self-contained website.

> Author: **Lakshmi Priya Anbu**
> © 2026. All rights reserved.

---

## 🔗 Live site

**[https://lakshmipriyaanbu.github.io/os-guide/](https://lakshmipriyaanbu.github.io/os-guide/)**

The site is served by GitHub Pages directly from this repository's `main` branch. It is publicly accessible — no login required.

---

## What's in the guide

The site is a single HTML page (`index.html`) organized into fifteen chapters:

| # | Chapter |
|---|---|
| 01 | What is an Operating System? |
| 02 | Types of Operating Systems |
| 03 | Kernel, User Mode, System Calls |
| 04 | Processes |
| 05 | Threads |
| 06 | CPU Scheduling |
| 07 | Process Synchronization |
| 08 | Deadlocks |
| 09 | Memory Management |
| 10 | Virtual Memory |
| 11 | File Systems |
| 12 | I/O and Disk Scheduling |
| 13 | Advanced Topics (virtualization, RTOS, containers) |
| 14 | Interview Q&A (50 questions with answers) |
| 15 | Glossary |

Design notes:

- Serif display type (Charter / Georgia) for headings, sans-serif for body text.
- Warm-neutral paper background with a study-blue accent and a terracotta callout hue.
- ASCII diagrams inline throughout for portability.
- Interview questions use `<details>` cards — click a question to reveal the answer.
- Subtle diagonal `© Lakshmi Priya Anbu 2026` watermark repeated across the page.

---

## Repository layout

```
os-guide/
├── index.html   ← the entire site (self-contained, no external assets)
└── README.md    ← this file
```

That's the whole thing. `index.html` inlines all CSS and content — no JavaScript, no external fonts, no image files. It renders identically on every modern browser (macOS, Windows, Linux, iOS, Android).

---

## How to modify the site

### Small edits (typo, one section)

1. Open [`index.html`](./index.html) in your editor of choice (VS Code, Nano, etc.).
2. Find the section you want to change (each `<h2>` marks a chapter).
3. Make the edit.
4. Commit and push:

   ```bash
   cd ~/Desktop/os-guide
   git add index.html
   git commit -m "Fix typo in Virtual Memory section"
   git push
   ```
5. GitHub Pages will redeploy automatically within about a minute.

### Bigger changes (add a new chapter, restructure)

1. Edit `index.html` — the file is organized top-to-bottom in reading order.
2. To add a new chapter: copy an existing `<h2 id="chXX">` block, adjust its ID, and add a matching entry to the sidebar TOC (`<nav class="toc">`) and to the Contents block near the top.
3. To adjust styling: edit the `<style>` block at the top of the file.
4. Preview locally before pushing:

   ```bash
   open ~/Desktop/os-guide/index.html   # macOS
   # or on any OS: just double-click index.html
   ```
5. When happy, commit and push as above.

### Changing the watermark

Locate the `body::before` block near the top of the `<style>` element in `index.html`. The SVG text inside the `background-image` URL is what shows on the page. Edit that string to change the watermark text; adjust `fill-opacity` (currently `0.06`) to change how faint or bold it is.

---

## Local development

No build step. No dependencies. Just open the file:

```bash
# Preview in a browser
open ~/Desktop/os-guide/index.html    # macOS
xdg-open index.html                   # Linux
start index.html                      # Windows
```

Or, if you want to serve it locally over HTTP (useful for testing hash-links):

```bash
cd ~/Desktop/os-guide
python3 -m http.server 8000
# then open http://localhost:8000/
```

---

## Publishing

The site is deployed by **GitHub Pages** from the `main` branch, root path.

- **Source branch:** `main`
- **Source folder:** `/` (root)
- **Deploy trigger:** any push to `main` triggers a rebuild.
- **URL:** https://lakshmipriyaanbu.github.io/os-guide/

Deployment status can be checked at [Actions › pages-build-deployment](https://github.com/LakshmiPriyaAnbu/os-guide/actions).

To change these settings: repo **Settings → Pages**.

---

## Contributing

This is a personal study guide. If you want to suggest a correction, feel free to open an issue or a pull request.

---

## License

Content © 2026 **Lakshmi Priya Anbu**. All rights reserved.

The site is free to read; please do not republish substantial portions without permission.
