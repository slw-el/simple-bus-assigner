# Busplaner Web App

Eine einfache Webanwendung zur Zuteilung von Gruppen (z.B. Jugendgruppen) auf Reisebusse unter Berücksichtigung von Kapazitäten und Puffern.

---

## English Version Below

---

## 🇩🇪 Busplaner Web App (Deutsch)

### Beschreibung

Diese Webanwendung hilft bei der Planung und Zuteilung von Teilnehmergruppen auf mehrere Reisebusse. Sie berücksichtigt die Kapazität jedes Busses sowie einen optionalen Puffer an freien Plätzen pro Bus. Gruppen können bei Bedarf aufgeteilt werden (maximal auf zwei Busse). Falls eine optimale Zuteilung im ersten Versuch nicht möglich ist, werden bis zu 10 weitere Versuche mit zufälliger Busreihenfolge unternommen, um eine bessere Lösung zu finden. Die Ergebnisse können manuell angepasst und als PDF exportiert werden.

Ursprünglich entwickelt für die Anforderungen der KJF Emsland, aber potenziell auch für andere Anwendungsfälle nutzbar.

### Funktionen

* **Gruppen- und Busverwaltung:**
    * Manuelle Eingabe von Gruppen (Name, Teilnehmerzahl) und Bussen (Kennzeichnung, Sitzplätze).
    * Import von Gruppen und Bussen aus CSV-Dateien (Format: `Name;Wert`, UTF-8 Kodierung wichtig!).
    * Export der eingegebenen Gruppen und Busse als CSV-Datei.
    * Download von CSV-Vorlagen.
* **Zuteilungsalgorithmus:**
    * Berücksichtigung eines einstellbaren Puffers (freie Plätze pro Bus).
    * Zuerst Zuweisung ganzer Gruppen (First Fit Decreasing).
    * Automatische Aufteilung von Gruppen auf maximal zwei Busse, falls nötig.
    * **Retry-Mechanismus:** Bis zu 10 zusätzliche Versuche mit zufälliger Busreihenfolge, falls die erste Zuteilung nicht alle Teilnehmer unterbringt.
* **Ergebnisanzeige:**
    * Übersichtliche Darstellung der Busbelegung (zugewiesene Gruppen/Teile, freie Plätze).
    * Detaillierte Ansicht für aufgeteilte Gruppen.
    * Anzeige nicht zugewiesener Gruppen/Teilnehmer.
* **Manuelle Anpassung:**
    * Verschieben ganzer Gruppen zwischen Bussen (mit Kapazitätsprüfung).
    * Tauschen ganzer Gruppen zwischen Bussen (mit Kapazitätsprüfung).
* **Export:**
    * Download der Zuteilungsergebnisse als PDF-Datei (eine Übersichtsseite + eine Detailseite pro Bus).

### Nutzung

1.  **Starten:** Laden Sie die `index.html`-Datei herunter und öffnen Sie sie in einem modernen Webbrowser (z.B. Chrome, Firefox, Edge). Es ist keine Installation oder Internetverbindung (nach dem Laden der Seite) erforderlich.
2.  **Daten eingeben:**
    * Fügen Sie Gruppen und Busse manuell über die "+ Hinzufügen"-Buttons hinzu.
    * *Oder:* Importieren Sie Gruppen und Busse über die entsprechenden CSV-Dateien. Nutzen Sie bei Bedarf die Vorlagen.
3.  **Puffer einstellen:** Geben Sie die Anzahl der Plätze an, die pro Bus frei bleiben sollen.
4.  **Berechnen:** Klicken Sie auf "Zuteilung berechnen". Die App versucht nun, die beste Zuteilung zu finden (ggf. mit mehreren Versuchen).
5.  **Ergebnis prüfen:** Sehen Sie sich die Zusammenfassung und die Detailansicht der Busbelegung an.
6.  **(Optional) Anpassen:** Nutzen Sie die "Manuelle Anpassung", um Gruppen zu verschieben oder zu tauschen.
7.  **Exportieren:** Laden Sie das Ergebnis als PDF oder die aktuellen Listen als CSV herunter.

### Verwendete Technologien

* HTML5
* CSS3 (mit Tailwind CSS Framework)
* JavaScript (ES6+)
* jsPDF & jsPDF-AutoTable (für den PDF-Export)

---

## 🇬🇧 Bus Planner Web App (English)

### Description

This web application assists in planning and allocating participant groups to multiple coaches/buses. It considers the capacity of each bus and an optional buffer of free seats per bus. Groups can be split if necessary (maximum across two buses). If an optimal allocation isn't found on the first attempt, up to 10 additional attempts with a randomized bus order are made to find a better solution. The results can be manually adjusted and exported as a PDF.

Originally developed for the needs of KJF Emsland (Catholic Youth in the Emsland region, Germany), but potentially usable for other scenarios.

### Features

* **Group and Bus Management:**
    * Manual input of groups (name, number of participants) and buses (identifier, seat capacity).
    * Import groups and buses from CSV files (Format: `Name;Value`, UTF-8 encoding important!).
    * Export the entered groups and buses as CSV files.
    * Download CSV templates.
* **Allocation Algorithm:**
    * Considers an adjustable buffer (reserved seats per bus).
    * Assigns whole groups first (First Fit Decreasing).
    * Automatically splits groups across a maximum of two buses if needed.
    * **Retry Mechanism:** Up to 10 additional attempts with randomized bus order if the initial allocation fails to accommodate all participants.
* **Result Display:**
    * Clear overview of bus assignments (assigned groups/parts, free seats).
    * Detailed view for split groups.
    * Display of unassigned groups/participants.
* **Manual Adjustment:**
    * Move entire groups between buses (with capacity check).
    * Swap entire groups between buses (with capacity check).
* **Export:**
    * Download allocation results as a PDF file (one summary page + one detail page per bus).

### Getting Started

1.  **Run:** Download the `index.html` file and open it in a modern web browser (e.g., Chrome, Firefox, Edge). No installation or internet connection (after loading the page) is required.
2.  **Enter Data:**
    * Add groups and buses manually using the "+ Add" buttons.
    * *Or:* Import groups and buses via the respective CSV files. Use the templates if needed.
3.  **Set Buffer:** Specify the number of seats to remain free on each bus.
4.  **Calculate:** Click "Calculate Allocation" ("Zuteilung berechnen"). The app will attempt to find the best allocation (potentially using multiple tries).
5.  **Review Results:** Check the summary and the detailed view of the bus assignments.
6.  **(Optional) Adjust:** Use the "Manual Adjustment" ("Manuelle Anpassung") section to move or swap groups.
7.  **Export:** Download the results as a PDF or the current lists as CSV.

### Technology Stack

* HTML5
* CSS3 (with Tailwind CSS Framework)
* JavaScript (ES6+)
* jsPDF & jsPDF-AutoTable (for PDF export)
