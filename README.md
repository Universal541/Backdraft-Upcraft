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
## Official logo (asset awaiting repository upload)
The canonical official logo was provided by the owner November 3, 2026. The website already has image slots for `assets/backdraft-upcraft-logo.webp` in the header, hero, and footer. Until that image is uploaded, existing text branding is displayed instead of a broken image.

To finish integration: download the optimized logo file provided in the chat and upload it via GitHub's **Add file → Upload files** into a newly created `assets` folder at repository root, preserving the exact filename `backdraft-upcraft-logo.webp`. GitHub's browser upload UI may require creating the folder first; the image can also be uploaded via a local Git commit.

Product transparency: all depicted collection products are concept illustrations. The Spoolhouse Bar, Iron Horse Across the Valley spool-end pyrography, and bespoke humidor for Sean are initial planned physical builds, not completed inventory. Do not publish unverified catalog prices or mark products completed until actual build evidence is available.

## Catalog artwork upload (November 3, 2026)
The 25-image source archive was supplied as BUCat1.zip. An optimized web asset ZIP was prepared in the chat, containing:
- `assets/backdraft-upcraft-logo.webp` (official artwork)
- `assets/catalog/01.webp` through `assets/catalog/25.webp` (original catalog sheets optimized for web)

The gallery in `catalog.html` uses 21 of those sheets; other assets are retained in the pack for future use. The gallery displays a graceful fallback until these files are uploaded to the repository.

**To publish all artwork:** unzip the provided asset ZIP on your computer and copy its `assets` directory contents into the repository `assets` directory, maintaining folder paths. Using local Git is the easiest way to commit all 26 image assets in one push; alternatively upload the logo into `assets/` and the 25 catalog images into `assets/catalog/` using GitHub's browser upload UI. Pushing a ZIP file alone will not unpack it for the site.

Some images show historical conceptual prices. These are intentionally marked as illustrated estimates, not verified offers. Earlier pricing notes include Roundhouse sizes 24″ $99, 30″ $129, 36″ $159, 48″ $199, 54″ $249; Homestead Sentinel from $149; Compartment of Questionable Ideas from $249. Before displaying these as actual selling prices, verify costs and specifications. Some catalog artwork may contain inconsistent historical price references.
