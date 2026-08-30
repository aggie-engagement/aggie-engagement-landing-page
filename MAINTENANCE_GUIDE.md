# Aggie Engagement Website Maintenance Guide

## Start Here
This guide is for the Utah State Athletics staff member who inherits the Aggie Engagement website. You do not need previous knowledge of the original creator's computer setup or any past ChatGPT/Codex conversations to use it.

## What You Need
Before you can maintain the website, you will need a few basic programs and accounts. These tools let you access the website files, preview changes on your computer, and publish approved updates.

1. GitHub account

Each maintainer should use their own GitHub account. GitHub is where the website files are stored online.

You will need to be given access to the `aggie-engagement` GitHub organization and the `aggie-engagement-landing-page` repository.

Do not share another person's GitHub password or login. Each person should sign in with their own account.

2. Visual Studio Code

Visual Studio Code is the program used to open and work with the website files on your computer.

Official download website:

`https://code.visualstudio.com/`

3. Git

Git keeps track of website changes and connects the local project on your computer to GitHub.

Official download website:

`https://git-scm.com/downloads`

4. Node.js / npm

Node.js is needed to run the local website preview before publishing changes. npm comes with Node.js.

Official Node.js download website:

`https://nodejs.org/`

You do not need a specific Node.js version unless the repository is updated later to specify one.

5. Codex / ChatGPT coding assistance

AI coding assistance can help inspect the project, make requested changes, troubleshoot problems, and explain technical steps in plain language.

You do not need access to Danika's old ChatGPT/Codex conversations. The important project context is stored in `AGENTS.md`, `PROJECT_HANDOFF.md`, `PROJECT_STATUS.md`, and this guide.

When starting a new Codex session for this website, ask Codex to read those project documentation files before making changes.

6. Web browser

A web browser is used to preview the website, access GitHub, and verify the live GitHub Pages site after publishing.

You do NOT need:

- a separate Vercel or other hosting account for this website
- Danika's personal GitHub login
- Danika's personal Visual Studio Code setup
- Danika's personal ChatGPT or Codex login

GitHub Pages handles the hosting for this website.

## Initial Setup
Use these steps when setting up the Aggie Engagement website on a computer for the first time.

1. Get GitHub access

Create or sign into your own GitHub account. GitHub is the website where the project files are stored online.

An existing owner of the `aggie-engagement` GitHub organization must invite you to the organization and repository. Accept that invitation before continuing.

Repository:

`aggie-engagement/aggie-engagement-landing-page`

Access and ownership should be handled through individual GitHub accounts, not shared passwords. Do not use another person's GitHub login.

2. Install Visual Studio Code

Download Visual Studio Code from:

`https://code.visualstudio.com/`

Use the normal installer for your computer. Visual Studio Code is the program you will use to open and work with the website files.

3. Install Git

Download Git from:

`https://git-scm.com/downloads`

Use the standard/default installation options unless Utah State IT gives you different instructions. Git is the tool that tracks website changes and connects your computer to GitHub.

After installing Git, you may need to restart Visual Studio Code so it can find Git.

4. Install Node.js

Download Node.js from:

`https://nodejs.org/`

Choose the current LTS version. LTS means "Long Term Support" and is the stable version recommended for most users.

npm is installed automatically with Node.js. npm is the tool used to run the local website preview command.

5. Clone the GitHub repository

Cloning means downloading your own working copy of the GitHub project to your computer.

Repository URL:

`https://github.com/aggie-engagement/aggie-engagement-landing-page.git`

Beginner-friendly Visual Studio Code steps:

1. Open Visual Studio Code.
2. Open the Source Control view.
3. Choose `Clone Repository`.
4. Paste the repository URL.
5. Choose a location on your computer where you can easily find the project later.
6. When Visual Studio Code asks if you want to open the cloned repository, choose yes.

Make sure you open the full cloned repository folder. Do not open only the `aggie-engagement` subfolder.

6. Confirm the correct folder

When the correct repository root is open in Visual Studio Code, you should see items including:

