# LocalWipe — Free Watermark Remover, 100% Local

Remove watermarks from photos without uploading them to any server. Everything runs in your browser — your images never leave your device.

## Features

- **100% Local Processing** — All computation happens in your browser using Canvas API
- **Zero Upload** — Your images never touch our servers, not even a single pixel
- **Free to Use** — 5 images/day free, no sign-up required
- **No File Size Limit** — Only limited by your browser's memory
- **Batch Support** — Process multiple images (coming soon)
- **Offline Capable** — Works without internet after initial page load
- **Privacy First** — No tracking cookies, no image data collection

## Live Demo

[https://localwipe.pages.dev](https://localwipe.pages.dev)

## Deploy to Cloudflare Pages

[![Deploy to Cloudflare Pages](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/)

1. Fork this repository
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Connect your GitHub account
4. Select this repository
5. Set build output directory to `/` (root)
6. Click "Save and Deploy"

No build step needed — it's a static site with all code in `index.html`.

## Manual Deploy

This is a static site. Upload the files to any static hosting service:

- **Cloudflare Pages**: Connect GitHub repo, no build config needed
- **Netlify**: Drag and drop the folder
- **Vercel**: Import from GitHub
- **GitHub Pages**: Enable in repo settings

## Local Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/localwipe.git
cd localwipe

# Open in browser
open index.html
# or
python -m http.server 8000  # then visit http://localhost:8000
```

No build tools, no Node.js, no dependencies. Just open `index.html` in a browser.

## Tech Stack

- **HTML/CSS/JS** — All inline in a single `index.html`
- **Tailwind CSS v3** — Utility-first CSS (via CDN)
- **Font Awesome 6** — Icons (via CDN)
- **Canvas API** — Image processing and brush tools
- **JSZip** — Batch download as ZIP (via CDN)

## How the Inpainting Works

The watermark removal uses an iterative diffusion algorithm:

1. User paints a mask over the watermark area
2. The algorithm identifies unmasked pixels at the mask boundary
3. In each iteration, masked pixels adopt the average color of their unmasked neighbors
4. After enough iterations, the fill propagates inward from all edges
5. A final smoothing pass blends the filled area with the surrounding image

This runs entirely in JavaScript using Canvas pixel manipulation — no server, no AI model download.

## Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change.

## License

[MIT](LICENSE)

## Disclaimer

LocalWipe is an independent project. Please ensure you have the right to remove watermarks from images before using this tool. Respect copyright laws in your jurisdiction.
