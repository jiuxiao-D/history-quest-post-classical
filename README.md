# HISTORY//QUEST v6 — Post-Classical History (600–1450 CE)

**Play the live game:** https://jiuxiao-d.github.io/history-quest-post-classical/

An offline-first, no-build English historical vocabulary game drawn from the user's 10-page, 110-term Post-Classical handout. The same 110 terms and 276 English rubric checkpoints power each mode.

## Daily vocabulary walkthrough (new in v6)

Before the first question of each local calendar day, the site automatically opens **📚 Vocabulary First**: 110 terms in their source-handout order, 10 definitions per page, 11 pages total. Each definition is visible, with an expandable list of PDF-derived English checkpoints. Mark each group of ten as reviewed before moving on. This is a study survey, not a scored quiz: no XP, mastery or flashcard schedule changes.

It gates **Recall Battle, MCQ Arena, SEQ Boss, Mock Exam, Rival Arena, and Flashcard Lab** until the daily survey is complete. History & Backup, Codex and AI Settings remain accessible. Progress is autosaved on each page, so navigation and reloading resume the same batch. After completing all 110, question modes become available until the next local day. The Vocabulary First button also allows optional extra browsing. The completed daily walkthrough is recorded in history.

## Study modes

- **🎴 Flashcard Lab (introduced in v5)**: Anki-inspired efficient review scheduling with keyboard shortcuts (Space / 1 / 2 / 3). Quick Flip, Active Recall (AI or offline English grading), and Reverse Cards. Every card reveals individual PDF-derived key ideas and offers two optional progressive hints.
- **⚔️ Recall Battle**: Explain a concept in your own English and receive checklist-based feedback.
- **🎯 MCQ Arena**: Mixed term-recognition and historical context questions.
- **✍️ SEQ Boss**: Free-response exam practice with individual rubric checkpoints.
- **⏱️ Mock Exam**: 10 MCQs, 2 SEQs, timed to 12 minutes.
- **🏆 Rival Arena**: 25 concept rounds with a simulated skill-matched rival and cross-match anti-repetition.
- **📜 Codex**: Browse all 110 concepts and mark favorites.
- **🗂️ History & Backup**: Keep per-answer history, scores and export/merge JSON backups.
- **⚙️ AI Settings**: Optional bring-your-own OpenAI-compatible chat-completions endpoint and model; the key stays in page memory only.

### Flashcard scheduling

Quick Flip cards are self-assessed after revealing the answer. Active Recall supports AI grading or offline fallback, followed by the user's final rating. Rate **Forgot** to revisit in five minutes (and again later in the current session); **Partial** to revisit in 30 minutes; **Know it** to begin at 1 day, then 3, 7, 14, 30+ days with subsequent successful recalls. A hint-assisted **Know it** rating is limited to **Partial**. Re-reviewing a non-due card doesn't fast-forward its interval. Flashcard reviews do not award XP; existing account XP stays intact. Use the **Due only** button to avoid studying new cards. The Daily Review screen prioritizes due reviews, recent mistakes from other modes, and new cards, with category balancing.

### Save migration / preserving history

- **Permanent browser storage key:** `history_quest_progress_stable`. Earlier `history_quest_110_v2` data is imported automatically on first load. Keep both keys and migration code in future updates.
- v5 extended the **existing v4 save** with `flashcards`, `flashSession`, `flashRecent` and `flashRewardClaims`. v6 adds `vocabWalk` (local date, daily completion and batch progress) to this same save, without changing XP, mastery, history, AI settings, Rival Arena rotation, or exam records.
- Refreshing mid-session resumes the current card, answer, hints and progress. Sessions can also resume after switching modes.
- Same hosted origin and browser normally preserve data across repository updates. Moving from `file://`, changing devices/browsers, using private mode or clearing site data does **not** automatically transfer progress.
- To transfer data: **History & Backup → Export complete backup**; then **Import / merge backup** on the destination. Version 4 and 5 backups remain importable. Same-day vocabulary walkthrough completion is retained when merging backups. Merges preserve existing events and prefer newer flashcard review schedules.
- Periodically export your JSON backup. The browser is **not** a server-side account or cloud-sync database.

## Local run and GitHub Pages deployment

Open `index.html` directly with Chrome or Edge; the built-in game is a self-contained single HTML file and works offline, including non-AI grading. No build tools are required.

This repository already has GitHub Pages enabled to **GitHub Actions**. The workflow `.github/workflows/pages.yml` deploys the root site automatically after every push to `main` (or via manual `workflow_dispatch`). No manual re-upload is necessary.

- [Live website](https://jiuxiao-d.github.io/history-quest-post-classical/)
- [GitHub Actions deployments](https://github.com/jiuxiao-D/history-quest-post-classical/actions/workflows/pages.yml)

## API key precautions

The API key is not written to local storage, backups, or this repository. Browser-side requests can still expose the token to the configured provider and browser extensions. Use a trusted CORS-capable provider or an authenticated personal proxy; usage charges may apply. Invalid or unreachable APIs revert to explicitly labeled offline rubric scoring.

Question simulations follow the supplied handout and are **not** official examination questions.