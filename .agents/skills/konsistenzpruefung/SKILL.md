---
name: konsistenzpruefung
description: Prüft deutschsprachige wissenschaftliche LaTeX-Arbeiten projektweit oder in einem ausdrücklich gewählten Kapitel beziehungsweise einer einzelnen Datei auf terminologische, sprachliche, strukturelle und LaTeX-bezogene Konsistenz. Verwenden, wenn der Benutzer die gesamte Masterarbeit, ein Kapitel oder eine Datei auf einheitliche Begriffe, Abkürzungen, Schreibweisen, Zeitformen, Personenbezeichnungen, Labels, Verweise und Zitationen untersuchen lassen möchte. Zunächst ausschließlich einen Bericht erstellen und Dateien nur nach ausdrücklicher Freigabe verändern.
---

# Konsistenzprüfung wissenschaftlicher LaTeX-Arbeiten

## Berechtigungsmodell

Die Prüfung standardmäßig ausschließlich lesend durchführen. Keine Datei aufgrund eines Prüfergebnisses verändern, bevor die konkreten Änderungen als Vorschlag gezeigt und ausdrücklich freigegeben wurden.

Dieses Freigabeverfahren als spezielle Regel für `$konsistenzpruefung` behandeln. Allgemeine Anweisungen zum unmittelbaren Bearbeiten von Korrekturen setzen es nicht außer Kraft. Übergeordnete System-, Entwickler- und Sicherheitsanweisungen bleiben unberührt.

## Prüfumfang bestimmen

Den Umfang anhand des Aufrufs bestimmen:

- **Ohne Einschränkung oder „gesamtes Projekt“:** Von `thesis.tex` ausgehen und rekursiv alle aktiven, über `\input` oder `\include` eingebundenen, selbst verfassten `.tex`-Dateien prüfen. `references.bib` ergänzend für Zitationsschlüssel und bibliografische Konsistenz berücksichtigen.
- **„Kapitel N“ oder benanntes Kapitel:** Die zugehörige Kapiteldatei und alle von ihr aktiv eingebundenen `.tex`-Dateien prüfen.
- **„aktuelle Datei“ oder konkrete Datei:** Ausschließlich die genannte beziehungsweise aktuell geöffnete Datei prüfen.

Bei mehrdeutigem Umfang einmal kurz nachfragen. Relative Projektpfade verwenden.

Generierte Dateien wie `.aux`, `.bbl`, `.bcf`, `.blg`, `.fdb_latexmk`, `.fls`, `.log`, `.lof`, `.lot`, `.pdf`, `.run.xml`, `.synctex` und `.toc` sowie `.git` und `.agents` nicht als Inhalt der Masterarbeit prüfen.

## Prüfung durchführen

Den gewählten Umfang systematisch auf folgende Kategorien untersuchen:

1. **Terminologie:** wechselnde Fachbegriffe, Produktnamen, Rollenbezeichnungen und Übersetzungen.
2. **Schreibweise:** Groß- und Kleinschreibung, Bindestriche, Zusammenschreibung, englische Begriffe und typografische Konventionen.
3. **Abkürzungen:** Einführung beim ersten Auftreten, Mehrfachdefinitionen, ausgeschriebene Formen und anschließende Verwendung.
4. **Personenbezeichnungen:** konsistente Gender-Schreibweise und nachvollziehbare Unterscheidung zwischen Studierenden, Versuchspersonen, Teilnehmenden und anderen Rollen.
5. **Zeitformen:** funktional angemessene und innerhalb vergleichbarer Textpassagen konsistente Verwendung. Abgeschlossene Durchführung, allgemeine Aussagen und Verweise auf Tabellen oder Abbildungen nicht blind auf dieselbe Zeitform vereinheitlichen.
6. **Zahlen und Einheiten:** Zahlenschreibweise, Dezimaltrennzeichen, Prozentangaben, Maßeinheiten und Bereiche.
7. **Gliederung:** parallele Überschriften, Nummerierungslogik und einheitliche Benennung vergleichbarer Abschnitte.
8. **LaTeX-Verweise:** verdächtige oder doppelte Labels, nicht auflösbare `\ref`- und `\autoref`-Verweise sowie inkonsistente Label-Präfixe.
9. **Zitationen:** verwendete Zitationsbefehle, fehlende BibTeX-Schlüssel und uneinheitliche Einbindung von Quellen.
10. **Abbildungen und Tabellen:** Benennung, Beschriftung, Verweise und wiederkehrende Darstellungsformen.

