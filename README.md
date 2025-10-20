# BDtronics Lab — Static Site Starter (EN)

A minimal static website for **BDtronics Lab** (Flexible Sustainable Electronics).

## What is what (plain words)
- **Hero**: the first section at the top of the Home page that explains who you are and has buttons (calls to action).
- **Favicon**: the tiny icon in the browser tab.
- **Open Graph image**: the preview image used by social networks when someone shares your link.
- **Design tokens**: reusable values (colors, spacing, etc.) used across the CSS so styles stay consistent.
- **GitHub Pages**: free hosting integrated in GitHub for static sites.
- **Workflow**: a small automation that deploys the site to GitHub Pages every time you push changes.

## Structure
```
assets/
  favicon.svg
  logo.svg            # replace with your final SVG
  logo-negative.png   # light-on-dark variant
  og-image.png        # social preview image
index.html
robots.txt
sitemap.xml
.github/workflows/pages.yml
LICENSE
README.md
```

## Local preview (optional)
Open `index.html` in a browser or run a tiny server:
```bash
python3 -m http.server 8080
```
Then open http://localhost:8080

## Publish on GitHub Pages
With the GitHub CLI:
```bash
gh repo create bdtronicslab-site --public --source . --remote origin --push
```
Or manually:
```bash
git init
git add .
git commit -m "feat: first commit for bdtronicslab site (EN)"
git branch -M main
git remote add origin https://github.com/<ORG_OR_USER>/bdtronicslab-site.git
git push -u origin main
```
Then in GitHub → **Settings → Pages** set **Build and deployment** to **GitHub Actions**. The included `pages.yml` will deploy automatically.

## Customize
- Replace placeholder images in `assets/`.
- Update texts in `index.html` (Hero title, Research areas, contacts).
- Change `og:url` in the `<head>` to your real domain if you have one.

## Accessibility & performance tips
- Keep good color contrast for text.
- Export the logo as **SVG with text converted to paths** for consistent rendering.
- Use **WebP** images and reasonable sizes.
