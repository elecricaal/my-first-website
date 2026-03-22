# My Web Development Learning Roadmap

## Context
I am a senior UX designer learning web development. I have experience with design but limited programming experience (took programming in my master's degree). I am learning to use VS Code, GitHub Copilot Chat, and the Terminal.

## Current Project
A 2-page HTML website with a solid CSS foundation:
- `hello.html` — Homepage with a card, h1, and a button that navigates to the second page
- `second.html` — Second page with a card, h1, and a back button
- `style.css` — Shared external stylesheet with a full design system

## Tech Stack
- HTML5 (with viewport meta tag for responsive support)
- CSS3 (external stylesheet `style.css` — design tokens, typography, color theme, card, button, responsive breakpoints)
- Vanilla JavaScript (minimal, used for navigation)

---

## Roadmap

### Step 1 — Shared CSS file + CSS Foundation
**Goal:** Move duplicate button styles into a single `style.css` file and build a solid CSS foundation.  
**Concept:** External stylesheets, DRY principle, design tokens, responsive design.  
**Status:** Completed  
**What was built:**
- `style.css` created — inline styles removed from both pages, button class unified to `.btn`
- **CSS Variables (Design Tokens)** — all colors, spacing, typography, border-radius, and transitions defined as variables in `:root`, mirroring Figma tokens
- **Google Font** — Inter loaded via `@import`, weights 400/500/600/700
- **Typography scale** — 7-step font size scale (12px–48px), weight and line-height variables, `h1`–`h3` and `p` pre-styled
- **Color theme** — 4 semantic groups: Primary (blue shades), Neutral (background/surface/border), Text (primary/secondary/inverse), Feedback (success/warning/error)
- **Spacing scale** — 6-step scale from 4px to 48px based on a 4px grid
- **Card component** — white surface card with border, shadow, and padding using theme tokens
- **Responsive design** — 2 breakpoints: tablet ≤1024px (card 80% width, smaller headings), mobile ≤480px (card full screen, body font never below 16px)
- **Viewport meta tag** — added to both HTML files (required for media queries to work on real devices)

### Step 2 — Git (Version control)
**Goal:** Track changes so I can always go back to a working version.  
**Commands to learn:**
```bash
git init
git add .
git commit -m "my first commit"
```
**Concept:** Version control, commit history, snapshots.  
**Status:** Completed  
**What was done:**
- `git init` — initialized a Git repository (`.git` folder created)
- `git config --global user.name / user.email` — set Git identity (name: Carel8i)
- `git add .` — staged all 6 project files
- `git commit -m "first commit: HTML pages and CSS foundation"` — saved first snapshot on branch `main` (commit `0c7f165`)
**Ask Copilot:**
- *"Set up Git for my project step by step"*
- *"Explain what git init, git add, and git commit do"*
- *"What is the difference between git add and git commit?"*
- *"I made a mistake, how do I go back to my last commit?"*

### Step 3 — GitHub (Cloud backup + sharing)
**Goal:** Push the project to GitHub for backup and to share work.  
**Concept:** Remote repositories, push/pull, collaboration.  
**Status:** Not started  
**Ask Copilot:**
- *"How do I push my project to GitHub for the first time?"*
- *"Explain the difference between Git and GitHub"*
- *"What is a remote repository?"*
- *"Walk me through creating a GitHub repo and connecting it to my local project"*

### Step 4 — Layout & real content
**Goal:** Design and build a real page layout.  
**Concepts to learn:**
- CSS Flexbox and Grid
- Semantic HTML (`<nav>`, `<section>`, `<footer>`, `<header>`)
**Status:** Not started  
**Ask Copilot:**
- *"Add a navigation bar with links to both pages"*
- *"What is flexbox and show me an example in my CSS"*
- *"What is the difference between flexbox and CSS Grid?"*
- *"Add a footer to both pages using semantic HTML"*
- *"Restructure my HTML to use proper semantic tags like header, main and footer"*

### Step 5 — Publish live with GitHub Pages
**Goal:** Put the website on the internet for free.  
**Concept:** Static site hosting, GitHub Pages, deployment.  
**Status:** Not started  
**Ask Copilot:**
- *"How do I publish my site with GitHub Pages?"*
- *"What files do I need to have ready before deploying to GitHub Pages?"*
- *"My GitHub Pages site is not updating after I pushed — why?"*

### Step 6 — JavaScript interactivity
**Goal:** Add real interactivity — animations, form validation, dynamic content.  
**Concept:** DOM manipulation, event listeners, functions.  
**Status:** Not started  
**Ask Copilot:**
- *"Explain what the JavaScript on my button does"*
- *"Add a smooth fade-in animation when the page loads"*
- *"Add a contact form with basic validation to my page"*
- *"What is the DOM and how does JavaScript interact with it?"*
- *"Show me how to write a JavaScript function that changes the button color on click"*

## Lessons Learned
- **Viewport meta tag is mandatory** — without `<meta name="viewport">` in the HTML `<head>`, mobile browsers render at desktop width and media queries never trigger
- **`align-items` on the parent constrains children** — `body { align-items: center }` prevents a child from stretching to full width even with `width: 100%`; override it at the breakpoint
- **Media query breakpoints must match actual device widths** — iPad Air is 820px, so a `max-width: 768px` breakpoint won't apply to it; use 1024px to cover all tablets
- **Never go below 16px for body text** — it's the browser default and the accessibility floor

---

## How I Use GitHub Copilot

| I want to...        | I say...                                              |
|---------------------|-------------------------------------------------------|
| Build something     | "Add a navigation bar with links to both pages"       |
| Understand code     | "Explain what this CSS does"                          |
| Fix a bug           | "This button isn't working, why?"                     |
| Learn a concept     | "What is flexbox and show me an example"              |
| Review my work      | "Is there anything wrong with my HTML?"               |

**Key tip:** Be specific and use UX language. Instead of "make it look nice", say "center the text and add 24px spacing between elements."

---

## Notes & Progress Log
_Use this section to track what you've learned and any blockers._

- [x] Step 1 — Shared CSS + full CSS foundation
- [ ] Step 2 — Git setup
- [ ] Step 3 — GitHub push
- [ ] Step 4 — Layout & content
- [ ] Step 5 — GitHub Pages
- [ ] Step 6 — JavaScript
