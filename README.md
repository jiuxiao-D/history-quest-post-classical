# HISTORY//QUEST — Post-Classical (600–1450 CE)

A zero-build, offline-capable single-page English recall game based on the supplied 110-term study handout. Features **Recall Battle**, **MCQ Arena**, **SEQ Boss**, a 12-minute **Mock Exam**, a **25-round Rival Arena**, **Codex**, **AI grading** (bring your own OpenAI-compatible Chat Completions API), and **History & Backup**.

## Run locally

Open [`index.html`](./index.html) in a modern browser. No package manager, build, backend, or account required. All built-in offline grading functions without an API key.

## Publish with GitHub Pages

The site is already committed on the public `main` branch, and [the automatic deployment workflow](./.github/workflows/pages.yml) is installed.

### One-time required GitHub setting

GitHub does not allow the connected file-writing integration to enable Pages on your behalf. Repository owner must do this once:

1. Open **[Settings → Pages](https://github.com/jiuxiao-D/history-quest-post-classical/settings/pages)**.
2. Under **Build and deployment → Source**, select **GitHub Actions** (NOT "Deploy from a branch").
3. Save if requested.
4. Return to **[Actions](https://github.com/jiuxiao-D/history-quest-post-classical/actions/workflows/pages.yml)** and select **Run workflow**, or rerun the latest failed workflow.

The site will then be published at:

**https://jiuxiao-d.github.io/history-quest-post-classical/**

**Note:** the URL is not live until the Pages workflow successfully deploys. Once enabled, every change to `main` automatically republishes the latest game.

## Preserve your progress across versions

- The save database is stored in the browser's `localStorage` under the **permanent key** `history_quest_progress_stable`.
- The app automatically migrates legacy `history_quest_110_v2` progress on first launch. **Do not change these keys or remove migration functions in future versions.**
- Updating the hosted app at the **same URL and browser origin** preserves your stored local data by default.
- When moving between a downloaded file, GitHub Pages, browsers or devices, choose **History & Backup → Export complete backup** in the old version, then **Import / merge backup** in the new version.
- Import merges progress, records and arena history by event ID, instead of resetting prior data.
- Browser private modes, cleared site data, or storage limits can still erase local saves, so keep periodic exported JSON backups.
- Older versions that never saved individual answers cannot restore those earlier answers; previously tracked mastery, XP, and arena summary data can be imported.

## AI API safety

AI grading is optional. API credentials are entered in-memory during the session and are **not embedded in this repository**, exported in backups, or stored in `localStorage`. The configured AI endpoint and model preferences (but not the key) are saved in the browser. The API provider must permit browser CORS requests; any requests are billed according to that provider's terms. Do not commit API credentials to the repository or source code. A browser-accessible, user-supplied API key can still be exposed to local browser extensions or scripts; consider a constrained token/proxy if you use it broadly.

## Future updates

Edit the root `index.html` in the same repository. Keep the same GitHub Pages hostname and repository path and preserve schema migrations and the stable save key. Back up JSON before major releases.