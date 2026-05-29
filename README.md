# Meta_RandomRingtone

Sub-master repo voor het **RandomRingtone-ecosysteem**: een platform-onafhankelijke beltoon-rotatie-app op basis van streaming-playlists (Spotify, Deezer, YouTube).

## Platform-repos

| Platform | Repo | Status | Versie | Stack |
|---|---|---|---|---|
| Android | [`RandomRingtone`](https://github.com/cpaglebbeek/RandomRingtone) | LIVE | v1.11.0 (Build 134) DEBUG — STABLE v1.10.1 | Kotlin + Jetpack Compose |
| iOS | [`RandomRingtoneIOS`](https://github.com/cpaglebbeek/RandomRingtoneIOS) | SKELETON | v0.0.1 | Swift + SwiftUI |

## Ecosysteem-doel

Beide platforms delen een **logisch gegevensmodel** (Playlist → Tracks → ringtone-mapping) en een **vergelijkbare UX**, maar elk gebruikt de native API's van het OS. De iOS-app is **geen 1-op-1 port** — zie `RandomRingtoneIOS/ARCHITECTURE.md` voor de target-mapping.

## Open ecosysteem-vragen

- **OPEN-1 (iOS):** methode voor ringtone-set op iOS — nog onbekend. Aangenomen: er is een werkbare weg (zie iOS-repo `CONFLICTS.md` / `ACTIONS.md`).
- **OPEN-2 (gedeeld):** licentie-beslissing voor het hele ecosysteem (Android heeft nu geen LICENSE; iOS volgt).

## Documentatie

- `CLAUDE.md` — sub-master regels + verwijzing Meta_Master
- `ECOSYSTEMS.md` — platform-repos + verantwoordelijkheidsverdeling
- `STATUS.md` — actuele versies per platform
- `ROADMAP.md` — gedeelde toekomstplannen
- `prompts/` — sessie-MD's voor ecosysteem-brede beslissingen

## Master

Bovenliggend: [`Meta_Master`](https://github.com/cpaglebbeek/Meta_Master) — single source of truth voor alle projecten.
