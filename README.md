# GATE 2027 CSE Prep Tracker

A minimal, mobile-first tracker for GATE 2027 CS preparation. Single static HTML
file, no build step, no backend — all data stays in your phone's browser
(`localStorage`).

## Deploy to GitHub Pages

1. Create a new GitHub repository (public or private, Pages works with both on
   most plans).
2. Add `index.html` to the root of the repository (rename if needed — it must
   be called `index.html` for Pages to serve it at the site root).
3. Commit and push.
4. In the repo, go to **Settings → Pages**, set **Source** to the branch you
   pushed (usually `main`) and folder `/ (root)`.
5. Wait a minute for Pages to build, then open the URL GitHub gives you
   (something like `https://yourusername.github.io/your-repo/`) on your phone.
6. Optional: add it to your Android home screen (browser menu → "Add to Home
   screen") so it opens like an app.

No other configuration is needed — there's no build tool, no base-path
setting, and nothing to install.

## Data & backups

Everything is stored in your browser's `localStorage`, scoped to that exact
URL. That means:

- Clearing your browser's site data for that URL erases your tracker.
- Using a different browser or device starts fresh.
- Use **Settings → Export data** every so often to download a
  `gate-2027-backup.json` file, and **Import data** to restore it (same
  device or a new one).

## Editing later

The whole app is one file (`index.html`) with plain HTML/CSS/JS — no
dependencies, no package manager. Open it in any editor to tweak subjects,
checklist items, or styling; the `SUBJECTS` array and the `PHASE*_FIELDS`
arrays near the top of the `<script>` block control what shows up in each
phase.
