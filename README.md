# Math Roadmap Interactive

Interactive **Math Mastery Roadmap** to track your journey from foundations to calculus, complex variables, Laplace transforms, and linear algebra.  
It includes a **Flowchart view** and a **Skill Tree view**, with **prerequisite locking**, **click-to-complete nodes**, **auto-saved progress**, **export/import**, and a **print-ready** layout — all in a single HTML file.

> Live demo (when deployed to GitHub Pages): `https://<your-username>.github.io/math-roadmap-interactive/`

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Quick Start](#quick-start)
- [Deploy to GitHub Pages](#deploy-to-github-pages)
- [What’s Inside](#whats-inside)
- [Curriculum Graph](#curriculum-graph)
- [Customize](#customize)
- [Privacy](#privacy)
- [Accessibility](#accessibility)
- [Tech Stack](#tech-stack)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Credits](#credits)

---

## Features

- **Two visual modes:** Flowchart + Skill Tree
- **Prerequisite locking:** Topics unlock only when their prerequisites are completed
- **One-click progress:** Click nodes or checklist items to toggle completion
- **Auto-save:** Progress stored in your browser’s `localStorage`
- **Export / Import:** Save or restore progress as a JSON file
- **Print mode:** Clean, white-paper layout for wall-print tracking
- **Zero dependencies:** Pure HTML/CSS/JS — no frameworks, no build tools

---

## Screenshots

Add an image to show the UI:

```
assets/screenshot.png
```

(You can take a screenshot after opening `index.html` in your browser and place it in `assets/`.)

---

## Quick Start

```bash
git clone https://github.com/<your-username>/math-roadmap-interactive.git
cd math-roadmap-interactive

# Ensure the main file is named index.html
# Open it locally:
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

- Check boxes or click nodes to **complete** topics.
- Locked topics are dim until **all prerequisites** are complete.
- Use **Export / Import / Reset** buttons (top right) to manage progress.
- Use **Print** for a clean poster view.

---

## Deploy to GitHub Pages

1. Initialize and push to GitHub:

```bash
git init
git add .
git commit -m "feat: add interactive math roadmap"
git branch -M main
git remote add origin https://github.com/<your-username>/math-roadmap-interactive.git
git push -u origin main
```

2. Enable Pages:

- GitHub → **Settings** → **Pages**
- **Build and deployment** → **Source: `Deploy from a branch`**
- **Branch:** `main` and **Folder:** `/ (root)`
- Save. Your site will be available at:
  ```
  https://<your-username>.github.io/math-roadmap-interactive/
  ```

---

## What’s Inside

- `index.html` — the entire app (UI, styles, logic) in **one** file  
- `assets/screenshot.png` — optional preview image (add your own)

> If your file is currently `math-roadmap.html`, rename it to `index.html` for GitHub Pages.

---

## Curriculum Graph

**Level 1 — Foundations**  
Arithmetic → Algebra Basics → Coordinate Geometry → Trigonometry Basics

**Level 2 — Pre-Calculus**  
Advanced Algebra → Sequences & Series → Analytic Geometry → Trigonometry Advanced → Limits & Continuity

**Level 3 — Calculus Core**  
Differentiation → Integration → Multivariable Calculus

**Level 4 — Complex & Laplace**  
Complex Numbers → Complex Functions → Laplace Transforms

**Level 5 — Linear Algebra**  
Matrices → Systems of Linear Equations → Vector Spaces → Eigenvalues & Eigenvectors

**Level 6 — Probability & Statistics**  
Probability Basics → Statistics Foundations

> The dependency graph is defined in the `TOPICS` array inside `index.html`.

---

## Customize

Open `index.html` and look for:

- **Topics & prerequisites:** edit the `TOPICS` array (each topic has `id`, `label`, `level`, `prereq: []`)
- **Node positions:** adjust `FLOW_POS` and `SKILL_POS` (SVG coordinates) for layout
- **Colors / radius / shadows:** tweak the `:root` CSS variables
- **Storage key:** update `STORAGE_KEY` (`math-roadmap-progress.v1`) if you change topic IDs

**Tips**
- Keep topic **IDs stable** to preserve saved progress
- If you add nodes, place them in both `FLOW_POS` and `SKILL_POS`

---

## Privacy

- All progress is kept **locally** in your browser via `localStorage`
- No analytics, no external calls, no cookies
- Use **Export** to back up progress as a `.json` file

---

## Accessibility

- High-contrast color states for **Locked / Unlocked / Done**
- Large click targets in the checklist and on SVG nodes
- Keyboard-friendly via the left-side checklist

---

## Tech Stack

- **Vanilla** HTML + CSS + JavaScript
- **SVG** for Flowchart & Skill Tree
- **No build** tools, **no dependencies**

---

## Roadmap

- Keyboard navigation and focus outline for SVG nodes
- Search / filter topics
- Multiple progress profiles (e.g., Beginner / Fast-Track)
- Time tracking & CSV export
- Dark mode toggle

---

## Contributing

1. Fork the repo and create a feature branch:

```bash
git checkout -b feat/improve-skill-layout
```

2. Make your changes, then:

```bash
git commit -m "feat: improve skill tree node spacing"
git push origin feat/improve-skill-layout
```

3. Open a Pull Request with a clear description and a screenshot.

---

## License

MIT © <your-name>

---

## Credits

Built for learners who want a **visual, prerequisite-aware** way to master university math — from fundamentals to advanced topics — with no setup and no distractions.
