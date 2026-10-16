# St. Aurelius Chapel — Interactive 3D

A self-contained, browser-based Three.js meditation chapel: an original low-poly stone and timber Catholic chapel under a star field, with an interaction-gated procedural liturgical choir.

Live demo: https://1nnovat1on.github.io/catholic-chapel-3d

## Experience

Open `index.html` directly in a modern browser, then select **Enter Chapel & Play Choir**. Drag to orbit, scroll to approach.

The scene includes:

- stone nave, timber details, a pitched roof, and a portal with wooden double doors
- a bell tower, steep steeple, and Latin cross
- six arched stained-glass windows with colored point-light spill
- an illuminated altar, crucifix, paired candles, warm point light, moonlight, fog, and star field
- damped Three.js OrbitControls for a smooth contemplative camera

## Choir synthesis

No recorded assets are bundled. After the user gesture required by browser audio policy, the Web Audio engine creates a continuous chord loop spanning C major and A minor tonal colors. It layers warm triangle/sine voices, subtle per-voice vibrato, a low-pass filter, a slowly decaying envelope, and generated convolution reverb to evoke a small cathedral acoustic.

## Architecture

`index.html` is deliberately self-contained: markup, styles, scene construction, controls, and audio engine are all in one file. The only network dependencies are pinned Three.js r128 CDN scripts:

- `three.min.js`
- `OrbitControls.js`

This keeps GitHub Pages deployment simple while allowing future contributors to adjust geometry in the visible procedural constructors (`box`, `cyl`, `windowAt`) and harmony in the `choir` function.

## Run locally

Open `index.html` in Chrome, Edge, Firefox, or Safari. A local server is optional because this uses classic scripts rather than ES modules.

## License

MIT-style use intended for peaceful, artistic, and devotional exploration.