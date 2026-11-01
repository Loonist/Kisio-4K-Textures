# Kisio Design Media — texture integration instructions for Claude

Open [textures.json](./textures.json). All 15 texture URLs are **already hosted on Shopify CDN**; do not request a ZIP or ask user to upload manually.

Target: unpublished Shopify theme **Kisio Game Studio — Animation Repair**. Do not touch live theme or publish.

Map assets by keys:
- planet_albedo, planet_clouds, planet_night_lights → planet sphere (equirectangular UV, separate cloud layer, night-side emissive mask).
- moon_albedo, moon_normal → rotating moon sphere with visible surface landmarks.
- floor_albedo, floor_roughness, floor_normal → ship floor materials with appropriate tiling, perspective and lighting; floor_normal is WebP.
- monitor_radar, monitor_systems, monitor_navigation, monitor_scan → four monitor DISPLAY surfaces only, aspect-preserving UVs and physically seated monitor bases.
- hologram_globe → transparent rotating hologram sphere.
- emitter_top, emitter_emissive → circular emitter top and additive controlled light.

Verify each CDN URL loads. Inspect image dimensions and transparency, handle proper color spaces, normal map conventions, caching and loading failure. Do not assume textures are native-resolution photography; they are generated/illustrated textures. Preserve geometry and composition. Verify planet slowdown (25% of baseline) and independent visible moon rotation. Optimize loading for mobile without introducing blur on desktop.

Report real Shopify draft preview screenshots and before/after comparisons, files changed, browser errors, performance where measured, and final 15-item asset checklist. Stop before publication or Phase 2.
