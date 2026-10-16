# GitHub profile README: research notes and results

Paste-ready file: `githubreadme_new.md` (goes in the repo `Suyashman/Suyashman`, file `README.md`).

## What I could and couldn't read

| Source | Result |
|---|---|
| GitHub profile + 23 public repos (API, READMEs) | Read. All project facts and metrics in the README come from here. |
| Portfolio site source (`my-portfolio/src/data/portfolio.js`) | Read. Education, location, email, older projects. |
| LinkedIn `/in/suyashsunam` | **Blocked** (HTTP 999). Nothing taken from it. |
| IEEE Xplore papers 11702370, 11323656 | **Blocked.** Titles/venues unknown, so they are placeholders. |

## Design decisions (from what recruiters and top profile READMEs do)

- **One screen of positioning, then proof.** Banner + typing line + 4 link badges, then a 3-line pitch. Recruiters skim.
- **Projects as a table with a measured result**, not a wall of badges. Numbers used are from your own READMEs
  (SAM3 F1 per class, FSRCNN 37.0 dB vs 33.66 dB bicubic, ~60 FPS).
- **Grouped skill icons** (skillicons.dev) instead of the old 25 loud shields, which read as filler.
- **Stats kept to one row** (stats + top languages). No trophies/streak/visitor counter: they highlight small numbers.
- **Sparkline** is described in general terms; no client names, no private code, no thresholds.
- Left out because you did not tick them: certificates, Codeforces, internship-assignment framing
  (the Apt and Tata Technologies repos appear only as plain projects).

## Fill in before pasting

1. Titles, venues and years of the **two IEEE papers** (search `[Paper 1 title]`).
2. Your **job title at Sparkline** if you want it shown (I wrote none).
3. Is "graduating 2027" right? Portfolio says 2023-2027.

## Things on your GitHub that hurt you more than the README helps

- **No pinned repos.** Pin: SAM3-Autolabeler, dataset-manager, worker-monitor, fsrcnn-dlss, SnakeNGen, advance-driver-assistance-system.
- **16 of 23 repos have no description or topics.** Add a one-line description plus topics (`computer-vision`, `yolo`, `pytorch`, `fastapi`).
- **`defect-detection` and `stock-price-prediction` are empty; `action-detection` has no README.** Fill, or make private.
- `sample1`, `SEM6-PRACTICALS`, `github-slideshow` look like clutter: archive or hide.
- Profile bio, location and name are blank. Set name, "ML / Computer Vision Engineer", Pune, link to suyashsunam.me.
- Old README linked the site with the text `suyash.sunam.me` but the URL `suyashsunam.me`. Fixed.

## Optional upgrades (not included, each adds setup)

- Animated contribution snake: needs a GitHub Action in the profile repo (`Platane/snk`).
- Dark/light aware banner via `<picture>`.
- The stats mirror `github-readme-stats.shion.dev` was kept from your old README; if cards break, swap to
  `github-readme-stats.vercel.app`.
