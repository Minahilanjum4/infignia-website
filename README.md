# Infignia — Cambridge O Level & A Level Tuition Website

A responsive, multi-page business website for **Infignia**, a Cambridge (CAIE) O Level and A Level
tuition academy teaching Mathematics, the Sciences, Economics and Computer Science.

Built for the Week 2 practical task: a **static HTML5 + CSS3 site**, no frameworks and no JavaScript.
Design direction: an "insignia / result-slip" motif — the site's signature illustration is a stylised
Cambridge result slip, tying the brand name (*Infignia* → *insignia*) directly to the subject matter
(grades, achievement, certification).

---

## 🔗 Live Site & Repository

- **Live demo:** https://minahilanjum4.github.io/infignia-website/
- **Repository:** https://github.com/Minahilanjum4/infignia-website

---

## 📄 Pages

| Page             | Sections                                                                 |
|------------------|---------------------------------------------------------------------------|
| `index.html`     | Hero, Features ("Why Infignia"), Course preview, Testimonials, CTA, Footer |
| `about.html`     | Company overview, Mission & Vision, Team members                          |
| `services.html`  | 8 course/service cards, Batch pricing plans                               |
| `contact.html`   | Contact form, Google Maps embed, Contact info, Social links               |

Every page shares the same header (logo, nav links with an active-page indicator, dark-mode toggle,
CSS-only mobile hamburger menu) and footer (sitemap links, course links, contact snippet, social icons).

---

## 📁 Project Folder Structure

```
infignia/
├── index.html
├── about.html
├── services.html
├── contact.html
├── css/
│   └── style.css
├── images/
│   ├── logo.svg                 # nav / footer brand mark
│   ├── hero-illustration.svg    # signature "result slip" hero graphic
│   └── about-illustration.svg   # About page illustration
├── assets/
│   └── grid-pattern.svg         # decorative background texture
└── README.md
```

---

## 🛠️ Technical Requirements — how they were met

- **HTML5 & CSS3** — semantic tags throughout (`header`, `nav`, `main`, `section`, `article`, `footer`).
- **External CSS** — a single `css/style.css`, linked from every page, organised into numbered sections
  with comments.
- **Flexbox** — navbar, buttons, footer columns, info rows, hero actions.
- **CSS Grid** — feature/course/pricing/testimonial/team grids, the contact page's two-column layout.
- **Media queries** — mobile-first breakpoints at `768px`, `1024px`, `1440px`, matching the brief's
  375 / 768 / 1024 / 1440 target widths.
- **CSS variables** — a full design-token system in `:root` (colour, radius, shadow, spacing, type),
  re-mapped for dark mode.
- **Clean folder structure & well-commented code** — see above; every CSS section is labelled and every
  HTML file uses matching comment markers.
- **No Bootstrap, no Tailwind, no JavaScript** — the mobile menu and the dark-mode toggle are both pure
  CSS, using the checkbox + `:checked` / `:has()` technique rather than any script.

---

## 🌙 Bonus Challenges Completed

This build completes **three** optional bonus challenges:

1. **Responsive hamburger navigation menu, CSS-only** — a hidden checkbox + `<label>` pattern drives the
   mobile nav; no JavaScript involved.
2. **CSS animations and hover effects** — card lift-on-hover, button hover states, and a hero fade-up
   animation (`@keyframes float-in`), all respecting `prefers-reduced-motion`.
3. **Dark mode using CSS variables** — the toggle switch in the navbar is a checkbox; `body:has(#theme-toggle:checked)`
   re-declares the design tokens for a dark palette. (Relies on the modern `:has()` selector — supported
   in current Chrome, Edge, Safari and Firefox; on older browsers the toggle simply has no visual effect.)

Also included as an extra: a **Batch Plans pricing section** on the Services page (Standard / Focused /
Private tiers).

---

## 📱 Responsive Testing

Verified at the four required widths:

- Mobile — 375px
- Tablet — 768px
- Laptop — 1024px
- Desktop — 1440px+

---

## 🎨 Design Credit

Layout and section rhythm closely follow the chosen "Startup Website" Figma Community template:
a gradient hero, an about "collage" section, a partner/resources strip, two alternating image+text
"goal" sections with floating stat cards, an icon-tile services grid, star-rated testimonial cards,
a cream stats strip, and a gradient CTA banner above the footer. The palette (deep violet gradient +
lavender accent + cream stats strip), typography (Fraunces/Manrope), copy, and all illustrations were
built from scratch for the Infignia brand — the template itself uses stock photography and placeholder
Lorem Ipsum copy, which have been replaced throughout with original SVG illustrations and real
Infignia content.

---

## 📸 Screenshots

Save your screenshots into a `screenshots/` folder inside this project, using the filenames below
(the images will then show up automatically here on GitHub).

### Home
![Home — Desktop](screenshots/home-desktop.png)
![Home — Mobile](screenshots/home-mobile.png)

### About
![About — Desktop](screenshots/about-desktop.png)
![About — Mobile](screenshots/about-mobile.png)

### Services
![Services — Desktop](screenshots/services-desktop.png)
![Services — Mobile](screenshots/services-mobile.png)

### Contact
![Contact — Desktop](screenshots/contact-desktop.png)
![Contact — Mobile](screenshots/contact-mobile.png)

---

## 🚀 Running Locally

No build step required — it's a static site.

1. Download or clone the folder.
2. Open `index.html` directly in a browser, **or** serve it locally for the most accurate experience:
   ```bash
   npx serve .
   # or
   python -m http.server 8000
   ```
3. Visit the printed local address in your browser.

---

## ✅ Notes for Submission

- The contact form currently posts to `#` (no backend attached) — wire it up to a form service
  (e.g. Formspree) or your own backend endpoint when deploying, or leave as a static demo.
- Replace the placeholder phone/email/address/social links with Infignia's real details before going live.
- Run a Lighthouse audit after deployment and optimise any large exported screenshots before committing
  them, to keep the Performance score at 90+.
