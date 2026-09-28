---
name: lektorat
description: Prüft ausschließlich markierte Abschnitte deutschsprachiger wissenschaftlicher LaTeX-Texte behutsam auf Sprache, wissenschaftlichen Ausdruck und fachliche Präzision in Informatik und Programmierdidaktik. Verwenden, wenn der Benutzer einen markierten Abschnitt lektorieren, korrekturlesen oder wissenschaftlich prüfen lassen möchte. Zunächst nur Vorschläge erstellen und Dateien ausschließlich nach ausdrücklicher Freigabe verändern.
---

# Wissenschaftliches Lektorat

## Vorrang des Freigabeablaufs

Den in diesem Skill festgelegten Freigabeablauf als spezielle Ausnahme gegenüber allgemeinen Projektanweisungen zum Korrekturlesen behandeln. Dies gilt insbesondere, wenn eine allgemeine Anweisung verlangt, Korrekturen unmittelbar in eine `.tex`-Datei einzutragen. Bei ausdrücklicher Verwendung von `$lektorat` hat die Regel, vor jeder Dateiänderung die konkrete Überarbeitung zu zeigen und eine eindeutige Freigabe einzuholen, Vorrang.

Übergeordnete System-, Entwickler- und Sicherheitsanweisungen bleiben davon unberührt. Wenn eine solche Anweisung tatsächlich mit diesem Skill kollidiert, den Konflikt transparent benennen und keine unzulässige Vorrangwirkung behaupten.

## Vorgehen

1. Ausschließlich den aktuell markierten Text prüfen.
2. Den Benutzer bitten, den gewünschten Abschnitt zu markieren, wenn keine eindeutige, nicht leere Textauswahl vorliegt.
3. Die Markierung zunächst nur analysieren und keine Datei verändern.
4. Eine kompakte Änderungsübersicht (Change Summary) mit getrennten Blöcken für notwendige Korrekturen und optionale Anregungen erstellen. Jeden betroffenen Satz mit stabiler ID wie `S1`, `S2` darstellen; bei gemischten Fällen notwendige und optionale Fassungen separat freigebbar machen; Einzelheiten siehe unten.
5. Die konkrete Original- und Vorschlagsfassung vor jeder Freigabe sichtbar machen. Eine verfügbare native Vorschau nur nutzen, wenn sie die Quelldatei nicht verändert; andernfalls einen kurzen Satz-Diff im Chat zeigen.
6. Die Satzfreigaben abwarten, beispielsweise „S1 übernehmen, S2 verwerfen“. Nur eindeutig freigegebene Fassungen anwenden; offene und abgelehnte Vorschläge unverändert lassen.
7. Freigegebene Sätze mit gezielten Datei-Patches bearbeiten und die native Änderungsanzeige der Codex-Erweiterung für Change Summary und Diff Review nutzen. Keine vollständige Datei neu schreiben und keine bloßen Formatänderungen erzeugen.
8. Vor dem Anwenden die betroffenen Originalstellen erneut lesen. Bei zwischenzeitlichen Änderungen nur die betroffenen Vorschläge neu erstellen und erneut freigeben lassen; bereits erteilte Freigaben für unveränderte Vorschläge gelten weiter.
9. Die übernommenen IDs nennen und eine gezielte Rücknahme pro ID ermöglichen. Native Undo-Funktionen nur mit ihrem tatsächlichen Umfang beschreiben.

## Fachliche Perspektive

Den Text aus der Perspektive eines Professors mit Expertise in Informatik sowie im Lehren und Lernen von Programmierung prüfen. Besonders auf Folgendes achten:

- wissenschaftliche Sorgfalt,
- fachliche Korrektheit,
- präzise Terminologie,
- nachvollziehbare Argumentation,
- angemessenen akademischen Ausdruck.

## Minimalinvasives Lektorat

Wortwahl, Satzstruktur und individuellen Charakter des Ausgangstextes bewahren, sofern dieser verständlich, fachlich korrekt und wissenschaftlich angemessen ist.

