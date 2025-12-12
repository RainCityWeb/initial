# Small Biz Site Factory

A simple, mobile-optimised website template for small businesses. Built with 11ty, Tailwind CSS, and Decap CMS.

## Features

- ✅ **Fully configurable** — all content in `site.json`
- ✅ **CMS-ready** — edit via `/admin` with Decap CMS
- ✅ **Mobile-first** — responsive Tailwind CSS
- ✅ **Accessible** — WCAG contrast, aria-labels
- ✅ **Fast** — static HTML, no runtime JS framework

## Quick Start

```bash
# Install dependencies
npm install

# Development (no CMS)
npm run dev

# Development with CMS
npm run dev:cms
# Then visit http://localhost:8080/admin

# Production build
npm run build
```

## Project Structure

```
src/
├── _data/site.json      # All content (business info, services, hours, etc.)
├── _includes/
│   ├── base.njk         # Base HTML layout
│   └── sections/        # Hero, About, Services, Hours, Location, Contact
├── css/style.css        # Tailwind CSS
└── index.njk            # Main page template

admin/
├── index.html           # CMS entry point
└── config.yml           # CMS field definitions
```

## Customizing Content

Edit `src/_data/site.json` directly or use the CMS at `/admin`.

**What's configurable:**
- Business name, tagline, description
- Services (with icons)
- Opening hours
- Location + map embed
- Contact info + social links
- Section titles
- CTAs
- Optional highlights

## Deployment

1. Push to GitHub/GitLab
2. Connect to Netlify
3. Enable Netlify Identity
4. Invite users to edit via CMS

**Netlify settings:**
- Build command: `npm run build`
- Publish directory: `_site`

## Local CMS Testing

The `dev:cms` script runs a local proxy so you can test the CMS without authentication:

```bash
npm run dev:cms
# Visit http://localhost:8080/admin
```

For production, set `local_backend: false` in `admin/config.yml`.

## Tech Stack

- [11ty](https://www.11ty.dev/) — Static site generator
- [Tailwind CSS v4](https://tailwindcss.com/) — Styling
- [Decap CMS](https://decapcms.org/) — Content management
- [Netlify](https://www.netlify.com/) — Hosting + Identity

## License

MIT
