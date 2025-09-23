# KGP-Wellness

KGP-Wellness is an IIT Kharagpur pilot proposal that combines RFID hostel attendance with a daily well-being check-in so administrators, counselors, and student mentors can intervene early with empathy. This repository contains the public-facing GitHub Pages deck that you can share with campus stakeholders.

## Project overview

- **Live hostel visibility:** Edge readers stream anonymised occupancy for muster-ready response.
- **Student-first wellness app:** A 30-second voluntary check-in powers trends, nudges, and help-on-call.
- **Explainable risk engine:** Human-in-the-loop scoring highlights sustained distress while preserving consent and privacy.
- **Dashboards for action:** Wardens see aggregates; counselors see individual alerts only when students opt in or emergencies arise.

## Repository structure

| Path | Description |
| --- | --- |
| `index.md` | Main narrative page pitched to campus administration, including the pilot plan, technical appendix, and diagrams. |
| `_layouts/default.html` | Custom Jekyll layout that provides typography, hero styling, and presentation-friendly components. |
| `_includes/head.html` | Shared head partial that loads MermaidJS and converts Mermaid fenced code blocks into rendered diagrams. |

## Preview the site locally

You can use Docker (recommended for a quick preview) or run Jekyll locally if you already have Ruby tooling installed.

### Option A – Docker

```bash
docker run --rm -it \
  -v "$PWD":/srv/jekyll \
  -p 4000:4000 \
  jekyll/jekyll:4.3 \
  jekyll serve --livereload --future
```

Then open `http://localhost:4000` in your browser.

### Option B – Local Ruby toolchain

1. Install Ruby (>= 3.0) and Bundler.
2. Install the GitHub Pages gem: `bundle add github-pages`.
3. Serve the site: `bundle exec jekyll serve --livereload`.

The custom head include automatically initialises Mermaid diagrams on every page load.

## Editing guidance

- Update the narrative in `index.md` to reflect programme changes; Markdown and inline HTML are both supported by the layout.
- Add new diagrams with fenced code blocks using the `mermaid` language hint—no additional scripts needed.
- Keep privacy, governance, and consent messaging front-and-centre when adapting content for new audiences.

## Deployment

Publishing to GitHub Pages is automatic—push to the default branch and GitHub will rebuild the site with the latest content and design.
