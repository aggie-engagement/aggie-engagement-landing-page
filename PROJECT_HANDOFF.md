# Aggie Engagement Website - Project Handoff

## Project Overview
This repository contains the Utah State Athletics Aggie Engagement landing page.

The goal of this handoff is to make sure future staff can fully maintain the website without relying on the original creator.

## Repository
GitHub organization:

`aggie-engagement`

GitHub repository:

`aggie-engagement-landing-page`

Production branch:

`main`

Git repository root:

`Aggie Engagement Landing Page`

Future maintainers should clone and open the full repository root, not just the `aggie-engagement` subfolder.

## Live Website
The website is hosted with GitHub Pages.

GitHub Pages publishes from:

`main` branch -> `/ (root)`

Current live site:

`https://aggie-engagement.github.io/aggie-engagement-landing-page/`

When an approved change is pushed to `main`, GitHub Pages automatically redeploys the website.

Pushing to `main` affects the production website.

## Main Website Files
The production website repository currently contains:

- `index.html` - root redirect page that points visitors to `/aggie-engagement/`
- `aggie-engagement/index.html` - actual main webpage structure and content
- `aggie-engagement/styles.css` - actual webpage styling
- `assets/` - shared website images
- `package.json` - local preview script definition
- `package-lock.json` - npm lockfile for the local preview setup
- `server.mjs` - simple local static preview server

The following documentation files have been created locally and should be committed/pushed after review:

- `AGENTS.md` - instructions for Codex / AI-assisted maintenance
- `PROJECT_HANDOFF.md` - project ownership and handoff information
- `PROJECT_STATUS.md` - current website status and future work

The root `index.html` redirect page is part of the GitHub Pages setup and should remain unless the deployment structure changes.

Assets are referenced from the webpage using `../assets/...` paths because the main page lives inside the `aggie-engagement/` folder.

The production page is static HTML/CSS. It uses no frontend framework, no JavaScript behavior, no external fonts, and no npm dependencies for the production page itself.

## Important Local Folder Note
The repository root is the outer folder named:

`Aggie Engagement Landing Page`

Inside it is the main webpage folder:

`aggie-engagement`

The inner `aggie-engagement` folder is not a separate repository. It contains the actual webpage HTML and CSS.

Future maintainers should clone the GitHub repository directly to their own computer and open the full repository root.

## Programs Used
The website has been maintained using:

- GitHub - code storage, version history, access management, and GitHub Pages hosting
- Visual Studio Code - local code editing
- Git - version control
- Codex / AI assistance - code changes, troubleshooting, and maintenance support
- Browser - previewing and verifying the live website

## Local Preview
To preview the site locally from the repository root, run:

`npm start`

Then open:

`http://localhost:5173/aggie-engagement/`

## Normal Maintenance Process
A normal website update should follow this process:

1. Open the cloned repository root in Visual Studio Code.
2. Ask Codex to read `AGENTS.md`, `PROJECT_HANDOFF.md`, and `PROJECT_STATUS.md`.
3. Describe the requested website change in normal language.
4. Let Codex inspect the existing code before changing anything.
5. Make the smallest necessary change.
6. Review the change.
7. Preview locally when appropriate with `npm start`, then open `http://localhost:5173/aggie-engagement/`.
8. Check `git status`.
9. Commit only the intended files.
10. Push the approved commit to `origin/main`.
11. Confirm the GitHub Pages deployment succeeds.
12. Open the live website and verify the change.
13. Verify any external links changed during the update.

## Hardcoded Website Content
The following items are hardcoded in `aggie-engagement/index.html` and may need to be updated by future maintainers:

- contact email: `aggieslead@usu.edu`
- phone number: `435-797-3116`
- location: `Logan, Utah`
- social media links
- survey URL: `https://utahstateaggies.com/sb_output.aspx?form=77`
- external Aggie Engagement URL: `https://utahstateaggies.com/sports/2025/5/5/Aggie-engagement.aspx`
- program names, descriptions, highlights, and section text

There are no staff names hardcoded in the webpage.

## Asset Notes
Shared images are stored in `assets/`.

`sagebrushawardphoto.jpg` is unusually large and should ideally be replaced or compressed with a web-optimized version later.

## GitHub Ownership
At the time this handoff documentation was created, the original maintainer was the only owner of the `aggie-engagement` GitHub organization.

Before the original maintainer leaves, organization ownership should be transferred to permanent Utah State Athletics / Aggie Engagement staff.

Ideally, at least two appropriate staff members should have Owner access to the organization.

The original maintainer should only be removed after the new owners have confirmed they can:

- access the organization
- access the repository
- clone the repository
- make a test change
- commit and push
- verify the GitHub Pages deployment

## Account Security
Do not store passwords, recovery codes, personal access tokens, or other credentials inside this repository.

Access should be granted through each person's own GitHub account.

## Future Documentation
If the website structure, hosting setup, repository location, or maintenance workflow changes, update this file so future staff do not have to rediscover how the project works.
