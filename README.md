# Personal Website Template

A clean, minimal, and fully responsive single-page personal website template — ideal for researchers, academics, and developers who want to share their publications, projects, and talks online.

- **Live:** [MKaufeld.github.io](https://MKaufeld.github.io/)

## Quick Start

### 1. Clone this template


```bash
git clone https://github.com/korbinianmoller/personal_website_template.git my-website
cd my-website
```

### 2. Replace your profile photo

Add your photo to the `images/` folder and update the `<img>` tag in the hero section:

```html
<img src="images/profile.jpg" alt="Profile picture">
```

Any common web image format works (`.jpg`, `.png`, `.webp`). The image is cropped to a circle — a square photo with your face centered works best.

### 3. Add your papers (optional)

For each publication:

1. **Add a card** in the Publications section — copy an existing `<article class="card">` block and update the title, author summary, and `data-modal-target` ID.
2. **Add the matching modal** further down the page — copy an existing modal block and update all the fields (title, authors, venue, abstract, links, BibTeX).
3. Place the PDF in the `paper/` folder and link to it, or link to an external URL.
4. Place the teaser image in `images/` and reference it in the modal.

### 4. Deploy to GitHub Pages

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


## Disclaimer

This template was built for personal use and shared as-is for anyone who finds it helpful. It is **not** intended to be a production-grade, fully polished, or security-hardened product. In particular:

- There may be bugs, edge cases, or browser inconsistencies that have not been tested or fixed.
- No guarantees are made about accessibility compliance, SEO completeness, or performance optimization.
- The template loads Font Awesome and Google Fonts from third-party CDNs — if you have strict privacy or content-security requirements, you may want to self-host those assets.
- No active maintenance or issue support is promised.

## License

This template is released under the **MIT License** — see [LICENSE](LICENSE) for details.
You are free to use, modify, and distribute it for any purpose, personal or commercial.
A credit in the footer is appreciated.


