# Feature Tour Video QA

## Output

- Embedded in: `index.html`
- Codec: H.264 / AVC
- Resolution: 176 × 110
- Frame rate: 1.5 fps
- Duration: 40.17 seconds (accelerated feature tour)
- Audio: none; chapter captions identify each operation
- Size: approximately 6 KB (repository-optimized accelerated preview encode)

## Recorded chapters

1. Initial real-time 3D specimen
2. Drag rotation and zoom
3. Structure hotspots and callouts
4. Four-wing flight mechanics
5. Angle-dependent structural colour
6. Surface, vein and membrane layers
7. Wing-scale micro cross-section
8. Isolated specimen view
9. Dorsal and ventral comparison
10. Complete metamorphosis
11. One-click reset
12. Concept source attribution: `thebuggeddev/anatomy`, created by `@thebuggeddev`

## Validation

- WebGL 2 initialized successfully under Chromium 144.
- 809 source frames were captured from the live demo.
- Browser console and page-error collection returned no errors.
- The final MP4 was encoded with `libx264`, `yuv420p` and fast-start metadata.

> The public repository carries a compact accelerated encode embedded in the project homepage so the complete feature tour remains easy to play directly from GitHub Pages.
