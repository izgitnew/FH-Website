# Juliana Henao — Life Coach Website

## Overview
Single-page static website for Juliana Henao, a life coach and holistic therapist based in Metro Atlanta serving bilingual Hispanic women. Built as a single `index.html` file with embedded CSS and JS — no build tools, no frameworks.

## Language
The entire site is in **Spanish**. All UI text, headings, CTAs, labels, meta tags, and aria attributes are in Spanish. Testimonials are real client quotes in Spanish. Do not introduce English text.

## Tech Stack
- Single `index.html` with embedded `<style>` and `<script>`
- Google Fonts: Playfair Display, Source Sans 3, DM Sans
- No build tools, no npm, no frameworks
- Deployed via GitHub Pages (`.github/workflows/pages.yml`)
- GitHub repo: https://github.com/izgitnew/FH-Website

## Key Design Decisions
- **No cards**: Sections use border separators, flowing text, and asymmetric grids instead of card containers
- **Minimal animations**: Only 3 elements have scroll-reveal (about photo, quote, video embed). Duration 0.45s, translateY 18px. Respects `prefers-reduced-motion`.
- **Real content only**: Real photos of Juliana, real client testimonials (Spanish), real YouTube embeds, real social links
- **Footer is lean**: 2 columns (Brand + Conectar). No nav duplication — the fixed nav already provides section links.
- **External links**: "Agenda tu sesión" and "Obtener la guía" link to julianahenaolifecoach.com. "Únete por WhatsApp" links to wa.link/atw69s.

## Images
- `juliana-hero.jpg` — Main portrait (hero section)
- `juliana-author.jpg` — Candid laughing photo (about section)
- `guide-cover.jpg` — 30 Días de Amor Propio guide cover (offerings thumbnail)
- `avatar-nancy.jpg`, `avatar-lina.jpg`, `avatar-monica.jpg` — Cropped client avatars (testimonials)
- `juliana-class.jpg` — Downloaded but not currently used

## Section IDs
- `#about` — Sobre mí
- `#services` — Trabaja conmigo (offerings)
- `#podcast` — Videos (YouTube section, CSS class is still `.podcast`)
- `#stories` — Testimonios
- `#newsletter` — Newsletter signup

## Common Gotchas
- The video section uses CSS class `.podcast` (legacy naming) but the section is for YouTube videos
- Newsletter form is front-end only — no backend. Submission hides the form and shows a success message with a "Suscribir otro correo" recovery link.
- Nav active state is tracked via IntersectionObserver on section IDs
