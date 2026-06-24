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
   - `.views-count` — the view count number

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which publishes the site to GitHub Pages automatically. Enable Pages once in the repo settings: **Settings → Pages → Source → GitHub Actions**.
