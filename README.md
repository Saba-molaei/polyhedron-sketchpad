# Polyhedron Sketchpad

**▶ [Open the sketchpad](https://saba-molaei.github.io/polyhedron-sketchpad/polyhedra.html)** — runs in the browser, nothing to install.

Draw on the faces of a convex polyhedron and see the drawing on its
[Schlegel diagram](https://en.wikipedia.org/wiki/Schlegel_diagram), or draw on the diagram and see it on the 3D solid.

## Models

31 convex polyhedra: the 5 Platonic, 13 Archimedean and 13 Catalan solids.

## How to use

| Action | How |
| --- | --- |
| Draw | Left-drag in either view |
| Rotate 3D / pan 2D | Right-drag, hold Space, or toggle **Rotate/Pan** |
| Zoom | Mouse wheel |
| Colours | Swatches or keys 1–6, plus a custom colour picker |
| Erase a stroke | **Eraser** (E) |
| Undo / redo | ⌘Z / ⇧⌘Z |
| Change the diagram's outer face | **Set outer face…**, then click a face |
| Spread the diagram | **Eye** slider |
| Save work | **Export JSON** / **Import JSON**, **Save PNGs** |

The outer face of the Schlegel diagram is everything outside its boundary, so its drawings
appear in the shaded ring around the diagram (the face turned inside-out).
Drawings are saved in your browser per model; export JSON to keep a copy.

## Files

- `polyhedra.html` — the app (uses [Three.js](https://threejs.org) from a CDN).
- `models.js` — polyhedron data, generated from `.obj` files.
- `build_models.py` — converts `.obj` files to `models.js`, keeping only closed convex polyhedra
  and dropping duplicates. It reads `../sgi_logo/models/*.obj`; edit `SRC` to point at your own folder.
