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
| Journal21 ("Damals am …") | ungewöhnliche historische Ereignisse | 🟢 aktiv | 16.08.2026 | Weiterhin sehr ergiebig (Recherche 21.08.: 13 der 25 gewählten Einträge stammen von hier), inkl. Bild-URLs im HTML |
| Wikipedia ("On this day") | hohe Vollständigkeit | 🟢 aktiv | 16.08.2026 | Direktzugriff auf en.wikipedia.org funktionierte am 16.08. über WebSearch-Zusammenfassung und diente mehrfach als Zweitquelle zur Verifikation (u. a. Lettland-Unabhängigkeit, Burroughs-Patent) |
| Britannica | internationale Einordnung, Hintergrund | 🟢 aktiv | 16.08.2026 | Zuverlässigster Direktzugriff, inkl. Bild-URLs; deckte 21.08. besonders gut mit Filmpremieren (Bambi, Dirty Dancing) und Naturereignissen ab |
| History.com | kulturgeschichtlich, amerikanisch | 🟢 aktiv | 16.08.2026 | Direktzugriff funktioniert, lieferte für 21.08. primär Dubletten zu Britannica (Hawaii, Mona Lisa) |
| National Geographic History | Archäologie, Wissenschaft, Expeditionen | 🟢 aktiv | 16.08.2026 | Weiterhin keine tagesgenaue "On this day"-Rubrik auffindbar; für 21.08. keine eigenen Treffer |
| Smithsonian Magazine | Erfindungen, Kultur, Geschichte | 🟢 aktiv | 16.08.2026 | Keine tagesgenaue Rubrik; für 21.08. nur allgemeiner Artikel mit Hawaii/Tornado-Erwähnung, keine neuen Ereignisse |
| BBC History Magazine | Europa, Weltgeschichte | 🟢 aktiv | 16.08.2026 | Suchergebnisse für "BBC History August 21" stammten grösstenteils von Drittseiten (z. B. beautifulbritain.co.uk) statt bbc.co.uk selbst; eine daraus stammende Angabe (BBC-Fernsehstart 21.08.1936) liess sich nicht verifizieren und wurde verworfen (siehe Bericht Recherche 21.08.) |
| Deutsche Welle Geschichte | deutsche Perspektive | 🟢 aktiv | 16.08.2026 | Keine tagesgenaue Rubrik auffindbar; für 21.08. keine eigenen Treffer, lieferte aber Hinweis auf Prager Frühling als Randtreffer |
| Bundeszentrale für politische Bildung | politische Ereignisse | 🟢 aktiv | 08.08.2026 | Für 21.08. keine spezifische Chronik-Seite gefunden; letzter erfolgreicher Direktabruf weiterhin 08.08. (Deutschland-Chronik) |
| Guinness World Records | kuriose Rekorde | 🟢 aktiv | 16.08.2026 | Für 21.08. erneut kein tagesgenauer Rekordeintrag auffindbar |

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
| 16.08.2026 | Erneut geprüft (Recherche 21.08.): Bildabruf weiterhin blockiert – sowohl direkter curl-Download (Netzwerk-Allowlist der Shell-Sandbox, HTTP 403 vom Proxy) als auch web_fetch auf Bild-URLs von Journal21 und Britannica-CDN (Ablehnung „nicht im Provenance-Set“, obwohl die URLs im selben Lauf per web_fetch/WebSearch sichtbar waren). Recherche-Dokument enthält daher weiterhin nur Quellenlinks statt eingebetteter Fotos. |

## Verknüpfungen

- [[CH-006 Konstantin]]
- [[ADR-009]]
