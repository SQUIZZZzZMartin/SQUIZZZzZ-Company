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
| Journal21 ("Damals am …") | ungewöhnliche historische Ereignisse | 🟢 aktiv | 29.08.2026 | Für 04.09. per WebSearch geprüft (Direktabruf via web_fetch diesmal nicht möglich, siehe technischer Hinweis 29.08.); lieferte Hudson/Manhattan und Piuro-Bergsturz |
| Wikipedia ("On this day") | hohe Vollständigkeit | 🟢 aktiv | 29.08.2026 | Direktabruf von en.wikipedia.org diesmal durch Netzwerk-Allowlist blockiert (siehe technischer Hinweis 29.08.); Inhalte nur noch über WebSearch-Zusammenfassungen zugänglich, weiterhin stärkste Einzelquelle |
| Britannica | internationale Einordnung, Hintergrund | 🟢 aktiv | 29.08.2026 | Direktabruf von britannica.com diesmal durch Netzwerk-Allowlist blockiert (siehe technischer Hinweis 29.08.); nur über WebSearch nutzbar, lieferte u. a. Athelstan-Krönung und Mark-Spitz-Rekord |
| History.com | kulturgeschichtlich, amerikanisch | 🟢 aktiv | 29.08.2026 | Nur über WebSearch geprüft; lieferte u. a. Geronimo-Kapitulation und Truman-TV-Rede |
| National Geographic History | Archäologie, Wissenschaft, Expeditionen | 🟢 aktiv | 29.08.2026 | Weiterhin keine tagesgenaue "On this day"-Rubrik auffindbar; für 04.09. keine eigenen Treffer über die üblichen Kanäle hinaus |
| Smithsonian Magazine | Erfindungen, Kultur, Geschichte | 🟢 aktiv | 29.08.2026 | Keine tagesgenaue Rubrik; für 04.09. keine spezifischen Treffer |
| BBC History Magazine | Europa, Weltgeschichte | 🟢 aktiv | 16.08.2026 | Für 04.09. nicht erneut geprüft; weiterhin Vorsicht bei Drittseiten-Treffern (siehe Hinweis 21.08.) |
| Deutsche Welle Geschichte | deutsche Perspektive | 🟢 aktiv | 29.08.2026 | Keine tagesgenaue Rubrik auffindbar; für 04.09. keine eigenen Treffer |
| Bundeszentrale für politische Bildung | politische Ereignisse | 🟢 aktiv | 29.08.2026 | Für 04.09. drei Treffer (Deutschland-Chronik): SMAD-Justizreform 1945, USA-DDR-Beziehungen 1974, erste Leipziger Montagsdemo nach Sommerpause 1989 – Letztere in Auswahl übernommen |
| Guinness World Records | kuriose Rekorde | 🟢 aktiv | 29.08.2026 | Für 04.09. erneut kein tagesgenauer Rekordeintrag auffindbar |
| Aargauer Zeitung / NZZ (Swissair-Flug 306) | Schweizer Zeitgeschichte, Unglücksfälle | 🟢 aktiv (neu) | 29.08.2026 | Neu aufgenommen: lieferte detaillierte, gut verifizierte Berichterstattung zum Swissair-Absturz von Dürrenäsch (04.09.1963, 80 Tote); ergänzt Journal21 für Schweizer Themen |

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
| 29.08.2026 | Erneut geprüft (Recherche 04.09.): Problem hat sich verschärft. curl auf eine Wikimedia-Commons-Bild-URL liefert weiterhin HTTP 403 vom Proxy. Zusätzlich ist diesmal auch web_fetch für praktisch alle externen Domains (u. a. en.wikipedia.org, britannica.com) durch eine Netzwerk-Allowlist komplett blockiert – nicht nur für Bilder, sondern auch für Text/HTML-Direktabrufe. Recherche musste vollständig über WebSearch-Zusammenfassungen erfolgen, Primärquellen wurden nicht direkt eingesehen, sondern nur über die von WebSearch gelieferten Auszüge. Empfehlung bleibt: technische Lösung (z. B. Domain-Freigabe oder separater Bildabruf-Kanal) ausserhalb des Chronisten klären. |

## Verknüpfungen

- [[CH-006 Konstantin]]
- [[ADR-009]]
