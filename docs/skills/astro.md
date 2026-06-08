# Astro Skill Notes

Use Astro as the production shell:

- Keep `src/pages/index.astro` as the single app entry until routing is needed.
- Import global CSS from the Astro page or layout.
- Prefer framework-free client scripts for small interactions.
- Keep browser-only code inside `<script>` blocks so server rendering remains simple.
