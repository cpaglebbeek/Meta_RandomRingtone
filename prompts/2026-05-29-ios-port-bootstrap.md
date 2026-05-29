---
date: 2026-05-29
slug: ios-port-bootstrap
ecosystem: RandomRingtone
platforms: [iOS, Android, Meta]
type: newp
status: done
resume: ""
---

# Sessie 2026-05-29 — iOS-port bootstrap

## Context
Gebruiker wil een iOS-versie van RandomRingtone. Bestaande Android-app (Kotlin/Compose, v1.11.0 DEBUG / STABLE v1.10.1) blijft de hoofd-distributie.

## Beslissingsboom in deze sessie

1. **Branch vs los repo** → "maak een nieuwe branch voor een iOS port" (oorspronkelijke prompt)
2. **WhatIf gegeven:** opties A (monorepo), B (branch-only), C (los repo). Gebruiker koos **C**.
3. **Sub-vraag C1 vs C2** (los repo zonder Meta-master vs los repo onder nieuw Meta-master): voorgesteld C2 (PhotoVerify-pattern, future-proof). Gebruiker stemde in met defaults.
4. **Naam-keuze:** `RandomRingtoneIOS` (CamelCase, consistent met `RandomRingtoneLogger`)
5. **Public:** ja, consistent met Android-repo
6. **Stack:** Native Swift/SwiftUI
7. **License:** match Android — Android heeft géén LICENSE (gecheckt via GitHub API), dus iOS ook geen. OPEN-2 voor latere beslissing.
8. **Scope-pivot iOS ringtone-API:**
   - iOS heeft geen public ringtone-API
   - Gebruiker: "ga uit van een manier dat het wel kan. al weet ik nog niet hoe"
   - Vastgelegd als **OPEN-1** in `RandomRingtoneIOS/CONFLICTS.md`

## Acties in deze sessie

- ✅ `/verifyrules` fase 0 — 9/12 volledig, 3 gedeeltelijk (zelf-gecorrigeerd)
- ✅ License check Android repo — geen LICENSE aanwezig
- ✅ Meta_RandomRingtone lokaal aangemaakt + initial docs (README, CLAUDE.md, ECOSYSTEMS.md, STATUS.md, ROADMAP.md)
- ⏳ Meta_RandomRingtone GitHub remote + push
- ⏳ RandomRingtoneIOS lokaal aanmaken + Xcode-skeleton + GitHub
- ⏳ Initial docs in iOS-repo (ARCHITECTURE met target-mapping, BUGLIST/RELEASES/CONFLICTS/ACTIONS skelet)
- ⏳ Memory entries: `project_meta_randomringtone.md` + `project_randomringtone_ios.md` + update `project_randomringtone.md`
- ⏳ Meta_Master sync: PROJECTS.json + ECOSYSTEMS.md + STATUS.md
- ⏳ `/sanitycheck` fase N+1

## Open items voor vervolg-sessie

- OPEN-1: iOS ringtone-set methode (onderzoek na skeleton)
- OPEN-2: ecosysteem-licentiekeuze
- OPEN-3: codenaam-pool iOS
- OPEN-4: iOS distributie-kanaal (TestFlight vs AltStore)
- Geen Mac aanwezig voor Xcode-build? Verifiëren bij eerste code-fase
