# HISTORY//QUEST v8 — Story Theater + Post-Classical History (600–1450 CE)

**Play the live game:** https://jiuxiao-d.github.io/history-quest-post-classical/

An offline-first, no-build English historical vocabulary game drawn from the user's 10-page, 110-term Post-Classical handout. The same 110 terms and 276 English rubric checkpoints power each mode.

## 🎞 Story Theater (new in v8)

The previous Story Mode has been **fully replaced** by a responsive PPT-like **36-slide visual presentation**, organized into **9 connected historical chapters**. The presentation references every one of the **110 vocabulary terms** from the handout at least once. Each slide displays **up to three short bullets** beside a large, custom SVG illustration (trade routes, empires, canals, hierarchies, timelines, splits, shipping, farms or conceptual networks).

Slide-specific, source-grounded **English speaker notes** are kept in a collapsible transcript so the slideshow remains clean and visually focused. A small memory hook reinforces each idea.

**Voice playback:**
- **🔊 Read this slide** reads a single slide without advancing.
- **▶ Auto-play** narrates a slide and moves to the next one **when the browser speech engine reports that the narration has finished**, not on a fixed timer. The play session concludes on the final slide.
- **⏸ Pause / ▶ Resume** suspends or resumes the current speech utterance. **Voice speed** offers 0.8×, 1.0×, 1.15×, or 1.3×. Use **Previous/Next**, chapter navigation, or the keyboard arrow keys.
- Playback must be started by user interaction because browsers restrict unsolicited speech. Text-to-speech requires browser support; the full spoken script remains accessible without sound.

Progress through the story is saved in the existing local browser save. Watching slides does not change quiz results, flashcard review schedules, or XP. There is **no mandatory vocabulary/story gate** to enter practice.

## Optional vocabulary walkthrough

**📚 Vocabulary Walkthrough** remains available as an optional survey of the original **110 terms**, 10 at a time, with their English definitions and expandable PDF-derived recall checkpoints. You may skip it entirely and go straight to Recall Battle, MCQ, SEQ, Mock Exam, Rival Arena or Flashcard Lab. Walkthrough progress remains saved as before.

## Study modes

- **🎞 Story Theater (new in v8)**: Narrated visual slide presentation, auto-advance by speech end, 36 slides and 110 terms.
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
- v5 extended the **existing v4 save** with `flashcards`, `flashSession`, `flashRecent` and `flashRewardClaims`. v6 added `vocabWalk` (local date and progress), v7 added story chapters, and v8 adds a separate `story.slide` and `story.visitedSlides` progress field. All of these remain on the same stable save key and preserve XP, mastery, history, AI settings, Rival Arena rotation, and exam records.
- Refreshing mid-session resumes the current card, answer, hints and progress. Sessions can also resume after switching modes.
- Same hosted origin and browser normally preserve data across repository updates. Moving from `file://`, changing devices/browsers, using private mode or clearing site data does **not** automatically transfer progress.
- To transfer data: **History & Backup → Export complete backup**; then **Import / merge backup** on the destination. Version 4 and 5 backups remain importable. Vocabulary walkthrough completion and story visits are retained when merging backups. Merges preserve existing events and prefer newer flashcard review schedules.
- Periodically export your JSON backup. The browser is **not** a server-side account or cloud-sync database.

## Local run and GitHub Pages deployment

Open `index.html` directly with Chrome or Edge; the built-in game is a self-contained single HTML file and works offline, including non-AI grading. No build tools are required.

This repository already has GitHub Pages enabled to **GitHub Actions**. The workflow `.github/workflows/pages.yml` deploys the root site automatically after every push to `main` (or via manual `workflow_dispatch`). No manual re-upload is necessary.

- [Live website](https://jiuxiao-d.github.io/history-quest-post-classical/)
- [GitHub Actions deployments](https://github.com/jiuxiao-D/history-quest-post-classical/actions/workflows/pages.yml)

## API key precautions

The API key is not written to local storage, backups, or this repository. Browser-side requests can still expose the token to the configured provider and browser extensions. Use a trusted CORS-capable provider or an authenticated personal proxy; usage charges may apply. Invalid or unreachable APIs revert to explicitly labeled offline rubric scoring.

Question simulations follow the supplied handout and are **not** official examination questions.