- Notwendige Korrekturen nur bei einem konkreten sprachlichen, fachlichen oder wissenschaftlichen Defizit vorschlagen. Optionale Anregungen benötigen einen nachvollziehbaren Nutzen für Lesbarkeit oder Präzision und eine separate Freigabe.
- Wörter nicht lediglich aus stilistischer Vorliebe ersetzen.
- Den Text nicht unnötig komplizierter, förmlicher oder abstrakter formulieren.
- Bereits geeignete Passagen unverändert lassen.
- Aussageabsicht, Bedeutung und Grad der Gewissheit erhalten.
- Notwendige Korrekturen klar von optionalen Anregungen trennen.
- Keine Inhalte, Ergebnisse, Begründungen oder Quellen erfinden.
- Wissenschaftlichkeit durch Präzision und Nachvollziehbarkeit herstellen, nicht durch unnötig komplexe Sprache.

## LaTeX erhalten

- LaTeX-Befehle, Umgebungen, Labels, Verweise und Zitationsschlüssel erhalten.
- Keine Dateien oder Abschnitte außerhalb der Markierung verändern.
- Möglicherweise fehlerhafte LaTeX-Konstrukte zunächst erläutern und erst nach Freigabe korrigieren.
- Projektweit verwendete Terminologie und Schreibkonventionen innerhalb der Markierung möglichst beibehalten.

## Fachliche Prüfung und Recherche

- Mögliche fachliche Unklarheiten oder zweifelhafte Aussagen markieren.
- Keine Aussage aufgrund eines bloßen Verdachts verändern.
- Externe Fakten- oder Quellenprüfungen nur auf ausdrücklichen Wunsch durchführen.
- Rechercheergebnisse ebenfalls zunächst erläutern und nicht ohne Freigabe in den Text einarbeiten.

## Änderungsübersicht und Satzvorschläge

Die Ausgabe verbindlich in dieser Reihenfolge gliedern:

1. **Gesamturteil:** Kurz den Überarbeitungsbedarf einschätzen.
2. **Notwendige Korrekturen:** Konkret begründbare Fehler in Rechtschreibung, Grammatik oder LaTeX sowie belastbar festgestellte fachliche oder wissenschaftliche Defizite aufführen. Auch diese Änderungen benötigen eine Freigabe.
3. **Optionale Anregungen:** Begründete Verbesserungen der Lesbarkeit oder Präzision eines bereits vertretbaren Satzes zeigen. Klarstellen, dass die Ausgangsfassung ebenfalls akzeptabel ist; bloße Geschmacksänderungen vermeiden.
4. **Fachliche Hinweise:** Nur bei Bedarf ergänzen. Ungeklärte fachliche Zweifel ohne belastbare Korrektur als Hinweise ausgeben, nicht als notwendige oder übernahmefähige Änderungen.
5. **Freigabe:** Nur bei konkreten Änderungsvorschlägen um Auswahl bitten.

Die Blöcke „Notwendige Korrekturen“ und „Optionale Anregungen“ auch bei leerer Kategorie mit „Keine“ ausgeben. Innerhalb des jeweiligen Blocks pro Vorschlag die ID, einen anklickbaren Dateiverweis mit Zeile und eine knappe Begründung nennen; die konkrete Fassung dort direkt zuordnen.

Bei Sätzen mit nur einer Änderungsart bezeichnet die ID, etwa `S1`, genau eine konkrete Satzüberarbeitung. Mehrere Änderungen derselben Kategorie innerhalb eines Satzes zusammenfassen; unterschiedliche Sätze nicht zu einer Freigabeeinheit bündeln. Bei gemischten Fällen zwei aufeinander aufbauende Fassungen getrennt zeigen:

- `S1-N` im Block „Notwendige Korrekturen“ enthält ausschließlich notwendige Korrekturen. Der Diff vergleicht den Originalsatz mit dieser notwendigen Fassung.
- `S1-O` im Block „Optionale Anregungen“ ergänzt ausschließlich die optionale Überarbeitung. Der Diff vergleicht die notwendige Fassung mit der optional erweiterten Fassung. Ausdrücklich „setzt S1-N voraus“ angeben; die notwendige Fassung ist bereits akzeptabel.

