# Aggie Engagement Website - Project Status

Last updated: August 30, 2026

## Current Status
The Aggie Engagement landing page is live and functioning.

The Git repository root is the outer `Aggie Engagement Landing Page` folder. Future maintainers should work from the repository root, not from only the `aggie-engagement` subfolder.

## Production Setup
- GitHub organization: `aggie-engagement`
- Repository: `aggie-engagement-landing-page`
- Production branch: `main`
- Hosting: GitHub Pages
- Publishing source: `main` branch -> repository root `/`
- Pushing to `main` affects the production website.

## Core Website Files
- `index.html` - root redirect page
- `aggie-engagement/index.html` - main production webpage
- `aggie-engagement/styles.css` - main production stylesheet
- `assets/` - shared website images
- `package.json` - local preview script definition
- `package-lock.json` - npm lockfile for the local preview setup
- `server.mjs` - simple local static preview server

## Local Preview
Preview command:

`npm start`

Normal preview URL:

`http://localhost:5173/aggie-engagement/`

## Current Maintenance Method
Website updates are currently made in Visual Studio Code with Codex assistance.

Changes are reviewed, committed to Git, and pushed to `origin/main`.

GitHub Pages automatically deploys changes pushed to the production branch.

## Handoff Status
- [x] Production repository identified
- [x] GitHub Pages deployment identified
- [x] `AGENTS.md` created, committed, and pushed to GitHub
- [x] `PROJECT_HANDOFF.md` created, committed, and pushed to GitHub
- [x] `PROJECT_STATUS.md` created, committed, and pushed to GitHub
- [x] `MAINTENANCE_GUIDE.md` created locally and reviewed
- [ ] `MAINTENANCE_GUIDE.md` committed and pushed to GitHub
- [ ] New GitHub organization owner added
- [ ] Successor added to repository/project
- [ ] Successor setup walkthrough completed
- [ ] Successor successfully clones repository
- [ ] Successor successfully makes a test update
- [ ] Successor successfully pushes to GitHub
- [ ] Successor confirms GitHub Pages deployment
- [ ] Original maintainer access removed, if appropriate

## Known Issues / Maintenance Concerns
- External links should be verified after future updates.
- The LinkedIn URL looks typo-prone and should be checked: `https://www.linkedin.com/company/utah-state-univerity-athletics/`
- The footer `Logan, Utah` link points to `#contact`, which is somewhat placeholder-like.
- `sagebrushawardphoto.jpg` is unusually large and should ideally be replaced or compressed with a web-optimized version.
- The root redirect path should be verified on the live GitHub Pages site.

## Future Work
Add unfinished website improvements, requested changes, or known future updates here as needed.

Recommended future work:

- Commit and push `MAINTENANCE_GUIDE.md` after final approval.
- Verify the GitHub Pages live redirect behavior from the root page.
- Confirm all external URLs are still correct.
- Web-optimize large image assets, especially `sagebrushawardphoto.jpg`.

## Documentation Rule
Update this file whenever the project's status meaningfully changes so the next maintainer can quickly understand where things stand.
