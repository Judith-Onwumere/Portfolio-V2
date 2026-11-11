# Judith Onwumere · Portfolio

A static portfolio site (plain HTML, CSS and JavaScript). No build step and no dependencies.

## Structure

```
index.html            Main page (hero, case studies, toolbox, experience, certificates, about, contact)
case.html             Case study viewer, used inside index.html and also shareable on its own
assets/css/style.css  Styles for index.html
assets/js/main.js     Behaviour for index.html (intro, curved text, elevator, inventory, certificates)
assets/img/           All images (WebP), plus og-image.jpg for link previews
favicon.svg, 404.html, robots.txt, vercel.json, .nojekyll
```

Share a single case study directly with `case.html?c=<slug>`, where the slug is `keys`, `lazy-stash`, `rateam`, `adqua` or `petrol-advisory`.

## Run locally

Open `index.html` in a browser. For the case study overlay, use a local server so the page can load `case.html`:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000

## Put it on GitHub

```
git init
git add .
git commit -m "Add portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Host it

**GitHub Pages:** repo Settings → Pages → Deploy from a branch → `main` / root. The site appears at `https://<your-username>.github.io/<repo-name>/`. All paths are relative, so it works from a sub-folder URL.

**Vercel:** Add New Project → import the repo → Framework Preset "Other" → leave build and output settings empty → Deploy.

**Netlify:** Add new site → import from Git → leave build command empty, publish directory `.` → Deploy.

## Before you go live

1. **Social preview image.** `assets/img/og-image.jpg` is a 1200x630 snapshot of the hero section. `index.html` already points to it at `https://judith-onwumere-v2.vercel.app/assets/img/og-image.jpg`. If you change domain, update the `og:image` and `twitter:image` tags. Sites like LinkedIn and X cache previews, so use their post inspector or card validator to refresh after you deploy.
2. **CV link.** The CV buttons point to a Google Drive download link. For a more reliable link, add your PDF to `assets/` and point the link to it.
3. **Custom domain.** Add it in your host's settings. Nothing in the code needs to change.
4. **Email.** The contact buttons use onwumerejudith@gmail.com. Search for it in `index.html` and `assets/js/main.js` if it ever changes.

Fonts (Bricolage Grotesque, Newsreader, Press Start 2P) load from Google Fonts.
