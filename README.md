# StudyTrack

A free student planner for homework, projects, exams and school tasks, with a focus timer, XP levels and a notebook-style Study Lab.

## Features
- One list for homework, projects, exams and school tasks, with search, filters and due-date countdowns
- Focus timer and XP levels
- Study Lab: add your own notes, then get answers, quizzes, flashcards, study guides and step-by-step math (needs an AI backend, see below)
- Device, light and dark themes
- Data stays in the browser (localStorage); no accounts

## Run locally
Open `site/index.html` in a browser. There is no build step.

## Deploy
Pushing to `main` deploys `site/` to GitHub Pages through `.github/workflows/pages.yml`.
In the repository, go to Settings > Pages and set Source to **GitHub Actions**.

## AI Study Lab
The Study Lab was built to run inside Claude, which supplies the AI. On GitHub Pages that connection does not exist, so the Study Lab shows an "unavailable" message while the planner works normally. To enable it on your own site, add a small server that holds your API key and forwards requests, then call it from `site/index.html`. Never put an API key in the page itself.

## Before you launch
The Terms of Use and Privacy text in `site/index.html` is a template. Replace the `[DATE]`, `[YOUR NAME / ORGANIZATION]`, `[YOUR COUNTRY/STATE]` and `[YOUR EMAIL]` placeholders and have a lawyer review it, especially for users under 13. Add a LICENSE file of your choice.

## Logo
Files in `site/`: `logo.svg`, `logo-512.png`, `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` and `social-preview.png` (1280x640). Upload `social-preview.png` under the repo's Settings > General > Social preview so links to the repo show the logo.

## Selling StudyTrack
Working plan: free planner, paid Pro plan (AI Study Lab and sync). Done: pricing section, Terms/Privacy/Refund pages, waitlist button (set `WAITLIST_URL` in `site/index.html` to a form link). Next: accounts, payments through a merchant-of-record provider, and an AI server with per-user limits.
