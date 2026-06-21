# Build Notes

Validated in the packaging environment:

- `npm install --ignore-scripts` completed.
- `npm run type-check` completed with no TypeScript errors.
- `next build` reached `Compiled successfully`, then the sandbox Node/Next build worker did not exit cleanly during page-data collection. The project is configured for Netlify Node 20 via `.nvmrc` and `netlify.toml` because this sandbox runs Node 22, which can leave Next build workers hanging in this environment.

Production recommendation:

1. Deploy on Netlify with Node 20.
2. Run `npm run type-check` in CI before `npm run build`.
3. Replace the starter `/admin` local editor with Sanity/Supabase before relying on multi-user live publishing.
