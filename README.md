# mark-sampler

Draw with data. A single-file, dependency-free tool that resamples a silhouette
into marks, digits and lines at descending resolutions, so you can pick the
coarsest version that still reads.

- **Sources:** built-in shapes, text, an uploaded image, or a 3D model
  (`.stl`, `.glb`, `.obj`) with turn / tilt / roll and a movable light.
- **Tiles mode:** symbol ramps (rings, dots, crosses, bars, geometric tiles) and
  data glyphs: binary 0/1, digits 0–9, ASCII density, with an optional "ground"
  field of faint zeros.
- **Lines mode:** contours, rings, spiral, parallel lines, waveforms and relief.
  With a 3D model the lines can wrap the form: terrain contours, latitude rings
  (one or two poles), helices and slices, with hidden surfaces removed.
- **Tone:** depth from edge, distance field, coverage, image luminance, a pasted
  or CSV data series, gradients, or 3D slices / depth / shading.
- **Output:** stroke-free filled SVG paths that import cleanly into Figma and
  Illustrator. Settings are kept in the URL as a shareable recipe.

## Running locally

It's one static file. Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8732
```

then visit <http://localhost:8732>.

## Deploying

Static site, no build step. On Vercel, import the repo with the framework preset
set to **Other** and leave the build and output settings empty.
