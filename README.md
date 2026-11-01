# Kinetic Text — tiny-display GIF maker

A single-file web tool that turns a line of text (plus images, logos, and
uploaded GIF clips) into a looping GIF sized for tiny LED panels and curtain
lights. Everything runs in the browser — no build step, no server.

## Use it

Open `index.html` in a browser, or visit the GitHub Pages site (below).

- Type text, pick a font, colors, background, and an entrance effect.
- Three reveal modes: build up, one letter at a time, or two-at-a-time slide.
- Add image / logo / uploaded-GIF steps to a sequence.
- Set a target size (e.g. 30×32) and press **Render GIF**.
- Save/Load your work as a `.ktproj` file.

## 3D text and logos need internet

The 2D path works fully offline. The optional **real 3D** text and the
extruded-logo view load [three.js](https://threejs.org/) from a CDN, so those
features need a network connection. Everything else runs with no network.

## Publish to GitHub Pages

1. Create a new empty repo on GitHub (no README).
2. Point this local repo at it and push:
   ```bash
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment**.
   Set **Source** to *Deploy from a branch*, branch **main**, folder **/ (root)**.
4. Wait a minute. The site is served at
   `https://<you>.github.io/<repo>/`, loading `index.html`.

## Browser note

Rendering GIF frames from an uploaded GIF needs a browser with the
`ImageDecoder` API (current Chrome / Edge). Text, colors, and export work
everywhere.