- `AGENTS.md`
- `PROJECT_HANDOFF.md`
- `PROJECT_STATUS.md`
- `MAINTENANCE_GUIDE.md`
- `README.md`
- `index.html`
- `aggie-engagement/`
- `assets/`
- `package.json`
- `package-lock.json`
- `server.mjs`

If you only see `index.html` and `styles.css`, you may have opened the `aggie-engagement` subfolder instead of the full repository root.

7. First Codex session

When you start a new Codex session for this website, paste this starter prompt:

```text
I am taking over maintenance of the Aggie Engagement website. Before making any changes, read AGENTS.md, PROJECT_HANDOFF.md, PROJECT_STATUS.md, and MAINTENANCE_GUIDE.md. Then inspect the repository structure so you understand how the website works. Do not modify, commit, or push anything yet. Tell me when you understand the project and summarize the maintenance workflow for me.
```

This lets Codex learn the project from the repository documentation instead of needing access to any previous maintainer's conversations.

8. Stop point

Do not make or publish a website change yet. The next sections of this guide will explain how to open, preview, edit, review, commit, and publish safely.

## Opening the Website Project
Use these steps when you have already completed Initial Setup and are coming back later to work on the website.

1. Open Visual Studio Code.

2. Open the repository.

Use `File > Open Folder`.

Select the full cloned `aggie-engagement-landing-page` repository folder on your computer. Do NOT open only the `aggie-engagement` subfolder.

3. Confirm you are in the right place.

In the Visual Studio Code Explorer, you should see items including:

- `AGENTS.md`
- `PROJECT_HANDOFF.md`
- `PROJECT_STATUS.md`
- `MAINTENANCE_GUIDE.md`
- `index.html`
- `aggie-engagement/`
- `assets/`
- `package.json`
- `server.mjs`

4. Understand the main files.

- root `index.html` = redirect page used as part of the GitHub Pages setup
- `aggie-engagement/index.html` = actual main webpage you will usually edit
- `aggie-engagement/styles.css` = styling for the main webpage
- `assets/` = website images

Do not delete or casually modify the root `index.html`.

5. Before starting a new task, open Codex and use this prompt:

```text
Read AGENTS.md, PROJECT_HANDOFF.md, PROJECT_STATUS.md, and MAINTENANCE_GUIDE.md before making changes. Then inspect the files relevant to my request. Do not change anything until you understand what I am asking.
```

6. After Codex has read the documentation, describe the change you want in normal language. You do not need to know HTML or CSS terminology.

## Using Codex to Help Maintain the Website
Codex is an AI coding assistant that can help you maintain the website without needing to know all the technical details yourself.

Codex can help with:

- reading the existing website code
- updating text
- changing links
- replacing images
- changing contact information
- adjusting layout or spacing
- adding or removing sections
- troubleshooting problems
- explaining technical steps in simple language

You can describe changes in normal language. For example:

- "Change the Community Outreach paragraph to this text..."
- "Replace the Strategic Partnerships image with this new image."
- "Update the contact email in the footer."
- "Make this section have a little more spacing on mobile."

Before every change, tell Codex to:

- read the project documentation
- inspect the relevant existing files
- make only the requested change
- avoid unrelated edits
- not commit or push until you approve

Reusable safe-change prompt:

```text
Read the project documentation first and inspect the existing files related to this request. Make only the change I ask for and preserve the existing design and functionality. Do not modify unrelated files. Do not commit or push anything until I review the result. After making the change, tell me exactly what files you changed and what you changed.
```

For visual changes, you can describe what feels wrong instead of knowing CSS terms. For example:

- "This feels too crowded."
- "The image looks awkward here."
- "I want this to feel cleaner and more professional."

Codex should translate that feedback into the technical changes.

If Codex proposes something you do not understand, ask it to explain before approving. Useful questions include:

- "Will this affect the live website?"
- "What files will this change?"
- "Can we do this in a smaller/simpler way?"

