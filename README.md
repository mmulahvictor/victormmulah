# Victor Mmulah — Personal Portfolio

> *"The entire goal of education is to transform mirrors into windows."*
> — Sydney J. Harris

A personal portfolio website for **Victor Mmulah** — ICT Officer, full-stack software developer, EdTech builder, open-source contributor, writer, and cyclist from Kisumu, western Kenya.

---

## Live Preview

Open `victor-mmulah.html` directly in any modern browser. No build step, no dependencies, no server required.

---

## About This Project

This is a single-file, zero-dependency HTML portfolio built with a strong editorial-magazine aesthetic rooted in the colours and character of western Kenya — laterite clay, Lake Victoria blues, savanna greens, and deep ink tones.

It documents Victor's full career journey, technical skills, active projects, published writing, open-source contributions, and the person behind the code.

---

## Features

| Feature | Details |
|---|---|
| **Pinned navigation** | Fixed top nav with glassmorphism blur, active section highlighting, and mobile hamburger menu |
| **Scroll progress bar** | Clay-to-gold gradient bar at the very top of the page |
| **Scroll-driven animations** | Sections and timeline items fade/slide in as you scroll |
| **Back-to-top button** | Appears after 400px scroll, smooth-scrolls back to hero |
| **Custom cursor** | Trailing clay dot + ring; expands on hover over links |
| **Animated hero grid** | Subtle drifting grid lines in the hero background |
| **Marquee tech band** | Scrolling ticker of skills and affiliations |
| **Responsive layout** | Mobile-optimised grid collapses, burger menu, adjusted padding |
| **Print stylesheet** | Clean print layout with hidden decorative elements |
| **Accessibility** | Skip-to-content link, ARIA labels, semantic HTML, proper heading hierarchy |
| **SEO & Open Graph** | Full meta tags, OG tags, Twitter Card, theme-color |
| **Proper entity encoding** | All special characters use HTML entities (no encoding issues) |

---

## Sections

1. **Hero** — Full-screen introduction with animated name, tagline, and CTAs
2. **Stats band** — Five key metrics at a glance
3. **About** — Career narrative, guiding philosophy, and personal context
4. **Journey** — Chronological career timeline from Maseno University to present
5. **Skills** — Six technical domain cards with tag clouds
6. **Projects** — Four active projects at Edutab Africa
7. **Writing** — Nine Medium articles with clickable links
8. **Open Source** — R-Instat contribution history and collaborators
9. **Beyond Code** — The cyclist, the historian, and hobby grid
10. **Character** — Four personality trait cards based on observed patterns
11. **Contact** — Links to Medium, email, and GitHub

---

## Design System

### Aesthetic Direction

The portfolio uses a **glassmorphism / frosted-glass** design language inspired by the Devoryn workspace UI — translucent cards with blur, cyan glow accents, ambient orb backgrounds, and a floating app-like feel. It functions as a single-page application (SPA) with a persistent sidebar and section switching, closely mirroring a real-world product dashboard.

### Colour Palette

| Variable | Hex | Usage |
|---|---|---|
| `--bg-deep` | `#070d1a` | Page background |
| `--bg-mid` | `#0d1628` | Card inner backgrounds |
| `--bg-card` | `rgba(255,255,255,0.055)` | Glass card surfaces |
| `--cyan` | `#00D4FF` | Primary accent, active states, glows |
| `--blue` | `#4A9EFF` | Secondary accent |
| `--green` | `#00E5A0` | Success, open source |
| `--orange` | `#FF8C42` | In-progress, mobile |
| `--red` | `#FF5C7A` | Errors, alerts |
| `--purple` | `#B06AFF` | Bootcamp, inclusion |
| `--text-1` | `#F0F4FF` | Primary text |
| `--text-2` | `#9AAFC8` | Body / secondary text |
| `--text-3` | `#5A7290` | Muted labels |
| `--glass-border` | `rgba(0,212,255,0.18)` | Card borders |

### Typography

| Role | Font | Weight |
|---|---|---|
| All UI text | Outfit | 300, 400, 500, 600, 700, 800, 900 |
| Code labels / mono | Space Mono | 400, 700 |

All fonts loaded from Google Fonts via `<link>` preconnect.

### Breakpoints

- **960px** — Two-column grids collapse to single column, burger menu replaces nav links

---

## File Structure

```
victor-mmulah.html    # Complete single-file portfolio
README.md             # This file
```

Everything lives in one HTML file — styles, markup, and scripts. No frameworks, no build tools, no package.json.

---

## Customisation Guide

### Updating contact links

