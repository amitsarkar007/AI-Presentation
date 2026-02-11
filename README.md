# AI 101 Presentation (Repute InfoSystems)

A `reveal.js` presentation that introduces AI fundamentals and practical AI usage in software delivery.

## Overview

- **Deck title:** AI 101
- **Audience:** Repute InfoSystems teams
- **Presenter:** Amit Sarkar
- **Primary source files:** `index.html` and `css/custom.css`

## Tech Stack

- `reveal.js` for slide rendering/navigation
- `http-server` for local hosting
- Static assets (images and logos) in `assets/images/`

## Prerequisites

- Node.js 18+ (recommended)
- npm

## Run Locally

1. Install dependencies:

```bash
npm install
```

2. Start the local server:

```bash
npm run start
```

3. Open:

`http://localhost:8080/`

## Project Structure

```text
AI-Presentation/
├── index.html              # Slide content and Reveal initialization
├── css/
│   └── custom.css          # Theme/style overrides
├── assets/
│   └── images/             # Slide visuals and company logos
├── package.json
└── README.md
```

## Editing Guide

- Add/update slides in `index.html` inside `<div class="slides">`.
- Reveal is initialized at the bottom of `index.html` in `Reveal.initialize(...)`.
- Any slide with `data-hide="true"` is removed at runtime by this script:
  - `document.querySelectorAll(".slides section[data-hide='true']").forEach((slide) => slide.remove());`
- Use `css/custom.css` for visual changes (spacing, typography, cards, colors, layout helpers).

## Script

- `npm run start`: serves the project at port `8080` with no caching (`http-server -c-1 -p 8080 .`)

## Notes

- This project is a static deck; there is no build step.
- Most slide images are local files in `assets/images/`.