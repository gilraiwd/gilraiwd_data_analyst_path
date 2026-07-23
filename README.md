# Pivot Tracker

A personal, single-file web app for tracking a self-directed career transition: a 4-month checklist, portfolio project tracker, job search tools, and progress dashboard — all running entirely in your browser with no backend, no accounts, and no data collection.

**Live demo:** _add your GitHub Pages link here once it's deployed_

## What this is

I'm using this to track my own transition from a GIS Analyst role into Power BI / data analytics. It's built with AI assistance (Google Gemini for the initial concept, Anthropic's Claude for iteration and features) — I directed the build and made the product decisions, but I didn't write the code by hand. If you're looking at this as a coding sample, it isn't one; it's a personal tool I use, built with AI tools the same way I'd use any other software.

## Features

- **4-month checklist** with linked learning resources, organized by phase
- **Portfolio project tracker** for the hands-on projects that back up the skill claims
- **Live dashboard** — overall progress, pacing vs. a target timeline, exam countdown, and a skill radar chart that actually shifts as you complete related tasks (not just a static before/after)
- **Job search tab** — a skills-based live search (via a free public job board API) plus a fallback link to a live Indeed search built from your own keywords, salary target, and remote preference — all individually optional
- **Application pipeline log** with editable status stages (Targeted → Applied → Screening → Interview → Offer/Rejected)
- **Export/Import** — download your progress as a JSON backup, restore it on another device
- **Print/PDF view** for an offline copy of the checklist

## Privacy & data storage

Everything — your progress, your job title, your salary numbers, your target range, your application log — is stored **only in your browser's `localStorage`**. None of it is written into the site's code, none of it gets uploaded anywhere, and none of it is visible to anyone else visiting this page. That's also why the version of this file in the repo shows generic placeholder values (like "Current Role" and "$75,000") instead of anyone's real numbers — those are just defaults until someone fills in their own info via the "My Info" panel.

If you fork this and put in your own numbers, they stay on your device. If you clear your browser data or switch browsers, use the Export button first to back up your progress as a `.json` file.

## Setup

This is a static single HTML file — no build step, no dependencies to install.

1. Fork or clone this repo
2. Open `index.html` directly in a browser, **or**
3. Enable GitHub Pages: **Settings → Pages → Deploy from a branch → main / (root)**

## Tech

Tailwind CSS (CDN), Chart.js (CDN), Font Awesome (CDN), and vanilla JavaScript. No frameworks, no bundler, no package.json.

## Customizing for your own transition

The checklist, projects, and skill categories in this version are specifically built around a GIS-to-BI-Analyst pivot (Power BI, DAX, SQL, PL-300 certification). If you want to adapt this for a different transition, the task lists live in the `TASKS_DATA` object and the skill radar categories live in the `SKILL_TASK_MAP` object near the top of the `<script>` tag — everything else (dashboard, charts, job search, application log) is generic and will work for any transition once those are edited.
