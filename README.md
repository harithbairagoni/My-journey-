# Harith’s World

Interactive portfolio based on the supplied 8-second video, build specification and Harith Bairagoni’s résumé.

## Develop

Requires Node.js 20.19+ or 22.12+.

```sh
npm ci
npm run dev
npm run build
npm run preview
```

## Experience

Scroll naturally through seven chapters or select a sidebar item, globe label or chapter dot. Drag the globe to orbit. Left/right arrow keys move between chapters. The lighting toggle, IST clock format, pause control, ambient tone, text view and résumé download work locally without accounts or APIs. The music playlist remains honestly marked as coming soon.

Paths: `/`, `/experience/landsafe`, `/experience/ethanol`, `/experience/strategy`, `/experience/workshop`, `/about`, `/contact`. Static hosting must serve `index.html` for these SPA paths.

## Source structure

- `src/data.ts`: résumé-grounded chapter content and contact links.
- `src/World.tsx`: procedural Three.js architecture, Earth, routes, character and camera interpolation.
- `src/App.tsx`: routing, scrolling, dashboard controls and accessible reading panel.
- `src/style.css`: responsive visual system.
- `public/Harith-Bairagoni-Resume.pdf`: supplied résumé, unmodified.

## Reference fidelity

The supplied video is a rendered concept, not an exported web application or 3D scene. Architecture and avatar are custom procedural approximations; no original GLB models or portrait reference images were provided. The implementation reproduces the dark space direction, Earth scene, architectural landmarks, luminous paths, HUD panels and guided chapter journey. It does not claim a pixel-identical or photorealistic reconstruction.

Earth textures: Three.js example assets at https://threejs.org/examples/textures/planets/earth_atmos_2048.jpg and earth_normal_2048.jpg. Fonts: Libre Baskerville, Space Grotesk and Space Mono, self-hosted from Google Fonts. Icons: Lucide. All résumé metrics originate from the supplied PDF.

## Accessibility and performance

The 3D bundle loads separately from the interface. Reduced motion disables continuous rendering and uses immediate camera updates. The text view preserves all experience content; dialog focus is trapped and restored. A 2D explorer appears on a render error or after the 4-second loading limit. Native scrolling remains enabled; no wheel-event interception is used.

## Verification

Production TypeScript compilation and Vite build passed. Desktop Chrome visually rendered the textured globe and all landmarks. Experience navigation, Landsafe detail panel and lighting toggle were verified through the browser. The résumé asset and all route responses were checked over HTTP. Responsive layouts are implemented; full mobile browser and cross-browser testing remain outstanding.