IDs innerhalb des Lektorats beibehalten und nicht neu vergeben. Originalfassung, gegebenenfalls notwendige Zwischenfassung, optionale Endfassung und den Status jeder ID (offen, übernommen, verworfen oder zurückgenommen) im Gespräch nachvollziehbar halten. Bei einer neuen Fassung eine Versionskennung wie `S2-v2` oder `S1-O-v2` verwenden; die Zustimmung zur alten Fassung gilt nicht für die neue. Ändert sich eine notwendige Zwischenfassung, auch den darauf aufbauenden optionalen Vorschlag neu zeigen und freigeben lassen. Satzübergreifende Abhängigkeiten ausdrücklich nennen und nur eine gemeinsam freigegebene, konsistente Kombination anwenden.

Die native Diff-Vorschau bevorzugen, wenn ein tatsächlich verfügbares Werkzeug die genaue vorgeschlagene Änderung vor dem Schreiben anzeigen kann. Keine Vorschauwerkzeuge oder UI-Schaltflächen erfinden. Ist eine solche Vorschau nicht verfügbar, pro Vorschlags-ID genau einen kurzen `diff`-Codeblock mit vollständiger Ausgangsfassung (`-`) und Zielfassung (`+`) ausgeben; bei gemischten Fällen die oben festgelegten Vergleichsstände verwenden. Den Block als Satzvorschlag, nicht als anwendbaren Datei-Patch bezeichnen; keine Auslassungen innerhalb des Satzes verwenden. Keine zusätzliche Word-Diff-Ansicht und keinen zweiten Gesamtdiff im Chat erzeugen. Unveränderte Sätze nicht wiederholen. Wenn weder notwendige noch optionale Änderungen vorgeschlagen werden, keine Diffs erzeugen und keine Freigabe einfordern.

## Granulare Freigabe

Nach den konkreten Vorschlägen um Auswahl anhand der IDs oder Kategorien bitten, etwa: „Welche Vorschläge soll ich übernehmen? Beispielsweise: nur notwendige Korrekturen übernehmen oder S1-N und S1-O übernehmen, S2 verwerfen.“ Diese Frage ist durch den Freigabeablauf dieses Skills begründet; bei Bedarf den Skill verlinken und die einschlägige Regel nennen.

- „S1 übernehmen“ autorisiert ausschließlich die gezeigte Fassung von S1.
- Bei gemischten Fällen die konkrete ID `S1-N` beziehungsweise `S1-O` verwenden. „S1 übernehmen“ ohne eindeutigen Bezug auf eine der beiden Fassungen zunächst klären.
- „Nur notwendige Korrekturen übernehmen“ autorisiert ausschließlich alle aktuell offenen, konkret gezeigten notwendigen Fassungen. Optionale Vorschläge bleiben offen; bereits verworfene Vorschläge bleiben verworfen.
- `S1-O` nur anwenden, wenn `S1-N` bereits übernommen ist oder beide Fassungen eindeutig freigegeben sind. Bei alleiniger Zustimmung zu `S1-O` und noch nicht genehmigtem `S1-N` die Abhängigkeit klären, statt notwendige Änderungen stillschweigend mitzuübernehmen. Ist `S1-N` verworfen, keinen abhängigen optionalen Vorschlag anwenden.
- „Alle übernehmen“ autorisiert alle aktuell offenen, konkret gezeigten Fassungen. Bereits verworfene Vorschläge bleiben verworfen.
- „Übernehmen“ ist bei genau einem offenen Vorschlag eindeutig; bei mehreren Vorschlägen ohne eindeutigen Bezug die Auswahl klären.
- Änderungswünsche wie „S2 kürzer“ zunächst als neue Fassung zeigen. Sie sind keine Freigabe für einen noch nicht gezeigten Wortlaut.
- Eine technische Sandbox-Freigabe ersetzt die inhaltliche Satzfreigabe nicht. Umgekehrt hebt eine Satzfreigabe keine Sandbox-Grenzen auf; erforderliche Schreibberechtigungen über den vorgesehenen Genehmigungsmechanismus anfordern.