Safety note: Do not tell Codex to force-push, rewrite Git history, delete large parts of the repo, change hosting configuration, or add new frameworks/dependencies unless there is a clear reason and you understand the impact. For normal content/design updates, targeted HTML/CSS edits are usually enough.

Codex does not need access to old conversations. The project knowledge it needs is stored in `AGENTS.md`, `PROJECT_HANDOFF.md`, `PROJECT_STATUS.md`, and this guide.

## Previewing the Website Before Publishing
Before publishing a change, preview the website on your own computer.

A local preview lets you see the website privately on your computer. Changes in the local preview are NOT automatically live on the public website. This is where you should check changes before publishing them.

1. Open the terminal in Visual Studio Code.

Use `Terminal > New Terminal`.

Make sure the terminal is opened from the full repository root. The prompt/path should correspond to the cloned `aggie-engagement-landing-page` repository folder.

2. Start the preview.

Run:

```text
npm start
```

This starts the project's local preview server. Do not close that terminal while you are actively using the preview.

3. Open the preview.

In a web browser, go to:

`http://localhost:5173/aggie-engagement/`

`localhost` means the website is being viewed from your own computer, not from the public internet.

4. Check the website.

Look at:

- the specific change you requested
- spelling/text
- images
- buttons and links
- spacing/layout
- desktop appearance
- mobile or narrow-window appearance when relevant
- whether unrelated parts of the website still look normal

5. If the preview does not start.

Try these simple checks:

- confirm Node.js was installed
- close and reopen Visual Studio Code if Node.js was just installed
- confirm you opened the full repository root
- run `npm start` again
- copy the error message into Codex and ask Codex to explain or fix it

Do not randomly delete files or change project configuration to solve an error.

6. Stop the preview.

Return to the terminal running the preview and press `Ctrl+C`.

This stops the local preview server and does not affect the live website.

Important safety note:

- Previewing locally does not publish the change.
- Committing a change does not by itself publish it.
- Pushing an approved commit to the `main` branch is the step that can trigger the GitHub Pages production deployment.

## Making a Website Update
Use this workflow every time you update the website, even for small changes. It helps prevent accidental changes to the live production site.

1. Start from the repository root.

Open the full `aggie-engagement-landing-page` repository in Visual Studio Code. Do not work from only the `aggie-engagement` subfolder.

2. Make sure the project is current before editing.

Before starting, make sure your computer has the newest version from GitHub.

Run:

```text
git status
```

If it says the working tree is clean, run:

```text
git pull origin main
```

`git pull` downloads newer changes from GitHub.

If `git status` shows existing changes you do not recognize, STOP and ask Codex or another maintainer for help before pulling or editing. Do not discard those changes.

3. Start Codex.

Have Codex read the project documentation first. Use the safe-change prompt already provided in this guide, then describe the requested update in normal language.

4. Let Codex inspect before editing.

Codex should identify the relevant existing files before changing them. For most main-page content changes, this will involve `aggie-engagement/index.html`. Styling changes generally involve `aggie-engagement/styles.css`. Images generally live in `assets/`.

The root `index.html` is the redirect page and normally should not be changed.

5. Make only the requested change.

Avoid unrelated cleanup or rewrites. Preserve the existing design and functionality. Do not commit or push yet.

6. Review what Codex changed.

Ask Codex exactly which files changed and what was changed.

Run:

```text
git status
```

`git status` shows which local files have changed. Make sure only expected files appear.

7. Preview the website.

Run:

```text
npm start
```

Open:

`http://localhost:5173/aggie-engagement/`

Review the requested change and make sure unrelated sections still look normal.

8. Revise if needed.

If something is not right, describe it to Codex and let Codex make another targeted adjustment. Preview again. Repeat until you are happy with the result.

9. Final check before publishing.

Ask Codex to perform a read-only review of the changes. It should check for accidental unrelated edits, broken paths or links, obvious HTML/CSS issues, and confirm exactly what would be committed.

Do not publish until you understand and approve the final change.

## Publishing Changes to the Live Website
Publishing means sending an approved change to GitHub so it can become part of the live website.

