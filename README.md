# Monaco Drive 3D — Complete Rebuild (prototype)

## Run / deploy
This is a static site. Extract the ZIP and upload the contents to the root of a Netlify site or GitHub Pages repository. `index.html` must be at the published root. Open it over HTTPS or localhost; do not use `file://`.

## Controls
- Touch: hold left/right, GO, BRAKE, or HB. Simultaneous inputs are supported.
- CAMERA switches chase/hood views; RESET CAR resets to the nearest available road; PAUSE opens the resume screen.
- Desktop: WASD/arrows, Space handbrake, C camera, R reset, Escape pause.

## Data and attribution
When available, live road centerlines and building footprints are requested from OpenStreetMap through public Overpass API endpoints. © OpenStreetMap contributors: https://www.openstreetmap.org/copyright. OSM data is licensed under the Open Database License (ODbL). Three.js is loaded from jsDelivr CDN.

## Important accuracy and test notes
- This build includes a procedural fallback street layout so the Start button can enter a playable 3D scene even when Overpass requests fail. The fallback is **not** the real Monaco street layout.
- The terrain is a procedural hill approximation, not a verified digital elevation model. It is not accurate enough to claim exact Monaco terrain.
- Live OSM roads/building footprints, if successfully fetched, are added to the scene, but this prototype does not yet perform a full topological junction reconstruction, true tunnel excavation, bridge layer handling, or a complete building collision system.
- The vehicle uses lightweight arcade movement, not a full rigid-body vehicle physics engine. Road-edge handling is forgiving and approximate.
- External internet access is required for Three.js and live map data. Overpass endpoints may be rate-limited or unavailable.
- No real iPad, browser automation, or live-host deployment test was performed in this environment. Do not treat this as production-certified or “perfect.”

## Verification report
- ZIP file list and HTML structure: checked during packaging.
- Automated browser interaction, full runtime test, and physical iPad Safari test: not performed.
