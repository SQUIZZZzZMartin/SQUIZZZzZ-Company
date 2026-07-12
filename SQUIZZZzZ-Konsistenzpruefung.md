# SQUIZZZzZ Vault – Konsistenzprüfung

Stand: 12.07.2026 · Geprüft: 46 Notes (davon 8 "000-Move"-Dokumente), Grafiken-Ordner, .obsidian-Konfiguration

## Zusammenfassung

Der Vault ist inhaltlich reichhaltig und die Grundarchitektur (Orange Codex / SOS / SQUIZZZzZ Knowledge / Academy, ADR-Prozess, Notentypen-Modell) ist klar durchdacht. In der praktischen Umsetzung weicht der Großteil der Notes jedoch von den selbst aufgestellten Standards ab. Die auffälligsten Probleme betreffen den Design-Bereich (drei parallele, sich überschneidende Hierarchien), fehlende Typ-Felder bei den meisten Notes, kaputte bzw. nicht existierende Verlinkungen sowie eine komplett unverknüpfte Altdokumentation (die acht "000-Move"-Dateien).

## 1. Kritische Befunde

**Orange Codex.md ist leer (0 Byte).** Die Note wird von SQUIZZZzZ.md, SOS.md, CD-000 und Matildes Character Book als zentrales Grundlagendokument verlinkt ("orientiert sich am Orange Codex"), enthält selbst aber keinen Inhalt.

**Drei konkurrierende Design-Hierarchien.** DES-000-Design System.md definiert ein 3-Säulen-Modell (Foundations / Corporate Design / Brand Design). CD-000-Corporate Design.md und BD-000-Brand Design.md führen jedoch jeweils eigene, sich überschneidende Verzeichnisse:
- DES-001-Farbwelt und DES-002-Typografie sind gleichzeitig im Verzeichnis von CD-000 UND von BD-000 gelistet. Nach ADR-003 darf eine Note aber nur eine strukturelle Einordnung (einen Verzeichnis-Elternteil) besitzen.
- CD-000 verweist auf [[CD-006-Grafische Standards]], [[CD-007-Icons]], [[CD-008-Diagrammstil]], [[CD-009-Bildsprache]] – keine dieser vier Dateien existiert. Die tatsächlich existierende Datei heißt "Grafische Standards.md", also ohne CD-Präfix und ohne Nummer – Namensabweichung zur Verlinkung.
- BD-000 verweist auf [[BD-005-Event Design]] und [[BD-006-Event Design]] – gleicher Titel, zwei Nummern, beide Dateien existieren nicht. BD-004 fehlt komplett (Nummerierungslücke).
- Grafische Standards.md listet selbst neun Unter-Notes (SVG-Standard, Raster, Typografie in Grafiken, Farbverwendung, Kasten und Formen, Linien und Pfeile, Icons, Legenden, Exportformate) – keine davon existiert.

**"BD-003-Lore" wird viermal falsch verlinkt.** CH-001-misterQ.md, CH-002-Lissi.md, CH-003-Jovis Kyckling.md und CH-004-Friedrich.md verlinken alle auf [[BD-003-Lore]]. Die tatsächliche Datei heißt aber "BD-003-Lore (SQUIZZZzZ-Akten).md". In Obsidian würde jeder dieser Links eine neue, leere Note "BD-003-Lore" anlegen, statt die bestehende zu öffnen.

**Acht "000-Move"-Dokumente sind komplett isoliert.** Die Dateien "000-Move-SQUIZZZzZ Dokumentation-01" bis "-08" (zusammen ca. 20 Seiten Gesamtdokumentation zu Philosophie, Corporate Design, Figuren, Bühnenwelten, Filmwelt, Spielmechanik, Produktion und Stilregeln) enthalten keinen einzigen Wikilink – weder rein noch raus. Keine andere Note verweist auf sie. Der Name "Move" deutet darauf hin, dass ihr Inhalt eigentlich in die reguläre Notenstruktur überführt werden sollte; das ist bisher nicht passiert. Teile überschneiden sich bereits mit sauber strukturierten Notes (z. B. sind die Farbwerte aus Teil 2 identisch mit DES-001-Farbwelt.md), andere Teile (Spielmechanik, Produktion, Stilregeln/Weltgesetze) existieren nirgendwo sonst im Vault.