Only publish after:

- the change has been reviewed locally
- you have checked `git status` and understand which files changed
- the local preview looks correct

1. Do a final status check.

Run:

```text
git status
```

Confirm that only the expected files are listed. If unexpected files appear, STOP and review them before continuing.

2. Stage only the intended files.

Staging selects which changed files will be included in the next saved Git version.

Explicitly name the intended files instead of blindly staging everything. For example:

```text
git add aggie-engagement/index.html aggie-engagement/styles.css
```

The exact file names will depend on what was changed. You can ask Codex to give you the exact `git add` command for the files that should be included.

3. Check again.

Run:

```text
git status
```

The intended files should now appear as ready to be committed.

4. Commit the change.

A commit is a saved checkpoint in Git.

Use:

```text
git commit -m "Short description of the update"
```

Example:

```text
git commit -m "Update Community Outreach content"
```

The commit message should briefly describe the change.

5. Push to GitHub.

Before pushing, remember:

- the production branch is `main`
- GitHub Pages deploys from `main` / repository root
- pushing the commit to `main` can update the public website

Run:

```text
git push origin main
```

6. Confirm the push.

A successful push will normally show output indicating `main` was pushed to `main`.

Run:

```text
git status
```

The normal final state should say the branch is up to date and the working tree is clean.

7. Verify the live website.

Open:

`https://aggie-engagement.github.io/aggie-engagement-landing-page/`

GitHub Pages may take a short amount of time to deploy. Refresh the page and confirm:

- the requested change appears
- images and links still work
- unrelated sections still look normal

8. If the live site does not update immediately.

- wait briefly and refresh
- check the repository on GitHub to confirm the commit appears on `main`
- check the GitHub Pages/Actions deployment status if necessary
- ask Codex to help inspect the issue instead of making random additional changes

Important safety rules:

- do not force-push
- do not push changes you have not reviewed
- do not include unrelated files in a commit
- do not share GitHub passwords or tokens
- if you are unsure what is about to be published, stop and ask Codex to perform a read-only review first

## Common Website Updates
Use this as a quick reference when you are not sure where a common change usually happens.

1. Updating text

What to ask Codex: update program descriptions, headings, button text, footer text, or other written content.

Usually involved: `aggie-engagement/index.html`

Caution: check spelling carefully and preview the website afterward.

2. Updating links

What to ask Codex: update a survey link, social media link, external Aggie Engagement link, or button destination.

Usually involved: `aggie-engagement/index.html`

Caution: test the link after publishing.

3. Updating contact information

What to ask Codex: update the email address, phone number, or location.

Usually involved: `aggie-engagement/index.html`

Caution: email links should use `mailto:` and phone links should use `tel:`. If you are unsure, let Codex handle the technical formatting.

4. Replacing an image

What to ask Codex: replace an existing image with a new one and update any related image description.

Usually involved: `assets/`, plus `aggie-engagement/index.html` or `aggie-engagement/styles.css`

Caution: use clear filenames, update alt text when appropriate, and do not delete the old image until confirming it is no longer used. Very large image files should ideally be web-optimized.

5. Changing spacing, colors, sizing, or layout

What to ask Codex: describe the visual issue in normal language, such as "this feels crowded" or "this looks too large on mobile."

Usually involved: `aggie-engagement/styles.css`

Caution: check both desktop and mobile/narrow-window views.

6. Adding or removing a section

What to ask Codex: add a new page section or remove an outdated section.

Usually involved: `aggie-engagement/index.html` and possibly `aggie-engagement/styles.css`

Caution: have Codex inspect similar existing sections first so the design stays consistent.

7. Updating buttons

What to ask Codex: change button wording, destination links, or button placement.

Usually involved: `aggie-engagement/index.html` and sometimes `aggie-engagement/styles.css`

Caution: check both the button wording and the destination link.

8. Updating social media

What to ask Codex: update footer social media names or URLs.

Usually involved: `aggie-engagement/index.html`

