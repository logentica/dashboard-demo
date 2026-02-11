# Dashboard Demo

A lightweight static site (landing page + public KPI dashboard) deployed on the Buildville platform.

## Quick Start

1. **Update `values.yaml`** if the tenant/domain changes
2. **Customize the site** in the `site/` directory
3. **Push to GitHub** - deployment is automatic

## What's Included

- **Astro 5** - Fast static site generation
- **Tailwind CSS** - Utility-first styling
- **React** - Interactive components via Astro islands
- **Blog Support** - Markdown content collections
- **Responsive Design** - Mobile-first layout
- **SEO Ready** - Meta tags and Plausible analytics
- **One-Click Deploy** - GitHub Actions + ArgoCD

## What's NOT Included

- User authentication
- Database
- Backend API
- Payment processing

Need these? Use [opensaas-template](../opensaas-template) instead.

## Project Structure

```
dashboard-demo/
├── values.yaml           # Deployment config (update this!)
├── agents.yaml           # AI agent config (optional)
├── deploy.sh             # One-click deploy script
├── push.sh               # Manual build script
├── AGENTS.md             # Developer instructions
└── site/                 # Astro project
    ├── src/
    │   ├── pages/        # Your pages go here
    │   ├── components/   # Reusable components
    │   ├── layouts/      # Page layouts
    │   └── content/blog/ # Blog posts (Markdown)
    └── public/           # Static assets
```

## Development

```bash
cd site
npm install
npm run dev
```

Visit http://localhost:4321

## Deployment

Just push to `main`:

```bash
git add .
git commit -m "My changes"
git push
```

GitHub Actions will:
1. Build the Astro site
2. Create a Docker image
3. Push to the registry
4. ArgoCD deploys automatically

## Configuration

Edit `values.yaml`:

```yaml
namespace: dashboard-demo
site:
  name: "dashboard-demo"
  description: "Public-facing landing page + no-auth dashboard demo"
image:
  repository: "registry.buildville.cloud/buildville/dashboard-demo"
ingress:
  hosts:
    - host: "dashboard-demo.buildville.cloud"
```

## Adding Content

### New Page

Create `site/src/pages/contact.astro`:

```astro
---
import BaseLayout from '../layouts/BaseLayout.astro';
---

<BaseLayout title="Contact">
  <h1>Contact Us</h1>
</BaseLayout>
```

### Blog Post

Create `site/src/content/blog/my-post.md`:

```markdown
---
title: 'My First Post'
description: 'Hello world'
pubDate: 2026-02-06
---

Your content here...
```

## License

MIT