## 2. Fehlendes Typ-Feld (ADR-002 / Notentypen-Modell)

ADR-002 legt fest, dass jede Note einem der fünf Notentypen zugeordnet wird. Von 36 regulären Notes (ohne die 000-Move-Dateien) tragen nur 6 tatsächlich ein "Typ"-Feld: CD-000, CD-001, DES-001, Grafische Standards, Notentypen, SOS. Kern-Notes wie SQUIZZZzZ.md, Unternehmensarchitektur.md, Wissensmanagement.md, Obsidian.md, Academy.md sowie sämtliche ADRs und Character Books (CH-001 bis CH-005) haben kein Typ-Feld.

## 3. Verzeichnis vs. Verknüpfungen (ADR-003)

Die in ADR-003 festgelegte Trennung wird nur teilweise gelebt:
- SQUIZZZzZ.md, die oberste Note der Hierarchie, hat kein Verzeichnis – Orange Codex und SOS stehen dort unter "Verknüpfungen", obwohl sie strukturell eigentlich direkte Kinder sein müssten.
- SOS.md listet unter "Verzeichnis" acht Bereiche (Notentypen, CD-000, Vorlagen, Rollen, KI-Mitarbeiter, Workflows, Qualitätsmanagement, Tools, Schnittstellen), von denen nur zwei tatsächlich als Notes existieren. Der organisatorische Teil des SOS ist also zu großen Teilen nur als Absicht dokumentiert.
- "SQUIZZZzZ Knowledge" – laut Unternehmensarchitektur.md eine der vier tragenden Säulen neben Orange Codex, SOS und Academy – hat selbst keine eigene Note. Nur SOS.md und Wissensmanagement.md erwähnen den Begriff.
- CH-005 Matilde.md hat weder Verzeichnis noch Verknüpfungen, obwohl vier (praktisch identische) Unter-Notes zu ihr existieren (CH-005-001 bis CH-005-004) – dazu gleich mehr.

## 4. Character Books (CH-001 bis CH-005): fünf verschiedene Schemata

Alle fünf sollten laut CH-000-Verzeichnis vom gleichen Typ ("Darsteller" bzw. "Company-KI") sein, folgen aber jeweils einer eigenen Gliederung: CH-001 nutzt unformatierte Überschriften mit Unterebene "Teil 2: Characterprofil > ### Charakter/Persönlichkeit/...", CH-002 bis CH-004 nutzen die gleichen Abschnittsnamen, aber fett formatierte Überschriften ohne CH-001s Unterebenen-Struktur, und CH-005 (Matilde) hat ein komplett anderes 6-Teile-Schema ohne jede Übereinstimmung mit den anderen vier. Keines der fünf enthält Zweck/Bedeutung/Verzeichnis/Verknüpfungen im Sinne des Notentypen-Modells.

## 5. Doppelte / verwaiste Dateien

- **CH-005-004-SQUIZZZzZ-Standards.md** und **CH-005-004-SQUIZZZzZ-Standards-v1.0.md** sind byte-identisch (Diff liefert keine Unterschiede) – ein Duplikat, vermutlich ein liegen gebliebener Versionierungsstand.
- Matildes vier Unter-Notes (CH-005-001 Onboarding-Prozess, -002 Persönlichkeit und Kommunikation, -003 Ausgabe und Einrichtung, -004 Standards) liegen im Grafiken-Ordner statt neben den anderen Notes, und werden von CH-005 Matilde.md nirgends verlinkt – sie sind im Wissensnetz nicht erreichbar. Das widerspricht zusätzlich dem eigenen Grundsatz aus Obsidian.md, dass Ordner nur der Dateiablage dienen und die Wissensstruktur über Verknüpfungen entsteht.
- **Google Drive Test.md** (33 Byte, Inhalt: "Ich habe bisher 25 KI-Assitenten") wirkt wie eine Test-/Wegwerfnotiz ohne redaktionellen Zweck.
- **Martin.md** enthält nur ein fehlerhaftes Markdown-Fragment: "**Verknüpfungen" (offener Fettdruck, keine Überschriften-Raute, kein schließendes **).

