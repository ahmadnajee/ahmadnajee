# Ahmad Naji — Profile setup

This package contains a redesigned profile README, a custom SVG banner, and a workflow that generates light and dark contribution animations. Your live GitHub repositories have not been modified.

## 1. Install the profile files

Open https://github.com/ahmadnajee/ahmadnajee and add these three paths to its main branch, preserving the directories:

- README.md (replace the current profile README)
- assets/header.svg
- .github/workflows/contributions.yml

Do not upload this whole folder as a nested directory. The README must be at the repository root. The workflow must be under .github/workflows. You do not need to upload this setup guide.

The easiest method is to clone the profile repository, copy the files into the matching paths, then commit and push using VS Code Source Control. Alternatively use GitHub's file editor and enter each complete path when creating the files. Windows may hide folders beginning with a dot; ensure .github is included.

## 2. Generate the contribution visual

After uploading the workflow to main:

1. Open the repository's Actions tab.
2. Select “Refresh contribution animation”.
3. Choose “Run workflow”, select main, then run it.
4. Wait for a successful run and refresh your profile.

The animation links will only work after the first successful run. The workflow is configured to refresh daily at 02:23 UTC (06:53 in Afghanistan), although GitHub may delay scheduled jobs. It uses GitHub's automatically provided GITHUB_TOKEN; no personal access token is needed.

Images are published to a dedicated profile-assets branch. Reserve that branch for these generated files: the publish step manages its contents. Do not use it for project source code. The workflow does not publish a website, and GitHub Pages does not need to be enabled. Automatic commits use the GitHub Actions bot.

If a run is blocked, inspect its log. The repository must permit GitHub Actions and the third-party actions used here. An organization policy or protected asset branch can also prevent publication. For a public repository, GitHub can disable scheduled workflows after 60 days of inactivity; enable the workflow again if necessary.

This graphic reuses your contribution calendar as an animation. It does not change or recolor GitHub's built-in calendar. GitHub continues to calculate the actual contribution counts.

## 3. Curate your pinned repositories

On your GitHub profile, choose “Customize your pins”. Select and drag the repositories into this suggested initial order:

1. OmniFood
2. Weather-Application
3. Pig-Game
4. 100-Day-with-Python

This is a starting presentation order based on the kinds of projects, not a review of their source-code quality. Move your strongest working, documented, original application to position one. Replace a learning exercise with your MERN project when it is ready to share. Keep a learning collection as a supporting pin. GitHub allows up to six pinned repositories and gists combined; four strong ones are sufficient.

Pinning controls the profile Overview section. It does not reorder the entire Repositories tab. The featured links in README are a separate curated selection.

## 4. Make each featured repository worth opening

The checked root README.md paths for OmniFood, Weather-Application, and Pig-Game returned 404. This does not rule out differently named documentation. Add or improve a visible README for each project before making it a main portfolio piece.

For each featured project:

- Add one sentence in the repository About field explaining what the app does.
- Add a working live-demo link if you have deployed it.
- Add relevant topics, based on the actual stack (for example javascript, react, or python).
- Include a clear screenshot near the top of its README.
- Explain the problem, working features, and technologies used.
- Give exact installation and run instructions, including required environment variables with example values only.
- Label the current status: in progress, working demo, or maintained.
- Credit the course or tutorial when applicable, then describe your own changes.

Repository README structure:

1. Project name and one-sentence purpose
2. Screenshot and live demo
3. Features that currently work
4. Tech stack
5. Local setup and run commands
6. What I built or changed
7. Known limitations and next steps
8. Credits and license, when applicable

The existing 100-Day-with-Python README has an unclosed shell code block and a progress section labeled Days 01–11. Fix the formatting and update the progress against the actual files; do not claim all 100 days are complete unless they are.

Do not delete practice repositories just to make the profile look tidier. Use curated pins to guide visitors. Consider archiving a repository only when it is genuinely inactive and you want to make that status clear.

## 5. Keep the profile accurate

The supplied profile keeps your stated MERN project and current Django/Next.js learning. Change those lines when your focus changes. Remove any technology you cannot yet discuss or demonstrate. Project descriptions are deliberately modest because source code was not audited.

The banner is a local SVG, so it does not depend on a banner-generation service. The two contact badges use shields.io. The animation depends on its GitHub Actions run and the Platane/snk generator. No live statistics or star counts are invented.

## References

- Pin and reorder repositories: https://docs.github.com/en/account-and-profile/how-tos/profile-customization/pinning-items-to-your-profile
- Contribution animation generator: https://github.com/Platane/snk
- Asset publisher and its configuration: https://github.com/crazy-max/ghaction-github-pages
- Workflow syntax: https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax
- Scheduled workflow inactivity behavior: https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule
