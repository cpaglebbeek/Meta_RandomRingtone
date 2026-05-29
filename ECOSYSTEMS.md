# RandomRingtone Ecosysteem

## Platform-matrix

| Aspect | Android | iOS |
|---|---|---|
| **Repo** | `cpaglebbeek/RandomRingtone` | `cpaglebbeek/RandomRingtoneIOS` |
| **Stack** | Kotlin + Jetpack Compose | Swift + SwiftUI |
| **Min OS** | Android 11 (API 30) | TBD (vermoedelijk iOS 16+) |
| **Status** | LIVE — v1.11.0 (Build 134) DEBUG; STABLE v1.10.1 | SKELETON — v0.0.1 |
| **Distributie** | sideload via icthorse.nl/RandomRing/Apk/ | TBD (TestFlight? sideload via AltStore?) |
| **Package/Bundle** | `nl.icthorse.randomringtone` | `nl.icthorse.RandomRingtoneIOS` (voorlopig) |
| **License** | geen (TBD) | geen (TBD, volgt Android) |
| **DB** | Room v7 | TBD (Core Data of SwiftData) |

## Gedeelde concepten

- **Playlist-providers**: Spotify (WebView OAuth), Deezer (publieke API), YouTube (Y2Mate-proxy)
- **Track-model**: id (TrackId-consolidatie, v1.10.0) + titel + artiest + URL + lokale file
- **Ringtone-rotatie**: random / schema / per-contact (Android), TBD voor iOS
- **MP3 album-art embed**: ID3v2.3 APIC (Android v1.9.16 Billie_Jean)

## Asymmetrieën

- iOS heeft **geen public ringtone-API** — fundamentele beperking, route TBD (zie iOS `CONFLICTS.md` OPEN-1)
- Android heeft Storage Access Framework — iOS heeft Files-app, andere model
- YouTube-download op iOS waarschijnlijk via dezelfde Y2Mate-proxy, maar UIWebView i.p.v. Android WebView

## Verantwoordelijkheidsverdeling

| Onderwerp | Eigenaar |
|---|---|
| Android-bugs / releases | `RandomRingtone/BUGLIST.md` + `RELEASES.md` |
| iOS-bugs / releases | `RandomRingtoneIOS/BUGLIST.md` + `RELEASES.md` |
| Gedeelde feature-roadmap | `Meta_RandomRingtone/ROADMAP.md` |
| Documentatie-portal | iCt Horse D1 (icthorse.nl/D1/RandomRingtone/) — wordt later platform-tabs |
| Licentie-beslissing | `Meta_RandomRingtone/ROADMAP.md` OPEN-2 |
