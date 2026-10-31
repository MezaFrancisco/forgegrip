# ForgeGrip logo — v2

## Status
v1 was a literal illustrated fist (hand-coded SVG anatomy) — rejected as amateurish/cartoonish,
proportions felt off. **v2 replaces it entirely** with an abstract geometric mark. Still a first
pass, still not visually proofed by a real design tool — react to it, don't treat it as final.

## Concept
Two overlapping circular forms — a **teal base** and a **volt disc breaking free of it**, with a
small cyan spark where it pulls away. Reads as momentum / breakthrough / progress pulling away
from a foundation — a training platform's actual promise — without illustrating anything literal.
A tiny diamond accent (rotated square) stands in for the mark in the wordmark-only fallback.

Deliberately simple: two circles and a dot is precise, safe geometry (no anatomy, no arcs to get
wrong), and pairs with confident, bold typography rather than competing with it.

## Files
| File | Use |
|---|---|
| `icon.svg` | Mark only, transparent background. |
| `app-icon.svg` | Mark on a rounded near-black tile — favicon / PWA / app-icon source. |
| `logo-lockup-dark.svg` | Icon + wordmark, for **dark** surfaces (cream wordmark). |
| `logo-lockup-light.svg` | Icon + wordmark, for **light/cream** surfaces (ink wordmark). |
| `icon-mono-black.svg` / `icon-mono-white.svg` | Single-ink, outlined so both forms stay legible. |
| `wordmark-only-dark.svg` / `wordmark-only-light.svg` | **Fallback with the icon dropped entirely** — pure typography + a tiny diamond accent, if the circle mark still isn't landing. |

## Palette (from `/Users/frank/code/forgegrip/index.html`)
Teal-deep `#0891B2` (base), volt `#A3E635` (breaking free), cyan `#22D3EE` (spark accent).
Wordmark: cream `#F4F0EB` / ink `#1A1A1A` depending on surface, "GRIP" always teal.

## Honest limitation
These are hand-authored SVG with no visual feedback loop during authoring — reliable for precise
geometry (circles, type) but not a substitute for an actual design tool or designer if this needs
to hold up as a permanent flagship mark. See the review page for a size/context test before using
anywhere real.
