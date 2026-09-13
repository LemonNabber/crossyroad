Using Three.js and vanilla JavaScript (no build tooling, no framework), build the initial scene for a Crossy-Road-style game.

Camera & look:

Use an OrthographicCamera, not perspective — this is essential for the flat, non-distorted "iso" look of Crossy Road. Position and angle it to look down at the world from a fixed isometric-style angle (elevated, slightly rotated, looking toward the origin).
Add an ambient light plus a directional light (with soft shadows enabled) to get a bright, toy-like look rather than flat/harsh default lighting.
Background should be a simple flat sky color, not black.

World structure:

The ground is made of rows of tiles, running perpendicular to the direction the player will eventually move.
Represent the world as a data array (e.g. rows = [{ type: 'grass', z: 0 }, { type: 'grass', z: 1 }, ...]) even though every row is currently type 'grass'. The renderer should build meshes by reading this array, not by hardcoding grass everywhere. This matters because future phases will change type per row to road/water/rail without touching this generation logic.
Render ~20 rows initially, each a flat plane/box spanning a fixed width, in a solid grass-green color, flat-shaded (no smooth shading — Crossy Road's blocky look depends on this).
Add thin, slightly darker line meshes running along the boundary between each row, so each row reads as a visually distinct strip even though they're all the same material for now.

Do not add: player character, movement, camera following, other tile types, hazards, or UI. This phase is scene setup only.

Acceptance test: When I open the page, I should see a static isometric-looking view of a grassy grid of rows stretching into the distance, with visible thin dividing lines between rows, lit in a bright non-flat way — no player, no interaction yet.
