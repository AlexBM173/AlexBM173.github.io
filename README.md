# Personal Academic Website

Personal website for Dr. Alex Placeholder — Postdoctoral Researcher in Observational Cosmology.

## Structure

```
personal-site/
├── index.html              ← Homepage
├── publications.html       ← Publications list (to build)
├── blog.html               ← Blog (to build)
├── cv.html                 ← CV page (to build)
├── outreach.html           ← Outreach page (to build)
├── assets/
│   ├── css/
│   │   └── style.css       ← All styles
│   ├── js/
│   │   └── main.js         ← Nav + scroll animations
│   └── images/
│       ├── headshot.jpg    ← Replace placeholder with actual headshot
│       └── cover.jpg       ← Replace placeholder cover image
├── .nojekyll               ← Disables Jekyll on GitHub Pages
└── README.md
```

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `username.github.io` for a user site, or any name for a project site).
2. Push this folder's contents to the `main` branch.
3. Go to **Settings → Pages** and set the source to **Deploy from a branch → main → / (root)**.
4. Your site will be live at `https://username.github.io` (user site) or `https://username.github.io/repo-name` (project site).

## Customising

### Replace placeholder content
- **Name & title**: Search for `Alex Placeholder` / `A·P` across all files.
- **Headshot**: Add `assets/images/headshot.jpg` and in `index.html` replace the `.headshot-placeholder` div with:
  ```html
  <img src="assets/images/headshot.jpg" alt="Dr. Your Name" class="headshot-img" />
  ```
  Then in `style.css` add `.headshot-img { width: 128px; height: 128px; border-radius: 50%; border: 3px solid var(--accent); object-fit: cover; }`.
- **Cover image**: Add `assets/images/cover.jpg` and in `style.css` update `.hero-cover` to include `background-image: url('../images/cover.jpg'); background-size: cover; background-position: center;`.
- **Links**: Update all `href="mailto:..."`, `href="https://github.com/..."`, and `href="https://linkedin.com/in/..."` values.
- **Timeline entries**: Edit dates, roles, and descriptions in the `#timeline` section of `index.html`.
- **Projects**: Edit the four project cards in the `#projects` section.

### Adding new pages
Each future page (publications, blog, cv, outreach) should:
1. Start with the same `<nav>` and end with the same `<footer>`.
2. Link back `<link rel="stylesheet" href="assets/css/style.css" />`.
3. Use the same `.section` / `.section-inner` structure for consistent layout.

## Fonts used
- **DM Serif Display** — headings (Google Fonts)
- **Instrument Sans** — body text (Google Fonts)
- **DM Mono** — labels, dates, monospace elements (Google Fonts)
