# sketch-a-score

Static site, no build step. Everything is in this folder.

## Files
- index.html — the whole app
- manifest.webmanifest, sw.js, icon-*.png, apple-touch-icon.png, favicon.svg — "install as app" + offline
- og.png — link-preview image
- robots.txt

## Deploy (pick one)
- Netlify: app.netlify.com/drop, drag this folder in.
- Cloudflare Pages: Workers & Pages > Create > Pages > Upload assets, drag this folder in.
- GitHub Pages: put the files in a repo, Settings > Pages > Deploy from branch.

## After deploying
1. Open index.html and replace YOUR-DOMAIN in the og:image line with your real address, then redeploy.
2. Optional: download https://cdn.jsdelivr.net/npm/mp4-muxer@5.2.1/build/mp4-muxer.js and save it next to index.html as mp4-muxer.js. The site then no longer needs the CDN for video export.
3. Custom domain: add it in your host's dashboard and follow its DNS instructions. HTTPS is automatic.

## Note
The page must be served over https (or localhost) for audio, install-as-app and offline to work. Opening index.html straight from disk will draw and play but won't install.