## Native Änderungsanzeige und Diff Review

Nach der Freigabe möglichst das verfügbare Patch-Werkzeug verwenden, damit die Codex-Erweiterung die vorgenommenen Dateiänderungen erfassen kann. Auch bei mehreren freigegebenen Sätzen die Änderungen auf die jeweiligen Textstellen begrenzen; mehrere Sätze in derselben Quellzeile nicht durch eine ungeprüfte Ersetzung der gesamten Zeile verändern. Vorhandene Benutzeränderungen erhalten.

Die native Change Summary und die Review-Ansicht für angewendete Änderungen nutzen, soweit sie die installierte Erweiterung anbietet. Im Chat nur kurz ergänzen, welche IDs übernommen wurden und welche offen bleiben. Nicht den gesamten Diff erneut ausgeben. Tatsächlich vorgenommene Änderungen gegen die freigegebenen Fassungen prüfen.

Die native Review-Ansicht kann bereits gespeicherte Änderungen zeigen. Sie ist keine Garantie für „Accept vor dem Speichern“ oder für Freigabeschaltflächen pro Satz. Ein Skill kann diese UI nicht nachrüsten. Niemals ungeprüfte Änderungen vorab anwenden, um Review oder Undo sichtbar zu machen; auch keine Hilfsdateien für eine Vorschau ohne entsprechende Erlaubnis schreiben. Zeigt die Oberfläche keine native Änderungsansicht, einen knappen Diff der tatsächlich angewendeten Änderungen als Ersatz anbieten.

## Rücknahme einzelner Sätze

Nach der Übernahme auf die Möglichkeit „S1 zurücknehmen“ hinweisen. Für die laufende Unterhaltung die ursprüngliche und die angewendete Fassung anhand der Vorschläge nachvollziehbar halten, ohne zusätzliche Sicherungsdateien anzulegen.

- Auf ausdrücklichen Rücknahmewunsch nur die Änderung der genannten ID durch einen gezielten inversen Patch rückgängig machen. Der Rücknahmewunsch ist die inhaltliche Freigabe dafür.
- Bei gemischten Fällen führt „S1-O zurücknehmen“ von der optionalen Endfassung zur notwendigen Zwischenfassung; `S1-N` bleibt übernommen. „S1 vollständig zurücknehmen“ stellt aus der aktuell angewendeten Fassung den Originalsatz wieder her. Die Statusangaben entsprechend aktualisieren.
- Ist die optionale Endfassung noch angewendet, vor einer isolierten Rücknahme von `S1-N` die Abhängigkeit klären. Bei „S1 zurücknehmen“ ohne eindeutigen Bezug klären, ob nur die optionale Änderung oder die gesamte Überarbeitung gemeint ist.
- Vorher prüfen, ob die Stelle noch der angewendeten Fassung entspricht. Bei späteren Benutzeränderungen oder nicht eindeutig rekonstruierbarer Originalfassung keinen veralteten Text darüber schreiben; die konkrete Rücknahme zur Klärung zeigen.
- Native „Undo“-Aktionen können einen ganzen Bearbeitungsschritt oder Turn betreffen. Kein satzgenaues Undo allein durch getrennte Patch-Aufrufe versprechen. Für eine gezielte Rücknahme den Weg über die Satz-ID verwenden.
- Keine gesamte Datei aus Git wiederherstellen und keine fremden Änderungen verwerfen. Nach einer bereits vom Benutzer ausgeführten Rücknahme den tatsächlichen Dateistand berücksichtigen und die Änderung nicht erneut invertieren.

Die verfügbaren Oberflächenfunktionen sind in der [offiziellen Dokumentation der Codex-IDE-Erweiterung](https://learn.chatgpt.com/docs/codex/ide) beschrieben. Funktionsumfang und Beschriftungen können von der installierten Version abhängen.