## 6. Kleinere Formatierungsinkonsistenzen

- Überschriften-Stil uneinheitlich: manche Notes nutzen "## Zweck", andere "## **Zweck**" (fett) – teils sogar innerhalb verwandter Notes (z. B. SQUIZZZzZ.md ohne Fettdruck vs. Wissensmanagement.md/Obsidian.md mit Fettdruck).
- **Notentypen.md** – ausgerechnet die Note, die den Standard definiert – hat zwei "Verknüpfungen"-Überschriften hintereinander (eine leere fettgedruckte, direkt gefolgt von einer zweiten mit dem eigentlichen Inhalt).
- CH-005 Matilde.md: Bildeinbindung mit Tippfehler – `![[CH-005-Matilde.png]]]` hat eine überzählige schließende Klammer.
- Namenskonvention uneinheitlich: CH-001-misterQ, CH-002-Lissi, CH-003-Jovis Kyckling, CH-004-Friedrich nutzen Bindestrich vor dem Namen, "CH-005 Matilde.md" nutzt ein Leerzeichen. Der eingebettete Bildname dort heißt wiederum "CH-005-Matilde.png" (mit Bindestrich) – selbst innerhalb einer Note uneinheitlich.
- Mehrere Notes verlinken auf noch nicht existierende, aber plausibel geplante Notes (z. B. Rollen, Tools, Workflows, Vorlagen, Qualitätsmanagement, Schnittstellen aus SOS.md; Markdown, Prompt Engineering, KI-Agenten, APIs, Automatisierung aus Academy.md). Das ist im Obsidian-Modell zulässig (Notentypen.md beschreibt automatisches Anlegen), sollte aber bewusst als offene To-dos geführt werden, nicht als stiller Bestand.

## 7. Was gut funktioniert

- ADR-Nummerierung ist lückenlos und konsistent (ADR-000 bis ADR-005, alle im Verzeichnis von ADR-000 korrekt gelistet, Status überall "Akzeptiert").
- Die Farbwerte sind über alle Fundstellen hinweg identisch (#FF8E00, #0B106C, #1921B1, #121889, #00B25C, #008A47, #006C38) – keine Widersprüche in den Markenfarben.
- Die vier Grund-Notes (SQUIZZZzZ, Unternehmensarchitektur, Wissensmanagement, Obsidian) sind inhaltlich stringent und untereinander sauber verknüpft.

## 8. Empfohlene nächste Schritte

1. Orange Codex.md befüllen – zentrale Lücke, da mehrfach als Grundlage referenziert.
2. Design-Bereich entwirren: eine Hierarchie festlegen (vermutlich DES-000 als Dach), doppelte Kindschaften von DES-001/DES-002 auflösen, CD-000/BD-000/Grafische Standards.md an die tatsächlich existierenden Dateien anpassen oder fehlende Unter-Notes anlegen.
3. Die vier "[[BD-003-Lore]]"-Links korrigieren auf "[[BD-003-Lore (SQUIZZZzZ-Akten)]]".
4. Entscheiden, was mit den acht "000-Move"-Dateien geschieht: entweder in die reguläre Notenstruktur überführen (Titel legt das nahe) oder archivieren.
5. Duplikat CH-005-004-SQUIZZZzZ-Standards-v1.0.md löschen bzw. mit der Hauptdatei zusammenführen, Matildes Unter-Notes aus dem Grafiken-Ordner verlinken oder umziehen.
6. Einheitliches Character-Book-Template für CH-001 bis CH-005 festlegen (oder bewusst dokumentieren, warum Company-KIs wie Matilde ein anderes Schema als Darsteller haben).
7. Typ-Feld nachtragen, wo es laut Notentypen-Modell verpflichtend ist.
