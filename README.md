# NeoEEG

Neonatal EEG and aEEG training app for clinicians. Installable on iPhone, iPad and Android as a Home Screen app and works offline after the first visit.

**Open:** https://anncheng1.github.io/NeoEEG/

## Install on iPhone
1. Open the link above in **Safari**.
2. Tap **Share** → **Add to Home Screen** → **Add**.

## Contents
Neonatal primer · electrode placement trainer · EEG→aEEG compression simulator · gestational-age library · five-category background classification · seizure recognition · artefact recognition game · HIE cooling timeline · case vignettes · pattern atlas.

## Adding real EEG images to the Pattern Atlas
The atlas shows synthetic teaching traces by default. To show a real recording image on a card:
1. Put the image file in `atlas/` (JPG/PNG/WebP).
2. Add an entry to `atlas/manifest.json`, keyed by the card id (lower-case name, words joined with hyphens; accents dropped, e.g. `delta-brush`, `trace-discontinu`, `burst-suppression`):

```json
{ "images": { "delta-brush": { "src": "atlas/delta-brush.jpg", "caption": "Delta brush, 34 wk PMA.", "credit": "Hospital Miri NICU, used with consent" } } }
```
Only add images you own or are licensed to publish — this repository is public. Individual users can also attach images privately on their own device with **＋ Add image** on each card.

## Releasing an update
Edit `index.html`, then bump `VERSION` in `sw.js` so installed copies refresh.

## Calibration
Traces are generated procedurally and checked numerically against the Hellström-Westas atlas (aEEG margins by age, five categories, interburst intervals). See the *Calibration check* section in the app's header, or `NeoEEG_calibration_check.md`.

## Disclaimer
Educational simulation. Not for clinical decision-making.
