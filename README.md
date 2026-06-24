# madebyzpriv portfolio

Static HTML/CSS portfolio site. No build step, no JS.

## Folder structure

```
index.html              the whole site
assets/css/style.css    all styling
assets/img/             thumbnail/poster images for videos
videos/tiktok/          drop TikTok video files here
videos/instagram/       drop Instagram video files here
```

## Adding a new video

1. Drop the video file into `videos/tiktok/` or `videos/instagram/` (e.g. `tiktok-4.mp4`).
2. Optionally drop a cover image into `assets/img/` (e.g. `tiktok-4-thumb.jpg`).
3. In `index.html`, copy one of the existing `<article class="video-card">` blocks in the matching section and paste it below the others.
4. Update the copy:
   - `src="videos/tiktok/tiktok-4.mp4"` — path to the file you dropped in
   - `poster="assets/img/tiktok-4-thumb.jpg"` — path to the cover image (or remove the `poster` attribute to skip it)
   - `<h3>` — video title
   - `.tag` — client or niche, e.g. "Coffee shop"
   - `.views-count` — the view count number (this shows in the badge over the video)

## Other things you can fill in

All of these live in `index.html`:

- **Hero stats** — the `10M+`, `30+`, `2` numbers in the `.hero-stats` block. Update `.stat-num` / `.stat-label`.
- **About photo** — drop a photo at `assets/img/about.jpg` and it appears automatically. No file = a styled placeholder shows instead.
- **Testimonials** — copy a `<blockquote class="quote-card">` block to add more client quotes. Fill in the quote, `.quote-name`, and `.quote-role`.
- **Social links / email** — update the TikTok, Instagram, and `mailto:` links in the contact section and footer (search for `madebyzpriv` / `hello@madebyzpriv.com`).
- **Marquee** — the scrolling niche list near the top is in the `.marquee` block. Keep both copies in sync so the loop stays seamless.

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which publishes the site to GitHub Pages automatically. Enable Pages once in the repo settings: **Settings → Pages → Source → GitHub Actions**.
