# Bastion — Cinematic Scroll Site

A premium scroll-driven cinematic site for **Bastion** (bastion.nyc), a by-referral career
advisory firm placing into tier-one finance and consulting — built with the
`cinematic-scroll-site` engine. World: *a vault at dusk where one gold ember proves the
stronghold was built from fire.* Luxe Dark / Atelier fortress-heraldic crossed with Editorial
Heritage. Their white page, inverted to stone-and-gilt.

## Identity (authored fresh in `skin.css`)
- **Type:** Cormorant Garamond (display, italic motto/eyebrows) + Inter (body, labels, UI).
- **Color:** bg `#0E0F10` / `#08090A`, panel `#15171A`, ink/bone `#ECE7DC`, muted `#8A8A82`,
  single accent **forge-gilt `#CB8E33`**, hairline `#2A2926`.
- **Device:** the **embrasure rule** (a gilt hairline notched with crenellations) and the
  **gilt corner-bracket**, both abstracted from the real logo's crenellated tower.
- **Logo:** the real `bastion.nyc/Full Logo.png` (verified), prepared in two treatments of the
  *same* mark — `logo-bone.png` (knockout, for dark surfaces) and `logo-gilt.png` (forge-gilt
  wordmark). The crenellated tower is also traced to `crest.svg` / `crest-gilt.svg` for the
  favicon, the embrasure device, and the staff monogram.

## Pages
- `index.html` — masthead, 5 film chapters, the Placement Wall, doctrine band, The Seal CTA.
- `stronghold.html` — About (heraldry + self-description; honest gaps left as silence).
- `wall.html` — the dedicated Placement Wall (21 names, verbatim disclaimer, load-bearing).
- `staff.html` — Staff page, re-conceived as *By Referral* (no named people; the firm publishes none).
- `reviews.html` — Reviews page, re-conceived as *The Summons* (no public reviews; none invented).

## Run locally
```
python3 serve.py 8913
```
Then open http://localhost:8913/.

## Film
The 5 scroll chapters are real scroll-scrubbed frame sequences — **144 frames each at
1920×804**, extracted from 4K Veo 3.1 clips (`quality:"ultra"`, 16:9, 6s) into
`assets/frames/<seq>/`. Source clips are kept in `assets/clips/` and the source job IDs:
- `ex-igne`     — d5a10f90-7961-4d32-a50b-24e843160d74
- `the-wall`    — f4e0d9b5-58f2-478e-8492-0a0d478a947c
- `the-keep`    — 3ee5fe52-158e-461c-925b-344dfc583824
- `the-skyline` — 1d1b502b-6d3d-451c-be95-bb1586a4d49a
- `the-ledger`  — 580cfe7d-5d25-4faa-9316-704e2dc43a51

To re-extract: `./extract.sh <seq> assets/clips/<seq>.mp4`
(STANDARD tier: `crop=3840:1608,scale=1920:804 -q:v 2`), then set each chapter's `data-count`
to the frame count in `index.html`.

## Notes
The **cinematic visuals are AI-generated and illustrative.** The Placement Wall reproduces the
firm's own stated placements verbatim, under the firm's own disclaimer ("Logos shown for
identification of placements only. No endorsement or affiliation implied."); no relationship
between Bastion and any named institution is implied. No founder, title, address, telephone,
rating, or review is published by the firm, and none is invented here — where the firm is
silent, so is this site.
