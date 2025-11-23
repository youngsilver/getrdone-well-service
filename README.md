# GET'R'DONE Well Service Website

Professional water well services website for Central Oklahoma featuring a faith-driven mission and responsive design.

## Features

- 🎥 Full-screen video background hero section (ready for your video)
- 📱 Mobile-first responsive design
- ✨ Shimmering scripture overlay (John 7:38)
- 🔧 Service showcase (Drilling, Pump Repair, Water Testing)
- ⭐ Customer testimonials
- 🙏 Faith-driven mission statement
- 📞 Multiple call-to-action buttons
- ♿ Accessibility features

## Quick Start

1. Open `index.html` in a web browser to view the site
2. The site is fully functional with an animated CSS water background

## Adding Your Video Background

Want to add a hand-in-water video to the hero section?

👉 **See [VIDEO_SETUP.md](VIDEO_SETUP.md) for complete instructions**

Quick steps:
1. Create a `videos` folder
2. Add your video as `hand-in-water.mp4`
3. Uncomment the video source lines in `index.html`

The site works perfectly without a video using the animated CSS background!

## Files

- `index.html` - Main website structure
- `styles.css` - Responsive styles and animations
- `script.js` - Interactive features (navigation, scroll effects)
- `VIDEO_SETUP.md` - Complete video setup guide
- `.gitignore` - Excludes large video files from Git

## Technologies

- Pure HTML5, CSS3, and JavaScript
- No frameworks or dependencies required
- Mobile-first responsive design
- CSS animations for water effect
- Intersection Observer API for scroll animations

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Video background with fallback support

## License

This website operates under Christ-centered principles, dedicated to the glory of God and service of His people.

---

"Whatever you do, work at it with all your heart, as working for the Lord." — Colossians 3:23*


## Deployment

This repository includes a GitHub Actions workflow that publishes the site to GitHub Pages. It supports two environments so you can develop without overwriting the production site:

- Production: triggered when pushing to `main`. Publishes the site at the repository root to the `gh-pages` branch (served as the main site).
- Preview: triggered for other branches and pull requests. Publishes a preview under `gh-pages` in the `previews/<ref>/` subfolder so each branch/PR gets an isolated preview.

Workflow path: `.github/workflows/deploy.yml`

How it works:

1. Push changes to `main` to update production (example: `git add .; git commit -m "Deploy site"; git push origin main`).
2. Push to other branches or open/update a pull request to get a preview deployment.
3. The preview is published under `gh-pages/previews/<ref>` where `<ref>` is either `pr-<number>` for PR previews or a sanitized branch name for branch previews.

Preview URL examples:

- Project site production: `https://<username>.github.io/<repository>/`
- Preview for `feature/foo` branch: `https://<username>.github.io/<repository>/previews/feature-foo/`
- Preview for PR #7: `https://<username>.github.io/<repository>/previews/pr-7/`

Notes:

- If Pages doesn't appear automatically after the first deploy, enable Pages in Settings -> Pages and choose the `gh-pages` branch.
- Change `publish_dir` in `.github/workflows/deploy.yml` if you add a build step (for example `dist/`).
- The workflow uses the repository `GITHUB_TOKEN` so no extra secrets are required.

If you'd like, I can also:

- Add a CNAME step for custom domains.
- Change preview naming (timestamped previews, or include commit SHA).
- Add automatic cleanup of older previews.

