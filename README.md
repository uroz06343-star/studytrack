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
