cstroie.github.io
=================

Source of https://cstroie.github.io/, a landing page for these browser-based projects. Each one is an installable PWA that works offline.

Retro computing:

- [BASIC-40](https://github.com/cstroie/BASIC-40): an 8-bit style BASIC interpreter
- [RPN-4](https://github.com/cstroie/RPN-4): an HP-style RPN scientific calculator, with an HP-12C style landscape layout on phones
- [FORTH-79](https://github.com/cstroie/FORTH-79): a small, mostly standard Forth
- [DigitalRerun](https://github.com/cstroie/DigitalRerun): a CP/M 2.2 computer with a Z80 and a VT100 or ADM-3A screen

Medical imaging:

- [IRIS](https://github.com/cstroie/GIRI): a searchable guide to radiology imaging indications, in Romanian (hosted in this repo under `/iris/`)

The other projects publish their own GitHub Pages sites under `/BASIC-40/`, `/RPN-4/`, `/FORTH-79/` and `/DigitalRerun/`.

## Notes

- `.well-known/assetlinks.json` holds the Digital Asset Links that let Android apps (Trusted Web Activities) built from these PWAs open full screen. Add one entry per app, with its package name and signing-key SHA-256 fingerprint.
- `.nojekyll` makes GitHub Pages serve the `.well-known` folder.
- All the apps share the `cstroie.github.io` origin, so each one must use its own prefix for service-worker caches and `localStorage` keys, and only delete caches with its own prefix.
