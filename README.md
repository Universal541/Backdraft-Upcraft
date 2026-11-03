# Backdraft Upcraft Website

Reclaimed. Repurposed. Reimagined.

## Launch status
- The website is a dependency-free static site in `index.html`.
- Cloudflare Pages should deploy it directly from the repository's `main` branch.
- No Node.js, npm, framework, or build step is required.
- The custom inquiry form is intentionally inactive until a Formspree endpoint is configured.
- Collection illustrations are inline SVG concept drawings, not verified finished products.

## Cloudflare Pages configuration
Connect this repository via Git integration:
- Production branch: `main`
- Framework preset: None
- Build command: (blank)
- Build output directory: `/` (repository root)
- Root directory: `/`

If a Pages project already exists, check Settings → Builds & deployments / Build configurations and verify these values. A failed initial deployment may be resolved by deploying this new commit. If it still fails before the build starts, inspect the deployment details and GitHub integration rather than changing website code blindly.

## Activating the contact form
1. Create and verify a form in Formspree.
2. In `index.html`, find `const FORMSPREE_ENDPOINT='';`.
3. Replace the empty value with your Formspree URL (e.g., `https://formspree.io/f/your-form-id`).
4. Save and commit the file. Cloudflare will deploy the change.
5. Send a real test inquiry and confirm that it arrives successfully.

No secret key is required in the public site for a standard Formspree form endpoint. Do not commit service-role keys, API secrets, or private credentials.

## Later enhancements
- Replace temporary illustrations with approved Backdraft logo and actual product imagery.
- Build product detail pages and catalog.
- Add pricing and availability only after confirmation.
- Consider Supabase for structured catalog or client-side features when necessary.
- Add the custom domain and review DNS/SSL after the initial Pages deployment succeeds.

## Notes
This is a starter public-facing website. Copy and illustrative category names should be reviewed before commercial launch.