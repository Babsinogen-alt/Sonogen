# Babsinogen

Clinical ultrasound decision-support tool for obstetric biometry, Doppler, anomaly markers, organ size, and **serial folliculometry**.

Live site: [https://babsinogen-alt.github.io/Sonogen/](https://babsinogen-alt.github.io/Sonogen/)

This is a **static GitHub Pages app**. Open `index.html` in a browser, or use the live URL. Nothing is sent to a server. Patient episodes stay on the device (IndexedDB / localStorage) and only after explicit consent.

## Edit the code on GitHub

1. Open [`index.html`](https://github.com/Babsinogen-alt/Sonogen/blob/main/index.html).
2. Click the pencil icon.
3. Commit the change.
4. GitHub Pages republishes in about a minute.

Other files:

| File | Role |
|---|---|
| `index.html` | The entire app (HTML, CSS, clinical engines, folliculometry) |
| `manifest.json` | Installable PWA name and icons |
| `sw.js` | Offline cache. Bump `CACHE_NAME` after a major change so visitors get the new version |
| `icon-192.png` / `icon-512.png` | App icons |

Do **not** upload `node_modules` or a `.zip`. GitHub Pages serves these files as-is.

## Modules

1. **Dating & EDD** — LMP (Naegele), CRL (Robinson & Fleming), MSD, ACOG 700 redating
2. **Biometry** — Hadlock EFW I–IV, head shape, growth centiles
3. **Doppler** — INTERGROWTH-21st UA-PI centiles, Mari MCA-PSV, CPR, uterine artery, ductus venosus
4. **Anomaly** — structured markers
5. **Folliculometry** — serial follicle tracking with cycle-aware, trend-based interpretation
6. **Organ size** — age-referenced measurements
7. **Reports & log** — printable summary; optional on-device save
8. **Quiz** — teaching bank including folliculometry

## Folliculometry

Interpretation is **trend-based**, not a 28-day calendar. Expected ovulation ≈ cycle length − luteal length (default 14 days, range 12–16). Ovulation is inferred from a **cluster of signs** (collapse, crenation, internal echoes, free fluid, corpus luteum, endometrial shift), never from follicle size or cycle day alone. Wording is conservative: “consistent with”, “probable”, “indeterminate”.

## Disclaimer

Decision support only. Not a substitute for clinical judgement, departmental protocol, or formal reporting systems.
