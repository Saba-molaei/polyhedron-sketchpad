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
| Turn a face to the front (3D) | Click it in either view |
| Rotate 3D / pan 2D | Right-drag, hold Space, or toggle **Rotate/Pan** |
| Zoom | Mouse wheel |
| Colours | Swatches or keys 1–6, plus a custom colour picker |
| Erase a stroke | **Eraser** (E) |
| Undo / redo | ⌘Z / ⇧⌘Z |
| Change the diagram's outer face | **Set outer face…**, then click a face |
| Enlarge the inner faces | **Spread** slider (far right = straight edges), **Eye** slider |
| New drawing | **New** (N) |
| Saved drawings | **My creations** (H): open, rename, delete or search them |
| Back up / move to another browser | **Export JSON** / **Import JSON** |
| Images | **Save PNGs** |

The outer face of the Schlegel diagram is everything outside its boundary, so its drawings
appear in the shaded ring around the diagram (the face turned inside-out).
Every drawing is a *creation*. It is saved automatically, as JSON in your browser's IndexedDB,
each time you finish a stroke, so closing the tab loses nothing. A new drawing is first saved
when you draw on it and gets a name like "Cube 3", which you can change under **My creations**.
When the page opens it reopens your last creation. Picking a model from the menu opens your
most recent drawing of that model.
Creations live only in this browser: use **Export JSON** to keep a copy or move them elsewhere.

## Files

- `polyhedra.html` — the app (uses [Three.js](https://threejs.org) from a CDN).
- `models.js` — polyhedron data, generated from `.obj` files.
- `build_models.py` — converts `.obj` files to `models.js`, keeping only closed convex polyhedra
  and dropping duplicates. It reads `../sgi_logo/models/*.obj`; edit `SRC` to point at your own folder.
