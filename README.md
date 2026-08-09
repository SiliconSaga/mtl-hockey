# MTL Hockey — site

The website for **Mountain Top League hockey** (West Orange, NJ). It's a plain, file-based Jekyll site every page is a simple text file you (or your AI agent) can edit. No logins to a website builder, no waiting on anyone else.

> **The easiest way to change anything: just ask your agent.**
> *"Update the Mites fee to $250."* · *"Add the TeamSnap registration links."* · *"Swap the Middle School team photo."*
> Then look over the PR it opens — every PR automatically gets a **preview site link and a visual diff** so you can see exactly what changes before it goes live.

## How the site is laid out

| You want to change… | Edit this file |
|---|---|
| Home page | `index.md` |
| Divisions, ages, fees, sign-up links | `_data/divisions.yml` (Home + Register update automatically) |
| Register page wording | `register.md` |
| Rink pages (maps, parking) | `rinks/*.md` |
| How It Works | `how-it-works.md` |
| FAQ questions & answers | `faq.md` |
| Contact info | `contact.md` |
| Menu | `_data/nav.yml` |
| The colors and look | `_sass/_base.scss` |
| Site title / description | `_config.yml` |
| Photos and images | `assets/images/` |
| **Flyers** (print/social) | `flyers/hockey-2026/` *(arriving with the flyer-kit migration PR)* — edit the HTML, then run `bash flyers/hockey-2026/export.sh` to regenerate the PDFs/PNGs in `exports/` |

## Previewing and publishing

- **Every PR gets a live preview**: a comment appears on the PR with a link to a full preview of the changed site, plus a visual diff against the current site. Review those, then merge — the live site updates within a couple of minutes.
- **Local preview** (optional): `bundle install` once, then `bundle exec jekyll serve` and open <http://localhost:4000/mtl-hockey/>.
- Publishing is merge-gated: nothing reaches the live site without a human merging a PR.

## The bigger picture

This is one of the Mountain Top League's per-sport sub-sites (soccer lives in [mtl-site](https://github.com/SiliconSaga/mtl-site)); the [Mountain Top League site](https://mountaintopleague.com/) remains the league-wide primer. Architecture notes live in `_docs/plans/`. CI (deploy + PR preview + visual diff) is shared via [volundr](https://github.com/SiliconSaga/volundr).