Search for the `#contact` section and update the `href` values:

```html
<a href="https://medium.com/@mmulahvictor" ...>Read on Medium</a>
<a href="mailto:mmulahvictor@gmail.com" ...>Email Victor</a>
<a href="https://github.com/mmulahvictor" ...>GitHub</a>
```

### Updating Medium article links

Each article card in the `#writing` section is a proper `<a>` tag pointing to `https://medium.com/@mmulahvictor`. Replace with specific article URLs as they become available.

### Adding a new timeline entry

Copy an existing `.timeline-item` block and update the year, title, org, description, and badge colours:

```html
<div class="timeline-item">
  <div class="timeline-dot" style="background:#YOUR_COLOR;"></div>
  <div class="timeline-year">2026</div>
  <div class="timeline-body">
    <h3>New Role or Achievement</h3>
    <span class="org">Organization · Location</span>
    <p>Description of what happened and why it matters.</p>
    <span class="badge badge-moss">Tag</span>
  </div>
</div>
```

### Badge colour classes

| Class | Colour | Use for |
|---|---|---|
| `badge-clay` | Clay orange | Industry work, bootcamps |
| `badge-moss` | Forest green | EdTech, open source |
| `badge-lake` | Lake blue | Academic, inclusion programs |
| `badge-gold` | Gold | Present / current status |

### Adding a skill card

Copy a `.skill-card` block inside `.skills-grid` and update the icon character, name, description, and tags.

### Colour variable overrides

All colours are defined as CSS custom properties in `:root`. Override them to retheme the entire site:

```css
:root {
  --clay: #YOUR_BRAND_COLOR;
  --ink: #YOUR_BACKGROUND;
}
```

---

## Browser Support

Tested and functional in:

- Chrome / Chromium 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Uses: CSS Grid, CSS Custom Properties, `IntersectionObserver`, `backdrop-filter`, `clamp()`. All modern baseline features with no polyfills needed for current browsers.

---

## Performance Notes

- **No JavaScript frameworks** — vanilla JS only
- **No external scripts** — all JS is inline
- **One external CSS dependency** — Google Fonts (3 families)
- **No images** — all visuals are pure CSS (gradients, geometry, noise via SVG data URI)
- **Single HTTP request after fonts** — the entire page is one file

---

## Deployment

Since this is a single HTML file, deployment is trivial:

### GitHub Pages
```bash
# Create a repo, push the file as index.html
cp victor-mmulah.html index.html
git init && git add . && git commit -m "Initial portfolio"
git remote add origin https://github.com/USERNAME/USERNAME.github.io
git push -u origin main
```

### Netlify / Vercel drop
Drag and drop `victor-mmulah.html` into the Netlify Drop interface at `app.netlify.com/drop`. Live in seconds.

### Custom domain (any static host)
Rename to `index.html`, upload via FTP/SFTP or your host's file manager. No server-side processing required.

---

## About Victor Mmulah

**Victor Mmulah** is a Kenyan full-stack software developer and ICT Officer based in Kisumu, western Kenya. He works at Edutab Africa building the GoLearn educational platform, contributes to the R-Instat open-source statistics project, and publishes developer guides and cultural essays on Medium.

- 📍 Kisumu, Kenya
- 🎂 Born February 8
- 💼 ICT Officer at Edutab Africa
- 🛠 JavaScript · React · Ruby on Rails · Flutter · Moodle
- 📝 [medium.com/@mmulahvictor](https://medium.com/@mmulahvictor)
- 📧 mmulahvictor@gmail.com
- 🐙 [github.com/mmulahvictor](https://github.com/mmulahvictor)

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| `1.0` | 2025 | Initial build — editorial magazine aesthetic (clay/bone palette, Playfair Display) |
| `1.1` | 2025 | Improved contrast ratios; pinned nav with glassmorphism; mobile hamburger |
| `1.2` | 2025 | Added Projects section; expanded hobby grid; birthday chip; Character/Personality section |
| `1.3` | 2025 | Scroll progress bar; back-to-top button; skip link; OG/meta tags; article links; print stylesheet |
| `2.0` | 2025 | **Full redesign** — Glassmorphism/frosted-glass aesthetic inspired by Devoryn workspace UI. SPA architecture with persistent sidebar navigation. Cyan/blue glow accents. Ambient orb backgrounds. Donut charts, Gantt timeline, animated progress bars. Nine sections: Dashboard, About, Journey, Projects, Skills, Writing, Open Source, Beyond Code, Character, Contact |

---

*Built with care. Rooted in western Kenya.*
