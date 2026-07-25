# The Beaverton Run — Proposal Site

A password-gated, single-page proposal from **Ghost Note** for a brand foundation and launch system: a 5K and kids run centered on mothers, first event Beaverton, June 2027.

Built in the Ghost Note proposal-site format (lime / purple / cream on near-black, Playfair Display + DM Sans).

## Access

The site opens on a password gate.

**Access code:** `beaverton`

The gate is client-side only. It keeps the proposal from casual view, but it is **not** real security — the code lives in the page source. Don't treat it as protection for anything sensitive.

## What's in here

```
beaverton-run-proposal/
├── index.html        # the entire proposal — self-contained, no build step
├── README.md         # this file
├── netlify.toml       # Netlify deploy config (publishes root as-is)
└── .gitignore
```

Everything is in `index.html`: markup, CSS, and JS inline. Fonts load from Google Fonts. The cover image and the Ghost Note logo load from remote URLs (see **Assets** below).

## Run it locally

No build step. Open the file directly:

```bash
open index.html
```

Or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

### Netlify (drag-and-drop)
Drag the `beaverton-run-proposal` folder onto https://app.netlify.com/drop. Suggested site name: `gn-beaverton-run-proposal`.

### Netlify (from this repo)
Connect the repo. `netlify.toml` publishes the root directory as-is — no build command needed.

### GitHub Pages
Settings → Pages → deploy from branch, root folder. The site is a single static `index.html`, so it works as-is.

## Assets (remote references)

Two images load from external URLs rather than being bundled:

- **Cover image** (hero background): `https://i1.t4s.cz/galleries/667/428863.jpg`
- **Ghost Note logo** (gate, nav, footer): `https://www.ghostnoteagency.com/wp-content/uploads/2022/02/GN_2020_Logo-horizontal-small-1.png`
- **Team headshots**: loaded from `ghostnoteagency.com` (Fredo, Natalia, Reggie, Sarah). Aminta and Adam use initial-avatars.

If you want the site fully self-contained, download these into an `/assets` folder and update the URLs in `index.html`. The logo has a text fallback built in (`onerror`), so if the URL breaks, "Ghost Note" shows instead.

## Before sending

A few things to set:

1. **Project name.** "The Beaverton Run" is a working placeholder. Naming is a Phase 1 deliverable — swap it for whatever the client calls it (search-and-replace in `index.html`).
2. **Contact block.** Currently organization, name, title, email, website. Add phone or address if you want them.
3. **Aminta.** Listed by first name with an initial-avatar and a placeholder title ("Strategy Lead"). Add her surname, real title, and headshot URL if you have them.
4. **Cover image rights.** Confirm you have the right to use the hero photo before this goes public.

## Structure

Password gate → Nav (dropdown menu) → Hero → Agency → Executive Summary → Opportunity → Approach → Phases → Core Team (bio modals) → Project Management → Timeline (Gantt) → Investment → Assumptions → Contact → Footer.

## Pricing model

Single price: **$85,000** for Phases 1 + 2, structured as **$21,250/month across 4 months**. Phase 3 (marketing engine) is optional and scoped separately.

---

Confidential — prepared by Ghost Note, 2026.