Caution: verify the exact destination URL before changing it. The current LinkedIn URL should be checked carefully before editing because its existing slug looks typo-prone but may still be the correct live URL.

9. Root redirect page

What to ask Codex: only change this if the GitHub Pages/deployment structure changes.

Usually involved: root `index.html`

Caution: this is not the normal page to edit. It supports the GitHub Pages structure. Do not change or delete it for normal content/design updates.

10. Local preview files

What to ask Codex: only change these if the local preview setup needs to change.

Usually involved: `package.json`, `package-lock.json`, and `server.mjs`

Caution: these files normally do not need to be changed for content/design updates.

If you are unsure which file needs to change, describe the goal to Codex and let Codex inspect the repository before editing.

## If Something Goes Wrong
Most problems are easier to fix if you stop before committing or pushing. Use the notes below when something does not look right.

1. Codex made a change that looks wrong.

- do not commit or push it
- ask Codex what files it changed
- run `git status`
- ask Codex to explain the change in plain language
- ask Codex to make a smaller targeted correction
- preview again before publishing

2. There are files changed that you do not recognize.

- STOP before pulling, committing, or pushing
- run `git status`
- ask Codex for a read-only explanation of every changed file
- do not delete or discard unfamiliar changes without understanding them first

3. `git pull` gives an error or conflict.

- do not force anything
- copy the exact terminal message into Codex
- ask Codex to inspect the situation without modifying anything first
- if another staff member may be working on the site, confirm with them before resolving conflicting changes

4. `npm start` does not work.

- confirm Node.js is installed
- restart Visual Studio Code if Node.js was just installed
- confirm the full repository root is open
- confirm the terminal is running from the repository root
- copy the exact error into Codex
- do not randomly edit `package.json`, `package-lock.json`, or `server.mjs`

5. The local preview looks right but the live site looks wrong.

- confirm the correct commit was pushed to `main`
- check GitHub Pages / Actions deployment status
- wait briefly and refresh the live page
- confirm the live URL is `https://aggie-engagement.github.io/aggie-engagement-landing-page/`
- ask Codex to inspect the issue before making more changes

6. A link or image is broken.

- check the exact URL or filename
- remember file paths and filenames must match exactly
- ask Codex to inspect where the link or image is referenced
- do not rename or delete multiple assets while troubleshooting

7. A bad change was already pushed live.

- do not force-push or rewrite Git history
- ask Codex to inspect the recent Git history and identify the safest way to correct or revert the specific change
- review and preview the correction before pushing again
- remember that Git history usually allows previous versions to be recovered

8. GitHub access does not work.

- confirm you are signed into the correct individual GitHub account
- confirm the invitation to the `aggie-engagement` organization/repository was accepted
- contact an existing organization Owner if access needs to be changed
- do not use another person's password

9. When to ask for help.

Stop and get help before proceeding if:

- you do not understand what will be published
- Git reports a conflict
- important files appear missing
- hosting or GitHub Pages settings appear changed
- someone suggests force-pushing or deleting Git history
- you are unsure whether you are working in the correct repository

Stopping before committing or pushing is safe. Local changes can usually be inspected or corrected without affecting the public website.

## Important Things to Know
Keep these project-specific facts handy:

1. The Git repository root is the full `aggie-engagement-landing-page` folder. Do not treat `aggie-engagement/` as a separate repository.

2. The actual main webpage is `aggie-engagement/index.html`.

3. The main stylesheet is `aggie-engagement/styles.css`.

4. The root `index.html` is a redirect page used by the GitHub Pages structure. Do not delete or casually modify it.

5. Shared images are stored in `assets/`.

6. From the main webpage, image paths commonly use `../assets/...`.

7. Local preview uses `npm start`.

8. Local preview URL: `http://localhost:5173/aggie-engagement/`

9. Production hosting uses GitHub Pages. The production branch is `main`, the source is the repository root, and pushing to `main` can affect the public site.

10. Live website: `https://aggie-engagement.github.io/aggie-engagement-landing-page/`

