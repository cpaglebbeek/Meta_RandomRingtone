# CLAUDE.md — Meta_RandomRingtone

Sub-master voor het RandomRingtone-ecosysteem.

## Verhouding tot Meta_Master

- **Meta_Master** = top-level source of truth (`/Users/christian/Documents/Gemini_Projects/Meta_Master`)
- **Meta_RandomRingtone** = ecosysteem-laag voor RandomRingtone-platforms (Android + iOS)
- Bij sessiestart **eerst** Meta_Master pullen (globale CLAUDE.md regel), **dan** Meta_RandomRingtone pullen indien sessie ecosysteem-breed werk raakt.

## Platform-repos

| Repo | Pad | Doel |
|---|---|---|
| `RandomRingtone` | `Gemini_Projects/RandomRingtone` | Android (Kotlin/Compose), live productieapp |
| `RandomRingtoneIOS` | `Gemini_Projects/RandomRingtoneIOS` | iOS (Swift/SwiftUI), in opbouw |

## Werkverdeling

- **Per-platform code, bugs, releases** → in de platform-repo zelf (`BUGLIST.md`, `RELEASES.md`, `CONFLICTS.md`)
- **Ecosysteem-brede beslissingen** (gedeelde features, naam-/branding-keuzes, licentie, shared back-end services) → in dit Meta-repo (`ROADMAP.md`, `prompts/`)
- **Documentatie-portal** (iCt Horse D1) → wordt later samengevoegd in `icthorse.nl/D1/RandomRingtone/` met platform-tabbladen

## Versie-strategie

- Android en iOS kunnen **onafhankelijk versioneren** (verschillende app-stores, verschillende store-cadences)
- **Codenaam-pool gedeeld** (Famous Singers): Android gebruikt Whitney Houston-track-namen, iOS kiest later eigen pool of deelt dezelfde
- Beide volgen **semver-met-bump-per-bugfix** (universele regel, zie globaal CLAUDE.md)

## Sessie-MD plek

Sessies die het hele ecosysteem raken (architectuur, naamgeving, licentie, gedeelde back-end) → `prompts/YYYY-MM-DD-<slug>.md` in dít repo.
Sessies die alleen één platform raken → `prompts/` in die platform-repo.

## Regels

1. Bij wijzigingen in dit repo: commit + push naar `cpaglebbeek/Meta_RandomRingtone` (public)
2. Bij wijzigingen in een platform-repo die ecosysteem-impact hebben: `STATUS.md` hier bijwerken
3. WhatIf-protocol geldt onverkort
4. Alle architecturele beslissingen expliciet vastleggen (`ARCHITECTURE.md` per platform + `ROADMAP.md` hier)
