# CLAUDE.md — ForgeGrip Marketing Site

Multi-page static site for **forgegrip.app** (GitHub Pages, `CNAME` = forgegrip.app). No build
step — plain HTML files sharing one `styles.css`, no framework.

**This is one of three places ForgeGrip lives.** See `## Related` below before assuming this repo
has the full picture.

## What's here

- `index.html`, `compete.html`, `membership.html` — the site. Each page is self-contained HTML
  (nav/footer/waitlist-form markup + the waitlist JS duplicated per page, since there's no build
  step to share it) but all link the same `styles.css`.
- `styles.css` — shared design system (CSS vars, nav/footer, buttons, section/card components).
  Was inline in `index.html` until 2026-10-30, when it got pulled out specifically so new pages
  could reuse it. Component classes worth knowing: `.showcase-row` (alternating screenshot+copy,
  used for feature deep-dives), `.proof-strip` (dark stat bar), `.cta-banner` (mid-page CTA),
  `.price-grid`/`.price-cell` (reused for both $ pricing and the non-$ membership tier cards).
- `shots/` — curated, resized screenshots from the live app, named by what they show (not by
  filename/timestamp). Source originals are in `screenshots-new/` (raw, unresized, added
  2026-10-30). Before using any of these in copy, verify build status in `forgegrip-app`'s
  `CHANGELOG.md` first — see the Compete/Membership pages note below for why that matters here.
- `logo/` — **v2 brand mark** (hand-authored SVG, teal-deep/volt/cyan, "two circles breaking free"
  concept). See `logo/README.md`. Self-described as a first pass, not design-tool-proofed.
- `ForgeGrip-Marketing-Pack/` — **Oct 27, 2026 brand refresh**, image-gen raster PNGs (cyan
  `#06B6D4` / lime `#A3E635`, "interlocking FG monogram" concept). See `START-HERE.txt` for what
  each of the 8 files is for and `CREATIVE-PROMPTS.txt` for how they were generated. Raster only —
  no vector master. Its palette already matches `index.html`'s `--teal`/`--volt` CSS vars exactly.
- `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`, `og-image.png`, `nav-icon.png`
  — added 2026-10-30, derived from `ForgeGrip-Marketing-Pack/03-app-icon-profile-avatar.png`
  (favicons + `nav-icon.png`, a tight 64×64 crop of just the monogram) and `07-website-hero.png`
  (og-image, cropped to 1200×630). Wired into `index.html`: favicon links + OG/Twitter meta tags
  in `<head>` (site had none before), and `nav-icon.png` as a small rounded-square chip
  (`.logo-icon`, 26px nav / 24px footer) placed before the existing text wordmark in both nav and
  footer — the text wordmark itself was kept, not replaced.
- `docs/` — sales playbook + founding-gym agreement (html/pdf exports).
- `screenshots/` — product screenshots, currently **not referenced** by `index.html` (unused asset
  pool, not dead files to delete without checking first).

## Related (the other two places)

- **App repo** (the actual product): `/Users/frank/code/forgegrip-app` — read **its** `CLAUDE.md`
  first for product/engineering state. That file's "RESUME HERE" section at the top is the current
  status.
- **Business docs & strategy**: `/Users/frank/notes/ob-notes/04_Business/MezaForge_projects/ForgeGrip/`
  — pitch decks, pricing, legal/structure, market research. Start at `ForgeGrip-Index.md` there.

## Compete &amp; Membership pages (added 2026-10-30)

Built from what's actually shipped in `forgegrip-app`, not from the original pitch — verified
against `CHANGELOG.md` and `docs/` before writing copy, because several things that *look* shipped
in that repo's planning docs turned out to be mockups:
- **HYROX competitions (marshal tap timing, big-screen display, per-station radar/benchmarks) are
  real and live** — migrations 0143–0182, confirmed in `CHANGELOG.md`. Safe to market as current.
- **The shareable public profile link is NOT live** — two separate changelog entries confirm
  "screenshot to share, public link coming later." Marked "Coming soon" on the Membership page, not
  presented as current.
- **The cross-gym "gap to the network" HYROX comparison is a concept visual, not a live feature** —
  the screenshot itself says "FORGEGRIP · not onboarded yet." Labeled as a future/concept view on
  the Compete page.
- **Skipped entirely**: a screenshot showing "Level 12 / Alpha Wolf / XP bar" on a rank card — the
  most recent `CHANGELOG.md [Unreleased]` entry explicitly says that exact combination isn't
  schema-backed ("no level, XP or title exists anywhere in the schema"), even though a *separate*,
  real Levels feature did ship (migration `0174`, Pup→Alpha Wolf, nobody's reached Alpha Wolf yet
  per the changelog's own projection). Too tangled to use without over-claiming — used a different
  screenshot (`rank-pack-standing.png`) and wrote copy only for the parts confirmed shipped (the
  rank ladder + "what closes the gap" mechanism).
- Also skipped: a 3-option (A/B/C) percentile-framing comparison image — that's internal design
  research, not a product screen.

No pricing numbers added anywhere on these two pages, per instruction — Performance is labeled
**Early Access** (matches `docs/DECISIONS.md` D-023), not priced.

## Open items (not resolved in this pass)

- **Two competing logo concepts** exist: `logo/` (v2, "breaking free circles") vs
  `ForgeGrip-Marketing-Pack/` (new, "interlocking FG monogram"). The marketing pack calls itself
  the "approved identity," which implies `logo/` is superseded — not yet confirmed with Francisco,
  and `logo/` has not been deleted.
  Note: despite different concepts, the two packs land on the same accent colors (cyan `#06B6D4`
  matches exactly, lime/volt `#A3E635` matches exactly) — likely because the image-gen prompts
  pulled the palette straight from this file's CSS.
- Marketing pack is raster-only. If this needs to go to print or exact reproduction, it needs a
  real vector master commissioned/refined from `02-logo-dark.png`.
