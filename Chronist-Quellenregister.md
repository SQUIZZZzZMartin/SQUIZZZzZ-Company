---
typ: Konzept-Note
---

## Zweck

Diese Note führt die Rechercheliste von [[CH-006 Konstantin|Konstantin Krönikör]], dem Chronisten. Sie hält fest, welche Quellen er für die Recherche historischer Ereignisse aktiv nutzt und welche nicht mehr.

## Bedeutung

Konstantin erweitert sein Quellenspektrum laufend eigenständig. Diese Note ist sein Gedächtnis dafür: Neu gefundene, geeignete Quellen werden hier ergänzt, nicht mehr ergiebige Quellen werden als inaktiv markiert statt gelöscht.

## Quellen

| Quelle | Schwerpunkt | Status | Zuletzt genutzt/geprüft | Hinweis |
|---|---|:---:|---|---|
| Journal21 ("Damals am …") | ungewöhnliche historische Ereignisse | 🟢 aktiv | 22.08.2026 | Weiterhin sehr ergiebig (Recherche 28.08.: 11 der 25 gewählten Einträge stammen von hier), inkl. Bild-URLs im HTML |
| Wikipedia ("On this day") | hohe Vollständigkeit | 🟢 aktiv | 22.08.2026 | Direktabruf der Seite "August_28" funktionierte vollständig (Events/Births/Deaths); stärkste Einzelquelle für 28.08. (11 Einträge), auch mehrfach als Zweitquelle zur Verifikation genutzt |
| Britannica | internationale Einordnung, Hintergrund | 🟢 aktiv | 22.08.2026 | Direktabruf "on-this-day/August-28" funktionierte; lieferte u. a. Chadwick Boseman und "The Killers"-Premiere als Alleinstellungsmerkmale |
| History.com | kulturgeschichtlich, amerikanisch | 🟢 aktiv | 16.08.2026 | Für 28.08. nicht direkt abgerufen (Zeitbudget), Treffer via WebSearch deckten sich mit Wikipedia/Britannica (MLK, Emmett Till) |
| National Geographic History | Archäologie, Wissenschaft, Expeditionen | 🟢 aktiv | 22.08.2026 | Weiterhin keine tagesgenaue "On this day"-Rubrik auffindbar; für 28.08. keine eigenen Treffer |
| Smithsonian Magazine | Erfindungen, Kultur, Geschichte | 🟢 aktiv | 22.08.2026 | Keine tagesgenaue Rubrik; für 28.08. keine spezifischen Treffer |
| BBC History Magazine | Europa, Weltgeschichte | 🟢 aktiv | 16.08.2026 | Für 28.08. nicht erneut geprüft; weiterhin Vorsicht bei Drittseiten-Treffern (siehe Hinweis 21.08.) |
| Deutsche Welle Geschichte | deutsche Perspektive | 🟢 aktiv | 22.08.2026 | Keine tagesgenaue Rubrik auffindbar; für 28.08. keine eigenen Treffer |
| Bundeszentrale für politische Bildung | politische Ereignisse | 🟢 aktiv | 22.08.2026 | Für 28.08. erstmals wieder eigener Treffer: 28.08.1991, Wiederaufnahme diplomatischer Beziehungen Deutschlands zu den baltischen Staaten (nicht in Auswahl übernommen, da Platz für andere Kategorien priorisiert) |
| Guinness World Records | kuriose Rekorde | 🟢 aktiv | 22.08.2026 | Für 28.08. erneut kein tagesgenauer Rekordeintrag auffindbar |

## Status

| Status | Bedeutung |
|---|---|
| 🟢 aktiv | wird derzeit für die Recherche genutzt |
| ⚫ inaktiv | wird derzeit nicht genutzt (Grund siehe Hinweis) |

## Technische Hinweise

| Datum | Hinweis |
|---|---|
| 25.07.2026 | Fotodownload von Quellseiten (z. B. Britannica-CDN) in unbeaufsichtigten Läufen technisch nicht möglich: Shell-Sandbox blockiert externe Bild-Domains per Netzwerk-Allowlist, und das web_fetch-Werkzeug akzeptiert nur zuvor als Text/HTML gesehene URLs, keine Bild-Binärdaten. Recherche-Dokumente enthalten daher vorerst nur Quellenlinks statt eingebetteter Fotos, bis eine Lösung gefunden ist. |
| 08.08.2026 | Erneut geprüft (Recherche 14.08.): Bildabruf weiterhin blockiert – auch Bild-URLs, die zuvor auf einer per web_fetch geladenen Seite (z. B. Journal21) erschienen sind, werden vom Werkzeug als „nicht im Provenance-Set“ abgelehnt. Journal21 selbst liefert inzwischen aber wieder vollständigen Text- und Bildlink-Inhalt per Direktabruf (siehe Eintrag oben zu 18.07. – JS-Rendering-Problem scheint behoben). |
| 16.08.2026 | Erneut geprüft (Recherche 21.08.): Bildabruf weiterhin blockiert – sowohl direkter curl-Download (Netzwerk-Allowlist der Shell-Sandbox, HTTP 403 vom Proxy) als auch web_fetch auf Bild-URLs von Journal21 und Britannica-CDN (Ablehnung „nicht im Provenance-Set”, obwohl die URLs im selben Lauf per web_fetch/WebSearch sichtbar waren). Recherche-Dokument enthält daher weiterhin nur Quellenlinks statt eingebetteter Fotos. |
| 22.08.2026 | Erneut geprüft (Recherche 28.08.): identisches Bild – curl auf Journal21-Bild-URL liefert HTTP 403 vom Proxy, web_fetch derselben URL lehnt trotz vorherigem Seitenaufruf mit „nicht im Provenance-Set” ab. Problem seit mindestens 25.07.2026 unverändert, drei Recherche-Läufe in Folge betroffen. Empfehlung: technische Lösung ausserhalb des Chronisten prüfen (z. B. anderer Bildabruf-Kanal), da eigenständige Recherche-Workarounds bislang alle scheitern. |

## Verknüpfungen

- [[CH-006 Konstantin]]
- [[ADR-009]]
