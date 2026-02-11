# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

De-Silo landing page — a single-file static site (`index.html`) for collecting beta signup emails. Korean-language UI targeting non-technical founders who want to validate ideas quickly with AI.

## Tech Stack

- **Single `index.html`** — no build step, no bundler, no package manager
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) — not a local install
- **Pretendard** font from Google Fonts
- **No JavaScript framework** — vanilla JS with one inline `handleSubmit()` function

## Development

Open `index.html` directly in a browser or use any static file server:

```bash
python3 -m http.server 8000
# or
npx serve .
```

There is no build, lint, or test command.

## Architecture

Everything lives in `index.html`:
- Sections: Hero (nav + headline + CTAs) → Features (`#features`) → CTA/email signup (`#cta`) → Footer
- Email form currently has no backend — `handleSubmit()` just shows a success message and resets the form
- Styling uses Tailwind utility classes with a dark purple/pink gradient theme (`gray-900`, `purple-900`)

## Conventions

- All user-facing text is in Korean
- Design uses `rounded-full` buttons, `backdrop-blur` glass cards, gradient text via `bg-clip-text text-transparent`
