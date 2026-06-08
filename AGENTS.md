# PaperBright Build Rules

These rules come from the workflow references used for the project: Astro for the app shell, Tailwind v4 for styling, and Vercel-style interface discipline.

- Build the real editor first; avoid landing-page filler.
- Keep the app static and browser-first so it deploys cleanly on Vercel.
- Use Astro islands only when interactivity needs a framework. Plain browser JavaScript is enough for this editor.
- Style with Tailwind v4 tokens and stable dimensions.
- Keep the palette restrained: paper, ink, neutral borders, and one blue signal color.
- Prefer dense, scannable controls over oversized promotional sections.
- Preserve local-first document behavior unless persistence requirements change.
