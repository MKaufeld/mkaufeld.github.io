# Personal Website Template

A clean, minimal, and fully responsive single-page personal website template — ideal for researchers, academics, and developers who want to share their publications, projects, and talks online.

- **Live demo (with content):** [korbinianmoller.github.io](https://korbinianmoller.github.io/) *(the original site this template is based on)*
- **Live demo of the empty template:** [Try it yourself!](https://korbinianmoller.github.io/personal_website_template/)

---

## Features

- **Zero build step** — pure HTML, CSS, and vanilla JavaScript. Just edit and deploy.
- **Responsive** — looks great on desktop, tablet, and mobile.
- **Sticky navigation bar** — with a hamburger menu on small screens.
- **Publication cards with modals** — each paper gets a full-detail popup with abstract, authors, venue, links, and a one-click BibTeX copy button.
- **Badge system** — mark papers or talks as `RECENTLY PUBLISHED` or `UPCOMING` with a single CSS class.
- **Smooth scrolling** — custom eased scroll animation for all anchor links.
- **Scroll-to-top button** — appears automatically after scrolling, adapts color in the footer zone.
- **Auto-updating copyright year** — the footer year is set by JavaScript, so it stays current.
- **No dependencies** — only CDN-loaded Google Fonts and Font Awesome (no npm, no bundler).
- **Easy theming** — all colors are defined as CSS variables in `styles.css`.

---

## Quick Start

### 1. Use this template

Click **Use this template** on GitHub (or fork/clone this repository):

```bash
git clone https://github.com/korbinianmoller/personal_website_template.git my-website
cd my-website
```

### 2. Customize `index.html`

Open `index.html` in any text editor. Every section that needs your input is marked with a `<!-- CUSTOMIZE: ... -->` comment. Work through them top to bottom:

| What to change | Where to find it |
|---|---|
| Page title & meta description | `<head>` section, top of file |
| Nav bar name & links | `<nav class="site-nav">` block |
| Your name & tagline | Hero section (`<header class="hero">`) |
| Social links (LinkedIn, Email, etc.) | Hero section & About section |
| Bio text | About section |
| Publication cards | Publications section |
| Publication modals (abstract, BibTeX, …) | Modal blocks below the publications section |
| Project cards | Projects section |
| Talk / teaching cards | Talks section |
| Footer name & copyright | Footer element |

### 3. Replace your profile photo

Add your photo to the `images/` folder and update the `<img>` tag in the hero section:

```html
<img src="images/profile.jpg" alt="Profile picture">
```

Any common web image format works (`.jpg`, `.png`, `.webp`). The image is cropped to a circle — a square photo with your face centered works best.

### 4. Add your papers (optional)

For each publication:

1. **Add a card** in the Publications section — copy an existing `<article class="card">` block and update the title, author summary, and `data-modal-target` ID.
2. **Add the matching modal** further down the page — copy an existing modal block and update all the fields (title, authors, venue, abstract, links, BibTeX).
3. Place the PDF in the `paper/` folder and link to it, or link to an external URL.
4. Place the teaser image in `images/` and reference it in the modal.

### 5. Deploy to GitHub Pages

1. Push your repository to GitHub.
2. Go to **Settings → Pages**.
3. Set **Source** to `main` branch, `/ (root)` folder.
4. Your site will be live at `https://yourusername.github.io/` (or your custom domain).

---

## File Structure

```
personal_website_template/
├── index.html          ← Main page (edit this)
├── styles.css          ← All styles; tweak CSS variables for theming
├── images/
│   ├── profile.svg     ← Replace with your own photo (profile.jpg, etc.)
│   ├── paper1-teaser.png   ← Teaser images for your publications
│   └── ...
├── paper/              ← (optional) PDFs of your papers
│   └── your-paper.pdf
├── LICENSE
└── README.md
```

---

## Theming

All colors are CSS custom properties at the top of `styles.css`. Change any value there to retheme the entire site instantly — no find-and-replace needed.

```css
:root {
    --color-primary:        #374151;   /* gray-700  — headings, outline buttons     */
    --color-secondary:      #2563eb;   /* blue-600  — highlights, card titles       */
    --color-accent:         #1d4ed8;   /* blue-700  — darker blue accent            */
    --color-dark:           #1f2937;   /* gray-800  — footer, dark buttons          */
    --color-light:          #ffffff;
    --color-bg-hero:        #f9fafb;   /* gray-50   — hero section background       */
    --color-bg-light:       #ffffff;
    --color-bg-pubs:        #f3f4f6;   /* gray-100  — publications background       */
    --color-bg-projects:    #ffffff;
    --color-bg-talks:       #f3f4f6;   /* gray-100  — talks section background      */
    --color-bg-card-dark:   #f3f4f6;   /* gray-100  — dark-variant card background  */
}
```

> **Tip:** also update `<meta name="theme-color">` in `index.html` to match `--color-dark` so the mobile browser chrome picks up your brand color.

---

## Navigation Bar

The sticky navigation bar is included by default. There are two ways to disable it:

**Option A — hide with the `hidden` attribute** (easiest, keeps the HTML for later):

```html
<nav class="site-nav" id="site-nav" hidden>
```

**Option B — delete it entirely**: remove the full `<nav>…</nav>` block from `index.html`.

To customize the links shown in the nav, edit the `<ul class="nav-links">` list and keep the `href` values in sync with the `id` attributes on each `<section>`.

---

## Card Badge Reference

Add a CSS class to the `<article>` element to show a status badge:

| Class | Badge shown |
|---|---|
| `class="card"` | No badge |
| `class="card new"` | `RECENTLY PUBLISHED` (blue) |
| `class="card upcoming"` | `UPCOMING` (blue) |

---

## Disclaimer

This template was built for personal use and shared as-is for anyone who finds it helpful. It is **not** intended to be a production-grade, fully polished, or security-hardened product. In particular:

- There may be bugs, edge cases, or browser inconsistencies that have not been tested or fixed.
- No guarantees are made about accessibility compliance, SEO completeness, or performance optimization.
- The template loads Font Awesome and Google Fonts from third-party CDNs — if you have strict privacy or content-security requirements, you may want to self-host those assets.
- No active maintenance or issue support is promised.

Use it as a starting point, adapt it freely, and fix what does not fit your needs.

That said, if you spot a bug, have an idea for an improvement, or want to contribute a fix, feel free to open an issue or submit a pull request — contributions are always welcome. You can also reach out directly via the contact details on [korbinianmoller.github.io](https://korbinianmoller.github.io/).

---

## License

This template is released under the **MIT License** — see [LICENSE](LICENSE) for details.
You are free to use, modify, and distribute it for any purpose, personal or commercial.
A credit in the footer is appreciated.

---

## Credits

Template designed and originally developed by **Korbinian Moller**.

- Original site: [korbinianmoller.github.io](https://korbinianmoller.github.io/)
