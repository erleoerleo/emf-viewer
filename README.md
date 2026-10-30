# EMF Viewer

A tiny static web page for viewing Windows Enhanced Metafiles (`.emf`) with zoom and pan. Everything runs in the browser; files are never uploaded.

**Live:** https://erleoerleo.github.io/emf-viewer/

## Usage

- Click **Open** or drop an `.emf` file onto the page.
- Scroll or pinch to zoom, drag to pan, double-click (or **Fit**) to fit the window.
- Load a file by URL: `index.html?url=path/to/file.emf` (same origin or CORS-enabled).

## How it works

`emfjs.js` is a patched copy of EMFJS from [rtf.js](https://github.com/tbluemel/rtf.js) 3.0.9 (MIT, see `LICENSE-rtf.js`). It converts EMF records to SVG; the viewer zooms by changing the SVG `viewBox`.

Not supported yet: embedded bitmaps, arcs/pies/chords, clip paths and EMF+-only content.

## Run locally

```
python -m http.server 8000
```

Then open http://localhost:8000/.
