# HISTORY//QUEST — Post-Classical (600–1450 CE)

A zero-build, offline-capable single-page English recall game based on the supplied 110-term study handout. Features **Recall Battle**, **MCQ Arena**, **SEQ Boss**, a 12-minute **Mock Exam**, a **25-round Rival Arena**, **Codex**, **AI grading** (bring your own OpenAI-compatible Chat Completions API), and **History & Backup**.

## Run locally

Open [`index.html`](./index.html) in a modern browser. No package manager, build, backend, or account required. All built-in offline grading functions without an API key.

## Publish with GitHub Pages

1. Create a **public** GitHub repository, suggested name `history-quest-post-classical`, with a `main` branch.
2. Upload `index.html`, `.nojekyll`, and `README.md` to the **root** of `main` (not inside another directory).
3. Open **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
4. Wait for GitHub to report the published website URL under **Settings → Pages**.

Expected conventional URL if hosted in the user account `jiuxiao-D` in repository `history-quest-post-classical` (NOT live until published):

`https://jiuxiao-d.github.io/history-quest-post-classical/`

After the initial setup, updates to `index.html` on `main` are automatically published by GitHub Pages.

See [GitHub's branch publishing guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

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