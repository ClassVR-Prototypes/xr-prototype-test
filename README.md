# xr-prototype-test

WebXR prototypes built with the
[ClassVR Prototyping Kit](https://github.com/ClassVR-Prototypes/classvr-prototyping-kit).
Each app lives in its own folder with an `xr-project.json`.

## Live site

Everything on `main` is published to GitHub Pages:

**https://classvr-prototypes.github.io/xr-prototype-test/**

Apps are served at the slug from their manifest, so `Planet Walk/` is at
`/planet-walk/`. Unlike a Claude artifact link — which runs the app inside a
frame that blocks WebXR — a Pages URL is a plain HTTPS page, so the
**Enter VR** button works and a headset can open it directly.

Publishing runs on every push to `main` (`.github/workflows/pages.yml`). The
site sits behind a CDN, so a change can take a few minutes to appear; the build
number on each app's panel tells you which version you are looking at.

To preview the site locally:

    python3 .github/scripts/build_pages.py --out _site
    python3 -m http.server -d _site
