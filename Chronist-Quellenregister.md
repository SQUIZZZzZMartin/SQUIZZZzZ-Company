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
| Journal21 ("Damals am …") | ungewöhnliche historische Ereignisse | 🟢 aktiv | 11.09.2026 | Für 11.09. Direktabruf via web_fetch wieder möglich (siehe technischer Hinweis 11.09.); sehr ergiebig, lieferte u. a. Elm-Bergsturz, Adorno-Geburt, WWF-Gründung |
| Wikipedia ("On this day") | hohe Vollständigkeit | 🟢 aktiv | 29.08.2026 | Für 11.09. nicht erneut direkt geprüft (Britannica/Journal21/bpb lieferten genug Substanz); weiterhin stärkste Einzelquelle bei Bedarf |
| Britannica | internationale Einordnung, Hintergrund | 🟢 aktiv | 11.09.2026 | Für 11.09. Direktabruf via web_fetch wieder möglich (siehe technischer Hinweis 11.09.); lieferte u. a. Pentagon-Grundsteinlegung, Pete-Rose-Rekord, Eurotunnel-Brand |
| History.com | kulturgeschichtlich, amerikanisch | 🟢 aktiv | 11.09.2026 | Nur über WebSearch geprüft; lieferte u. a. Fort Ross und Hoover-Dam-Fernstart |
| National Geographic History | Archäologie, Wissenschaft, Expeditionen | 🟢 aktiv | 11.09.2026 | Weiterhin keine tagesgenaue "On this day"-Rubrik auffindbar; für 11.09. keine eigenen Treffer über die üblichen Kanäle hinaus |
| Smithsonian Magazine | Erfindungen, Kultur, Geschichte | 🟢 aktiv | 11.09.2026 | Keine tagesgenaue Rubrik; für 11.09. nur 9/11-bezogene Treffer, keine für Auswahl geeigneten Funde |
| BBC History Magazine | Europa, Weltgeschichte | 🟢 aktiv | 16.08.2026 | Für 11.09. nicht erneut geprüft; weiterhin Vorsicht bei Drittseiten-Treffern (siehe Hinweis 21.08.) |
| Deutsche Welle Geschichte | deutsche Perspektive | 🟢 aktiv | 29.08.2026 | Keine tagesgenaue Rubrik auffindbar; für 11.09. nicht erneut geprüft |
| Bundeszentrale für politische Bildung | politische Ereignisse | 🟢 aktiv | 11.09.2026 | Direktabruf via web_fetch erfolgreich; lieferte detaillierten Eintrag zur Grenzöffnung Ungarns für DDR-Bürger (11.09.1989), in Auswahl übernommen |
| Guinness World Records | kuriose Rekorde | 🟢 aktiv | 11.09.2026 | Für 11.09. kein tagesgenauer, für die Sendung geeigneter Rekordeintrag auffindbar (einzige Treffer bezogen sich auf 9/11-Gedenkrekorde) |
| Aargauer Zeitung / NZZ (Swissair-Flug 306) | Schweizer Zeitgeschichte, Unglücksfälle | 🟢 aktiv | 29.08.2026 | Für 11.09. nicht benötigt |
| Computer History Museum | Technikgeschichte, IT-Pioniere | 🟢 aktiv (neu) | 11.09.2026 | Neu aufgenommen: lieferte gut verifizierten Geburtstags-Eintrag zu Charles Geschke (Adobe-Mitgründer, 11.09.1939); ergänzt bestehende Quellen um Technik-/IT-Schwerpunkt |
| WebSearch (allgemein, u. a. Britannica-, LOC-, Wikipedia-, tagesspiegel.de-Auszüge) | breite Ereignis- und Faktensuche über Suchmaschinen-Zusammenfassungen | 🟢 aktiv | 18.09.2026 | Für 18.09. einzige verfügbare Rechercheroute: direkter web_fetch auf journal21.ch, britannica.com etc. war diesmal durch eine Netzwerk-Allowlist vollständig blockiert (Fehler „not on the network allowlist"), auch für reinen Text/HTML-Abruf. Alle 17 Einträge stammen daher aus WebSearch-Zusammenfassungen, gezielt gegenrecherchiert; drei Kandidaten (vermeintliche Neptun-Entdeckung 18.09., Hollerith-Patent 18.09., Grundsteinlegung Deutsches Museum 18.09.) erwiesen sich bei Gegenprüfung als falsch datiert und wurden verworfen. |

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
| 11.09.2026 | Erneut geprüft (Recherche 11.09.): Text/HTML-Direktabruf via web_fetch ist diesmal wieder uneingeschränkt möglich – journal21.ch, britannica.com und bpb.de liessen sich vollständig direkt abrufen (nicht nur über WebSearch-Zusammenfassungen). Bildabruf bleibt jedoch weiterhin blockiert: curl auf Journal21-Bild-URLs liefert erneut HTTP 403 vom Proxy, und web_fetch auf dieselben Bild-URLs (die im selben Lauf auf einer per web_fetch geladenen Seite erschienen) wird mit „nicht im Provenance-Set" abgelehnt. Das Problem betrifft also weiterhin ausschliesslich Bilder, nicht mehr den Text-/HTML-Zugriff. Die Recherche 11.09. enthält daher wie in den Vorläufen nur Quellenlinks statt eingebetteter Fotos. |
| 18.09.2026 | Erneut geprüft (Recherche 18.09.): Rückschlag – web_fetch verweigerte diesmal jeden externen Host von Beginn an mit „not on the network allowlist" (nur noch npm-, PyPI-, GitHub- u. ä. Entwicklungs-Domains erlaubt), also strenger als am 29.08. Weder journal21.ch noch britannica.com noch andere Primärquellen liessen sich direkt abrufen. Recherche musste vollständig über WebSearch-Zusammenfassungen erfolgen. Bildabruf war dadurch erst recht nicht möglich – auch kein Testversuch, da schon der Text-/HTML-Zugriff verweigert wurde. Positiv: Gegenrecherche über WebSearch deckte drei falsch datierte Kandidaten auf (Neptun-Entdeckung, Hollerith-Patent, Grundsteinlegung Deutsches Museum – alle drei tatsächlich an anderen Tagen), die verworfen wurden. Empfehlung bleibt: technische Klärung des Allowlist-Zugriffs ausserhalb des Chronisten, da die Blockade zwischen Läufen offenbar schwankt (mal Volltext möglich, mal komplett gesperrt). |

## Verknüpfungen

- [[CH-006 Konstantin]]
- [[ADR-009]]
