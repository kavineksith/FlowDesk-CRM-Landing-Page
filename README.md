# FlowDesk CRM — Landing Page

A small responsive landing page built for the CenoDigital Web Developer Intern assignment.

---

## How to View Locally

No build tools or server needed for viewing. Just:

1. Download or unzip the project folder
2. Open **`index.html`** in any modern browser (Chrome, Firefox, Edge, Safari)

That's it — the page works straight from the file system.

> **Want to edit the styles?**
> Edit `style.scss`, then compile it to `style.css` using:
> ```bash
> npm install -g sass        # one-time install
> sass style.scss style.css  # compile
> ```
> Or use the **Live Sass Compiler** extension in VS Code for auto-compile on save.

---

## What I Built

| Section | Choice |
|---|---|
| Hero | Product name, headline, value prop, CTA button |
| Supporting Section | **Key Features** — three feature cards |
| Interactive Feature | **FAQ accordion** (native `<details>`/`<summary>`) + **Smooth scroll** via CSS `scroll-behavior: smooth` |

Both interactive features work with **zero JavaScript** — smooth scroll is a single CSS rule on `<html>`, and the FAQ uses the browser's built-in `<details>` element.

---

## What I Prioritised and Why

**Semantic HTML first.**
I used `<nav>`, `<section>`, `<article>`, `<footer>`, `<details>`, and `<summary>` instead of generic `<div>`s everywhere. This improves accessibility and makes the code easier to read at a glance.

**No JavaScript.**
The brief required an interactive feature. I chose a CSS + native HTML approach: smooth scroll is just `scroll-behavior: smooth` on `html`, and the FAQ accordion is the built-in `<details>` element — no JS at all. This keeps the page fast, simple, and easy to maintain.

**Clean SCSS structure.**
The SCSS is split into clearly labelled sections with comments (Variables → Reset → Utilities → Components → Responsive). Variable names like `$primary` and `$muted` make colours easy to update in one place.

**Mobile-first responsive layout.**
The hero and feature grid stack vertically on screens below 768px using CSS Grid and a single `@media` block.

---

## What I Would Improve with More Time

- **Animations** — add subtle CSS `@keyframes` entrance animations on scroll using the `Intersection Observer` API or pure CSS `animation-timeline`.
- **Waitlist form** — add the email input with CSS-only `:invalid`/`:valid` state styling for front-end validation feedback.
- **Dark mode** — a simple CSS `prefers-color-scheme` media query would toggle the colour variables.
- **More sections** — a "Who It's For" audience section and a pricing table would round out a real marketing page.
- **Performance** — lazy-load the Unsplash hero image with `loading="lazy"` and use `srcset` for different screen sizes.

---

*Submitted by Kavin Eksith — CenoDigital Web Developer Intern Task, May 2025*
