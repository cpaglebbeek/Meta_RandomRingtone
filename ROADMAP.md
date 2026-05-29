# ROADMAP — RandomRingtone Ecosysteem

## Korte termijn (Q2-Q3 2026)

### Android
- Toestel-validatie v1.10.1 STABLE (Bundel 1 in `RandomRingtone/ACTIONS.md`)
- v1.11.0 selectieve backup/restore feature-test → mark stable
- Bundel 3 P0 SECURITY: signing key roteren, `.jks.backup` uit history

### iOS
- **Fase 0 — Skeleton (klaar 2026-05-29):** repo + docs + SwiftPM-skeleton zonder code
- **Fase 1 — Architectuur-onderzoek + vastlegging-gates:** OPEN-1/5/6 onderzoeks-docs (`docs/ringtone-set-research.md`, `persistence-choice.md`, `background-rotation.md`) + verplichte vastleggings-docs (`docs/PRINCIPLES.md`, `docs/DEPENDENCIES.md`, `docs/USER_JOURNEYS.md`). `ARCHITECTURE.md` verfijnen, sanitycheck herhalen (doel 90%+).
- **Fase 2 — Minimum viable downloader:** Spotify-playlist lezen + tracks downloaden + lokale lijst. Eerst Mac met Xcode regelen. Bij eerste view ook `DESIGN_TOKENS.md` + `docs/screens/` aanmaken.
- **Fase 3 — Ringtone-set integratie:** afhankelijk van OPEN-1 uitkomst (eigen tones-app, GarageBand-export, Shortcuts, alarm-pivot)
- **Fase 4 — Polish + distributie:** TestFlight of AltStore-route; CHANGELOG.md losweken van RELEASES.md

### Ecosysteem (Meta_RandomRingtone) — vastlegging-gates fase 1
Uit sanitycheck 29-5 — gaten op conceptueel-technisch en logisch-technisch niveau:
- [ ] **`docs/PRINCIPLES.md`** aanmaken — waarom dit ecosysteem-pattern (sub-master + platform-repos), waarom geen monorepo, waarom PhotoVerify-precedent
- [ ] **`docs/DEPENDENCIES.md`** aanmaken — cross-repo dependencies (Logger-backend ↔ Android, gedeelde Y2Mate-proxy ↔ Android+iOS), oorzaak-gevolg matrix
- [ ] OPEN-2 licentiekeuze (AGPL-3.0 lijkt logisch, consistent met andere iCt Horse repos)
- [ ] OPEN-3 codenaam-pool iOS
- [ ] D1 documentatie-portal uitbreiden met iOS-tabblad zodra code-base substantieel is

## Middellange termijn (Q4 2026)

- Web-versie? (alleen download + library, geen ringtone-set in browser)
- Gedeelde backend voor playlist-sync tussen devices?
- Mac-versie via SwiftUI-Catalyst (gratis bij Swift-codebase)?

## Lange termijn

- App-store-publicatie? (review-risico's: download van YouTube, kopie-bescherming, etc.)
- Multi-account / multi-device sync

## Beslissingen-log

- **2026-05-29:** ecosysteem opgesplitst in Meta-master + platform-repos (PhotoVerify-pattern), keuze C2 uit WhatIf-sessie. iOS port gestart als parallel platform-repo, geen branch in Android-repo.
- **2026-05-29:** scope-pivot iOS-ringtone-set uitgesteld — aanname dat er een werkbare weg is, methode TBD (OPEN-1).