Schnelle Textsuche bevorzugt mit `rg` durchführen. Fundstellen anschließend im Kontext lesen, bevor sie als Inkonsistenz bewertet werden.

## Bedeutung vor Einheitlichkeit

Nicht jede sprachliche Variation als Fehler behandeln.

- Begriffe nicht vereinheitlichen, wenn sie fachlich unterschiedliche Konzepte oder Rollen bezeichnen.
- Direkte Zitate, Literaturtitel, URLs, Quellcode, Bezeichner, Zitationsschlüssel und Labels nicht aus rein stilistischen Gründen verändern.
- Zeitformen nach ihrer Aussagefunktion beurteilen.
- Einen Begriff nicht allein deshalb ersetzen, weil eine andere Variante häufiger vorkommt.
- Bei unklarer fachlicher Abgrenzung die Varianten mit Fundstellen darstellen und eine Entscheidung des Benutzers einholen.
- Keine projektweite Konvention erfinden, wenn der Text keine belastbare Präferenz erkennen lässt.

## Empfohlene Form bestimmen

Eine empfohlene einheitliche Form in dieser Reihenfolge ableiten:

1. ausdrücklich im Text, Glossar oder Abkürzungsverzeichnis definierte Form,
2. fachlich notwendige oder domänenspezifisch korrekte Bezeichnung,
3. bei der ersten Einführung erläuterte Form,
4. projektweit überwiegend und korrekt verwendete Form,
5. bestehende sprachliche und typografische Konvention der Arbeit.

Wenn diese Kriterien keine eindeutige Entscheidung erlauben, keine automatische Empfehlung erzwingen, sondern die Entscheidung als offen kennzeichnen.

## Prüfbericht ausgeben

Zunächst keine Diffs und keine Dateiänderungen erzeugen. Den Bericht wie folgt strukturieren:

1. **Prüfumfang:** geprüfte Hauptdatei, Kapitel oder Einzeldatei nennen.
2. **Gesamturteil:** Art und ungefähren Umfang der Inkonsistenzen zusammenfassen.
3. **Fundstellen:** Jede relevante Inkonsistenz mit einer stabilen Kennung, Kategorie, Varianten, relativen Dateipfaden und Zeilennummern aufführen.
4. **Empfehlung:** bevorzugte Form und kurze fachliche Begründung nennen oder die Entscheidung als offen markieren.
5. **Priorität:** zwischen eindeutigem Fehler, relevanter Inkonsistenz und optionaler Vereinheitlichung unterscheiden.
6. **Freigabe:** Fragen, welche Fundstellen oder Kategorien korrigiert werden sollen.

Bei mehr als 20 Fundstellen zuerst eine Zusammenfassung nach Kategorien und die wichtigsten eindeutigen Fehler zeigen. Weitere Fundstellen in überschaubaren Paketen anbieten. Ohne Zustimmung keine zusätzliche Berichtsdatei im Projekt anlegen.

## Änderungen vorschlagen und anwenden

Nach Auswahl konkreter Fundstellen die vorgesehenen Änderungen nach Dateien gruppiert als Unified Diff in `diff`-Codeblöcken darstellen. Geänderte Zeilen vollständig ausgeben und ergänzend die Git-Word-Diff-Schreibweise `[-entfernt-]{+eingefügt+}` als Lesehilfe verwenden.

Vor dem Schreiben nochmals ausdrücklich um Freigabe für die gezeigten Diffs bitten. Eine Zustimmung gilt nur für die dargestellten Änderungen. Nach der Freigabe ausschließlich diese Änderungen anwenden und anschließend mitteilen, welche Dateien verändert wurden. Die tatsächlichen Dateiänderungen können danach zusätzlich im Prism-Diff kontrolliert werden.

Wenn sich eine betroffene Datei zwischen Vorschlag und Freigabe verändert hat, den Diff neu erzeugen und erneut freigeben lassen.

## Recherchegrenze

Die Prüfung standardmäßig nur auf den Projektinhalt stützen. Mögliche fachliche Zweifel kennzeichnen, aber keine externe Fakten- oder Quellenrecherche durchführen, sofern der Benutzer diese nicht ausdrücklich verlangt.