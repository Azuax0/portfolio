# Mattéo Binet — Portfolio

Responsive bilingual portfolio showcasing Mattéo Binet’s pre-MSc developer/sysadmin profile.  
Built with plain **HTML**, **Materialize CSS**, and custom styling that mirrors the digital résumé on `digitalresume.html`.

## Highlights

- **Hero / About** sections mixing full-stack development and infrastructure experience.
- **Portfolio grid** with modal deep-dives (APC22, plugins, job board, AI experiments, automation projects).
- **French ↔ English toggle** (header + mobile sidenav) – all copy is stored in data attributes for instant language switches.
- **Contact section** with actionable links and a styled form ready for integration.
- **Neon glass UI** with consistent typography, chip tags, and Material Icons.

## File Structure

```text
index.html          # Main portfolio page
digitalresume.html  # Detailed résumé (linked from “Voir le CV numérique”)
style.css           # Global styles + responsive breakpoints
desktop.css         # (Optional) legacy split stylesheet – not referenced
tablet.css          # (Optional) legacy split stylesheet – not referenced
mobile.css          # (Optional) legacy split stylesheet – not referenced
photo.jpg           # Hero portrait
photo_n2.jpg        # About section portrait
readme.txt          # Documentation for the standalone digital résumé
README.md           # This document
```

> Only `style.css` is required for the current build. The `desktop/tablet/mobile.css` files remain for reference if you wish to reintroduce split stylesheets.

## Tech Stack

- **HTML5** semantic layout
- **Materialize 1.x** (CDN) for grid, cards, nav, modals, sidenav
- **CSS3** with `clamp()`, `grid`, `flex`, and custom neon glass effects
- **JavaScript** (inline in `index.html`) for:
  - Materialize component initialisation
  - IntersectionObserver reveal animations
  - Language switch handling

## Getting Started

1. Clone or download the repository.
2. Open `index.html` in a modern browser (Chrome, Firefox, Edge).
3. Click “Voir le CV numérique” to open the complementary résumé page.

No build step or dev server is required.

### Optional: Serve Locally

```bash
# Any static server works; here’s one example with Python
python -m http.server 8080
open http://localhost:8080/index.html
```

## Customisation Tips

- **Content**: Edit copy inside `index.html`. French/English strings live near the bottom in the `translations` object.
- **Projects**: Update the portfolio cards and corresponding modals. Each modal is keyed by `id` (e.g., `project-jobboard`).
- **Branding**: Tweak colors, shadows, radii, fonts in `style.css`. The neon identity is centralised under `.neon-bg`, `.glass`, `.chip-glow`, etc.
- **Resume link**: Replace `digitalresume.html` or point to an external PDF if preferred.

## Responsive Behaviour

The layout adapts to three core breakpoints:

- **≤ 520 px**: Mobile-first layout, sidenav menu, full-width buttons, centered hero.
- **521 – 1023 px**: Tablet tweaks—header stacks brand, nav, and language toggle without wrapping; two-column hero; tightened card spacing.
- **≥ 1024 px**: Desktop grid with expanded spacing, large hero portrait, and multi-column portfolio.

Additional `clamp()` font sizing keeps headings legible across widths.

## Accessibility & UX Considerations

- High-contrast neon glass palette with consistent iconography.
- Keyboard-friendly language toggle buttons (`aria-pressed`).
- Smooth scrolling and reveal animations (disabled via `prefers-reduced-motion`).
- Nav anchor targets include `scroll-margin-top` to avoid fixed-nav overlap.

## Deployment

Host on any static platform (Netlify, GitHub Pages, Vercel static export).  
Ensure assets remain in the same directory relative to `index.html`.

## Versioning & Maintenance

- Commit changes frequently with focused messages (content, styling, assets).
- Document major updates (new project, design shift) in this README so collaborators understand the context.

---

Questions or feedback? Reach out via the contact links in the hero section.  
Mattéo Binet © 2024
