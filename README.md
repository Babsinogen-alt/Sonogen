# Babsinogen

Clinical decision-support for obstetric biometry, Doppler, anomaly markers, organ size, and **serial folliculometry**.

Live site: [https://babsinogen-alt.github.io/Sonogen/](https://babsinogen-alt.github.io/Sonogen/)

This repository is a **static GitHub Pages app** (`index.html` plus icons). Open the file in GitHub and use the pencil icon to edit. Nothing is sent to a server — measurements stay in the browser (optional IndexedDB log, local folliculometry series).

## Modules

1. **Dating & EDD** — LMP (Naegele), CRL (Robinson–Fleming), MSD fallback, ACOG/AIUM/SMFM Committee Opinion 700 redating, FHR ranges
2. **Biometry** — HC / cephalic index / shape-corrected BPD, Hadlock I–IV EFW, Hadlock 1984 GA, growth centiles 24–41 weeks
3. **Doppler** — UA-PI (INTERGROWTH-21st LMS centiles), AEDF/REDF, MCA-PSV (Mari), CPR, uterine artery, ductus venosus
4. **Anomaly** — structured markers (CNS, NT, chest, renal, liquor, placenta)
5. **Folliculometry** — serial follicle tracking, cycle-aware interpretation (natural / irregular / OI / IUI / ART), ovulation-sign scoring, endometrial correlation, end-of-tracking impression
6. **Organ size** — age-graded references
7. **Reports & Log** — printable summary; optional on-device save with explicit consent
8. **Quiz** — six topical banks, 20 clinical-scenario questions each (Dating, Biometry, Doppler, Anomaly, Folliculometry, Gynaecology & organ size)
9. **References** — bibliography for every formula and threshold used in the app

## Folliculometry (how it thinks)

- Trends over time matter more than a single diameter.
- Expected ovulation ≈ **cycle length − luteal length** (default luteal 14 days, typical 12–16). A 28-day cycle is **not** assumed.
- Mature/pre-ovulatory size is a **range** (often ~18–25 mm in natural cycles; stimulated trigger size is protocol-dependent, often ~16–22 mm).
- Ovulation is inferred from a **cluster of signs** (collapse or ≥30% shrinkage, crenation, internal echoes, pouch-of-Douglas fluid, corpus luteum, trilaminar→secretory shift). Two signs = probable; three or more with collapse or a typical corpus luteum = consistent with ovulation. Ultrasound cannot prove oocyte release.
- If serial data are weak, the report says so and recommends a repeat scan.

Teaching series are on the Folliculometry tab: **Load ovulatory example** and **Load irregular / inconclusive**.

## How to edit on GitHub

1. Open [index.html](./index.html).
2. Click the pencil.
3. Commit changes to `main`.
4. GitHub Pages rebuilds in about a minute. If you previously installed the PWA, do a hard refresh so `sw.js` can pick up cache `babsinogen-v6`.

Do **not** upload a `.zip` as a single file. GitHub Pages serves the unzipped files at the repository root.

## Disclaimer

Decision support only. Correlate every flag with clinical findings, departmental protocol, and serial trends. Not a substitute for clinical judgement.