11. The site is simple static HTML/CSS. It has no frontend framework, no JavaScript-driven behavior, no external font setup, and normal content/design updates usually do not require new dependencies.

12. Hardcoded items in the main page may need maintenance over time: contact email, phone, location, social links, survey/form link, external Aggie Engagement page link, and program names/descriptions.

13. No staff names are currently hardcoded into the webpage.

14. Known maintenance notes: verify external links periodically; be careful with the LinkedIn URL because the current slug looks typo-prone but may still be valid; the footer `Logan, Utah` link is somewhat placeholder-like and may be worth reviewing later; `sagebrushawardphoto.jpg` is unusually large and should ideally be replaced or compressed with a web-optimized version in the future; if deployment structure is ever changed, re-check the root redirect behavior.

15. Project knowledge should live in the repository documentation rather than depending on one person's memory or previous ChatGPT/Codex conversations.

## Access and Ownership
The website is stored in GitHub under:

- Organization: `aggie-engagement`
- Repository: `aggie-engagement/aggie-engagement-landing-page`

Each staff member should use their own GitHub account. Do not share passwords, recovery codes, or personal access tokens. Do not rely on one person's personal login for long-term access.

At least two appropriate permanent staff members should have Owner access to the `aggie-engagement` organization. Owners can manage organization access, which is important for continuity if one person leaves.

Do not remove an existing Owner until the replacement access has been tested.

Before removing the previous maintainer, the new maintainer should personally confirm they can:

- access the GitHub organization
- access the repository
- clone the repository to their own computer
- open it in Visual Studio Code
- run `npm start`
- view the local preview
- make a small test update
- review the change
- commit it
- push to `main`
- verify the GitHub Pages deployment

Only remove a previous maintainer after the successor has successfully completed the handoff test and appropriate permanent Owners are in place.

If the previous maintainer no longer needs access, remove their organization/repository access rather than sharing or changing their personal account credentials.

What is NOT required for ownership transfer:

- no separate hosting account needs to be transferred because GitHub Pages hosts the site
- no previous ChatGPT/Codex conversation history needs to be transferred
- no personal Visual Studio Code account needs to be transferred

If repository ownership, hosting setup, workflow, or important URLs change, update `AGENTS.md`, `PROJECT_HANDOFF.md`, `PROJECT_STATUS.md`, and `MAINTENANCE_GUIDE.md` so the next maintainer has accurate information.

## Quick Reference
Use this as a quick cheat sheet when maintaining the website.

Important locations:

- Repository: `aggie-engagement/aggie-engagement-landing-page`
- Main webpage: `aggie-engagement/index.html`
- Stylesheet: `aggie-engagement/styles.css`
- Images: `assets/`
- Root `index.html`: redirect page; normally do not edit
- Live site: `https://aggie-engagement.github.io/aggie-engagement-landing-page/`
- Local preview: `http://localhost:5173/aggie-engagement/`

Before starting an update:

```text
git status
git pull origin main
```

Only run `git pull origin main` when the working tree is clean. If unfamiliar changes appear in `git status`, stop and inspect them first.

Preview:

```text
npm start
```

Then open:

`http://localhost:5173/aggie-engagement/`

To stop preview:

```text
Ctrl+C
```

Before publishing:

```text
git status
git add [intended file(s)]
git status
git commit -m "Short description of change"
git push origin main
git status
```

Replace `[intended file(s)]` with the actual files that were changed. Do not blindly copy that placeholder into the terminal.

Safe Codex starter prompt:

```text
Read AGENTS.md, PROJECT_HANDOFF.md, PROJECT_STATUS.md, and MAINTENANCE_GUIDE.md first. Inspect the existing files related to my request. Make only the requested change and preserve existing design and functionality. Do not modify unrelated files. Do not commit or push anything until I review it. Tell me exactly what files you changed and what you changed.
```

If unsure:

- stop before committing or pushing
- run `git status`
- ask Codex for a read-only review
- never force-push
- it is safer to stop and inspect than guess
