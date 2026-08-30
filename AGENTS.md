# Aggie Engagement Website - Codex Instructions

## Project Purpose
This repository contains the Utah State Athletics Aggie Engagement landing page.

The website should remain clean, professional, modern, easy to navigate, and consistent with Utah State Athletics / Aggie Engagement branding.

Future maintainers may not have extensive coding experience. Explain technical steps clearly and do as much of the implementation directly as is safely possible.

## Before Making Changes
Before editing anything:

1. Read this entire `AGENTS.md` file.
2. Read `PROJECT_HANDOFF.md` and `PROJECT_STATUS.md` if they exist.
3. Inspect the existing code related to the request.
4. Do not change unrelated files or sections.
5. Preserve existing working functionality unless specifically asked to change it.

Never guess how the site works when the repository can be inspected first.

## Website Structure
The Git repository root is the outer `Aggie Engagement Landing Page` folder.

Future maintainers should open and work from the repository root. Do not treat the `aggie-engagement` subfolder as a separate repository.

The production website files are:

- `index.html` - root redirect page that points visitors to `/aggie-engagement/`
- `aggie-engagement/index.html` - main production webpage structure and content
- `aggie-engagement/styles.css` - main production webpage styling
- `assets/` - shared website images used by the page and stylesheet
- `package.json` - local preview script definition
- `package-lock.json` - npm lockfile for the local preview setup
- `server.mjs` - simple local static preview server

The normal local preview command is:

`npm start`

The normal local preview URL is:

`http://localhost:5173/aggie-engagement/`

This repository is the source of truth.

## GitHub / Deployment
GitHub repository:

`aggie-engagement/aggie-engagement-landing-page`

Production branch:

`main`

The website is hosted using GitHub Pages.

GitHub Pages deploys from:

`main` -> `/ (root)`

Changes pushed to `main` are therefore production website changes.

Because GitHub Pages deploys from the repository root, the root `index.html` redirect page is part of the production setup and should not be removed unless the deployment structure changes.

## Normal Workflow
For a website update:

1. Understand the request.
2. Inspect the relevant existing HTML/CSS.
3. Make the smallest reasonable change.
4. Review the diff.
5. Confirm unrelated files were not changed.
6. Test or preview the change when appropriate with `npm start`, then open `http://localhost:5173/aggie-engagement/`.
7. Commit only the intended files.
8. Push the approved change to `origin/main`.
9. Confirm the push succeeded.
10. Remember that pushing to `main` affects the production GitHub Pages site.

Before committing, always check `git status`.

Do not force-push or rewrite Git history for normal website updates.

## Editing Philosophy
Prefer targeted edits instead of unnecessary rewrites.

Common changes may include:

- updating text
- updating links
- replacing images
- changing contact information
- modifying buttons
- updating program information
- adjusting spacing or layout
- adding/removing website sections
- small visual improvements

Preserve:

- responsive/mobile behavior
- accessibility
- existing working links
- existing design consistency

Do not add unnecessary frameworks, libraries, or dependencies for simple changes.

## Design Direction
Keep the site:

- clean
- modern
- professional
- polished
- collegiate without being overly themed
- visually intentional rather than busy

Primary visual direction:

- Utah State navy
- white
- gray/silver

Avoid:

- gold as a main accent
- neon/bright colors
- clutter
- excessive animation
- generic or cheesy athletics graphics
- unnecessary decorative elements

Graphics should clearly relate to the program or section they represent.

## Content
Aggie Engagement includes areas such as:

- Aggies Lead / student-athlete development
- A-Club / alumni engagement
- community outreach
- strategic partnerships

Website language should be concise, professional, welcoming, and appropriate for a Division I athletics department.

Never invent:

- dates
- statistics
- names
- contact information
- URLs
- program details

If required information is unknown, ask the maintainer.

## Links
When changing links:

- verify the destination
- use `mailto:` for email
- use `tel:` for phone
- avoid placeholder links unless specifically requested

## Images
When replacing images:

- use the project's existing `assets/` folder
- use clear filenames
- update alt text appropriately
- confirm the image displays correctly
- do not delete an old asset until confirming it is unused

## Working With Non-Technical Maintainers
The person requesting a website change may describe what they want visually rather than using HTML/CSS terminology.

Translate their request into the appropriate technical change.

Do not require them to know coding terminology.

When they need to perform a step themselves, give short numbered instructions.

## Documentation
This website should not depend on knowledge held by one individual.

If important project information is discovered that future maintainers will need, recommend documenting it in `PROJECT_HANDOFF.md` or `PROJECT_STATUS.md`.
