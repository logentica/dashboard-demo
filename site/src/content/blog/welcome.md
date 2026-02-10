---
title: 'Welcome to Dashboard Demo'
description: 'A quick tour of what this dashboard demo includes and how to adapt it.'
pubDate: 2026-02-06
---

This project is a small, static site meant to be shared publicly: a landing page plus an example KPI dashboard.

## What's included

- Landing page at `/` (copy + CTA)
- Dashboard at `/dashboard` (KPI cards + a simple time-series chart)
- About page at `/about`
- Health endpoint at `/health` for ingress checks

## How to adapt the dashboard

The dashboard page is intentionally simple and uses a synthetic dataset.

- Update KPI labels/values in `site/src/pages/dashboard.astro`
- Swap the chart series with your own data (or embed a charting library)
- Adjust styling via `site/src/styles/global.css` (Tailwind components live there)

## Blog posts

Posts live in `site/src/content/blog/`. Keep them focused on the demo: what it shows, what to customize, and example use cases.

If you don't need a blog, remove the `/blog` route and the link in `site/src/components/Header.astro`.
