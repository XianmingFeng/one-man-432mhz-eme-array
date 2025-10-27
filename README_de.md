# Tragbare 432MHz (70cm) EME Yagi-Array

**Ein leichtes, werkzeugloses, von einer Person tragbares 2x2x14-Element-Yagi-Array für 432 MHz EME-Betrieb.**

---

## Übersicht

Dieses Projekt stellt ein Open-Source-Design für ein 432 MHz (70cm) EME (Erde-Mond-Erde) Antennen-Array vor.

Die Motivation für dieses Design ergibt sich aus einem persönlichen Bedürfnis: Da es nicht möglich ist, permanente Antennen zu Hause zu installieren, musste die gesamte Amateurfunkausrüstung auf Tragbarkeit ausgelegt sein. Dieses Antennensystem ist die Lösung für Funkamateure, die für den Betrieb ins Feld gehen müssen.

Während traditionelle EME-Arrays oft groß und fest installiert sind, konzentriert sich dieses Design darauf, den minimal erforderlichen Gewinn für EME zu erreichen, wobei **Tragbarkeit, geringes Gewicht und schneller Aufbau durch eine Person** im Vordergrund stehen.

## Praxiserprobter Einsatz & Flugreisen

Dieses System ist nicht nur ein Konzept. Seine Benutzerfreundlichkeit wurde während der **VK9QO Christmas Island DXpedition im Jahr 2025** erfolgreich bestätigt.

Das gesamte System erfüllt die Anforderungen für Flugreisen und kann als Gepäck aufgegeben werden. Dies macht es zu einer idealen und bewährten Lösung für "Rovers" und DXpeditionen, die Hochgewinn-Ausrüstung zu entlegenen oder seltenen DXCC-Gebieten transportieren möchten, um EME-Betrieb durchzuführen.

## Hauptmerkmale

* **Ein-Personen-Tragbarkeit:** Das Gesamtgewicht des gesamten Array-Systems, einschließlich der Tragetasche, liegt **unter 10 kg**.
* **Kompakte Lagerung:** Alle Komponenten sind so konzipiert, dass sie in einer einzigen Angelrutentasche verstaut werden können, was den Transport durch eine Person erleichtert.
* **Werkzeuglose Montage:** Für den Aufbau oder Abbau im Feld sind keine Werkzeuge (Schraubendreher, Schraubenschlüssel usw.) erforderlich. Der gesamte Vorgang kann von Hand durchgeführt werden.
* **Schneller Auf- und Abbau:** Das Design ist auf Geschwindigkeit optimiert. Dies wird erreicht durch:
    * Minimierung der Anzahl loser Teile.
    * Die meisten Komponenten bleiben während der Lagerung als eine Einheit verbunden.
    * Verwendung eines einfachen "Ausklappen-und-Verriegeln" und "Entriegeln-und-Einklappen"-Mechanismus für Auf- und Abbau.

## Designphilosophie: Zugänglichkeit & Niedrige Kosten

Ein Hauptziel dieses Projekts ist es, jedem den einfachen Bau dieses Antennensystems zu ermöglichen. Das Design vermeidet bewusst komplexe Bearbeitungsprozesse (wie CNC-Fräsen), um die Einstiegshürde zu senken.

Bastler sollten in der Lage sein, die gesamte Antenne mit nur den grundlegendsten Werkzeugen fertigzustellen:
* Handbohrmaschine (Pistolenbohrer)
* Handsäge
* Handnietzange
* Rohrbieger
* 3D-Drucker (Alle erforderlichen `.step`-Dateien finden Sie im Verzeichnis [`/CAD/3d_print`](/CAD/3d_print))

**Ein Hinweis zu 3D-Druckern:** Wir verstehen, dass nicht jeder einen 3D-Drucker besitzt. Jedoch:
1.  Die Zugänglichkeit und Erschwinglichkeit eines 3D-Druckers für zu Hause sind deutlich höher als die einer CNC-Maschine.
2.  Selbst wenn Sie keinen besitzen, ist die Nutzung eines 3D-Druckdienstes weitaus kostengünstiger und zugänglicher als die Beauftragung von CNC-gefertigten Teilen.

## Technische Daten

* **Band:** 432 MHz (70cm)
* **Array-Konfiguration:** 2x2x14-Element-Yagi-Array (Vier 14-Element-Yagis in einem 2x2-Raster gestockt).
* **Polarisation:** Horizontal.
* **Stocking-Rahmen:** Benutzerdefinierter H-Rahmen.

## Montagesystem (Stativ)

Das Array-System ist für die Montage auf einem Standard-Stativ ausgelegt. Die Verbindung erfolgt über das 3D-gedruckte Teil **`spearder_mount`** (Dateien verfügbar in `/CAD/3d_print`).

Diese Halterung verbindet den H-Rahmen des Arrays mit der Schnellwechselplatte (QR-Platte) eines Stativkopfes.

**Anforderungen an die Schnellwechselplatte:**
Das `spearder_mount`-Teil ist vielseitig konzipiert. Es ist kompatibel mit jeder QR-Platte mit Langloch, die diese Kriterien erfüllt:
* **Länge:** Größer als 80 mm.
* **Befestigung:** Verwendet einen langen Schlitz für die Schraube (kein einzelnes Loch mit fester Position).
* **Schraube:** Kompatibel mit einer standardmäßigen 1/4-Zoll (imperial) Stativschraube.

*Als Beispiel verwendet der Autor eine 38 mm breite Arca-Swiss-kompatible QR-Platte in Kombination mit einem Fluid-Videokopf.*

**Stativ-Empfehlung:**
Es wird dringend empfohlen, ein Stativ mit einer **Mindesthöhe von 1,8 Metern** zu verwenden.

* **Grund:** Ein zu kurzes Stativ führt dazu, dass das hintere Ende des Antennen-Arrays bei der Drehung zu hohen Elevationswinkeln (z. B. beim Verfolgen des Mondes) auf den Boden trifft oder schleift.

## Designdetails

### H-Rahmen Stocking-System

Der H-Rahmen, der zum Stocken der vier Yagis verwendet wird, ist für einen werkzeuglosen, schnellen Aufbau konzipiert. Sein Design ist inspiriert vom Klappbeinmechanismus eines tragbaren Tisches. Dieses Konzept ermöglicht es, den Rahmen in Sekunden auszuklappen und zu verriegeln oder zu entriegeln und zur Lagerung zusammenzuklappen.

*Die ursprüngliche Idee für dieses klappbare H-Rahmen-Konzept stammt von **BI1QGX**.*

### Modifizierte 14-Element-Yagi

Das Grunddesign der 14-Element-Yagi basiert auf der **[GTV 70-14m von DG7YBN](https://dg7ybn.de/432MHz/GTV70_14.htm)**.

#### Elektrisches Design & Boom-Korrektur

Das elektrische Design übernimmt die Daten von DG7YBN und wendet einen Boom-Korrektur (BC)-Faktor an, um die Auswirkungen des leitenden 20x20x1mm Vierkant-Aluminiumbooms zu kompensieren. Die Elemente sind 5 mm über dem Boom montiert (Abstand von der Unterseite des Elements zur Oberseite des Booms).

Die folgende Tabelle zeigt die ursprüngliche NEC-Freiraumlänge (FL NEC), die endgültige boomkorrigierte Länge (BC) und die erforderliche halbe Länge (Half L) für die Elementkonstruktion.

| \[mm\] | Diam | Pos Boom | FL NEC | BC | Half L |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Refl | 8 | 40 | 328 | 330.7 | 165.35 |
| DE | 10 | 144.5 | 313.4 | 316.1 | 158.05 |
| D1 | 8 | 193 | 309 | 311.7 | 155.85 |
| D2 | 8 | 286 | 304 | 306.7 | 153.35 |
| D3 | 8 | 468 | 292 | 294.7 | 147.35 |
| D4 | 8 | 681 | 286 | 288.7 | 144.35 |
| D5 | 8 | 928 | 282 | 284.7 | 142.35 |
| D6 | 8 | 1192 | 279 | 281.7 | 140.85 |
| D7 | 8 | 1477 | 274.5 | 277.2 | 138.6 |
| D8 | 8 | 1764 | 271 | 273.7 | 136.85 |
| D9 | 8 | 2054 | 268 | 270.7 | 135.35 |
| D10 | 8 | 2345 | 266 | 268.7 | 134.35 |
| D11 | 8 | 2627 | 264 | 266.7 | 133.35 |
| D12 | 8 | 2860 | 256 | 258.7 | 129.35 |

Eine detaillierte Erklärung zur Boom-Korrektur-Methodik finden Sie auf [DG7YBNs BC-Seite](https://dg7ybn.de/BC_numbers/BC.htm).

#### Mechanische Optimierungen

Zusätzlich zum elektrischen Design führt dieses Projekt signifikante *mechanische* Modifikationen am ursprünglichen Design ein, um es für Tragbarkeit und schnelle Montage zu optimieren. Zu diesen Optimierungen gehören:
* Neu gestaltete Boom-Segmente und Klappscharniere.
* Ein neues Feedbox-Design.
* Ein spezielles Element-Befestigungssystem (siehe unten).

#### Elementhalterung (Das `element_mount`-Teil)

Ein Hauptmerkmal dieses Designs ist die 3D-gedruckte Elementhalterung (`element_mount.step`), die für alle parasitären Elemente (Reflektoren und Direktoren) verwendet wird.

* **Zwei-Schlitz-Design:** Das Teil verfügt über zwei Schlitze. Ein Schlitz hält das Element im Betrieb senkrecht zum Boom. Ein zweiter Schlitz in einem fast senkrechten Winkel dient dazu, das Element in seiner zusammengeklappten (verstauten) Position zu halten.
* **Störungsfreie Lagerung:** Der "Lager"-Schlitz ist absichtlich um einen kleinen Winkel (den `parking_angle`) versetzt. Dies stellt sicher, dass die Elemente im zusammengeklappten Zustand nicht perfekt parallel zum Boom liegen, wodurch verhindert wird, dass sie mit benachbarten Elementen oder den Köpfen der Befestigungsschrauben kollidieren.
* **Parametrisches Allzweck-Design:** Diese Elementhalterung ist ein universelles Allzweck-Design, das für viele Yagi-Projekte geeignet ist, die Vierkant-Booms und Rund-Elemente verwenden. Es wurde als eigenes **parametrisches OpenSCAD-Projekt** veröffentlicht.

Für vollständige Details, Parameter (zur Anpassung an Ihre eigene Boomgröße, Elementdurchmesser, Lagerwinkel usw.) und `.scad`-Dateien besuchen Sie bitte das dedizierte Projekt-Repository:
**[https://github.com/XianmingFeng/yagi_element_mounting](https://github.com/XianmingFeng/yagi_element_mounting)**

## Stückliste (BOM)

Dies ist eine unvollständige Stückliste und wird im Laufe des Projekts aktualisiert. (Hinweis: Die Teilenamen sind spezifisch und wurden beibehalten.)

| Kategorie | Teil | Menge |
| :--- | :--- | :--- |
| Yagi-Elemente & Feedbox | `element_mount` 3D-Druckteil | 52 |
| | Zylinderkopfschraube (Halbgewinde) M3x40 | 52 |
| | Flügelmutter M3 | 56 |
| | `feed_box_front` 3D-Druckteil | 4 |
| | `feed_box_middle` 3D-Druckteil | 4 |
| | `feed_box_rear` 3D-Druckteil | 4 |
| | `feed_box_isolator` 3D-Druckteil | 4 |
| | Linsenkopf-Innensechskantschraube M3x8 | 8 |
| | Zylinderkopfschraube M3x40 | 4 |
| | Rändelmutter Messing (Einschmelzmutter) M3x4x5 | 36 |
| | Zylinderkopfschraube M3x24 | 28 |
| | Kupfer-Kabelschuh RNB-1.25-4 | 16 |
| | | |
| Yagi-Boom-Klappmechanismus | Kleiner Doppelfeder-Kippverschluss (ohne Schlossloch) | 8 |
| | Verschluss-Gegenhaken A320B-0-2 | 8 |
| | Eisen-Gänsehalsscharnier 20mm | 16 |
| | Rundkopf-Blindniete M4x5 | 96 |
| | `boom_hinge_cap_front` 3D-Druckteil | 8 |
| | `boom_hinge_cap_rear` 3D-Druckteil | 8 |
| Boom-zu-H-Rahmen Schnellspanner | Vierkantrohr 2-Wege T-Verbinder 25x25 | 4 |
| | Flügelschraube M6x30 | 4 |
| | Flügelmutter M6 | 4 |
| | V-Federclip F5mm Einzelstift (Hohl), L:37mm H:8mm | 4 |
| | Rundkopf-Blindniete M5x8 | 8 |
| H-Rahmen Klappmechanismus | 90-Grad Klapptischbein-Scharnier, Mini-Größe, Rechts | 2 |
| | 90-Grad Klapptischbein-Scharnier, Mini-Größe, Links | 2 |
| | Rundkopf-Blindniete M5x6 | 24 |

## Inhalt des Repositorys

* **`/CAD`**: Enthält alle 3D-Modelldateien.
    * **`/CAD/3d_print`**: Enthält `.step`-Dateien für alle 3D-gedruckten Teile, geordnet nach Komponenten:
        * `boom_hinge/`: Teile für das Yagi-Boom-Klappscharnier.
        * `drilling_jig/`: Schablonen für präzises Bohren.
        * `element_mount/`: Die universelle Halterung für parasitäre Elemente.
        * `feed_box/`: Teile für die Feedbox des gespeisten Elements.
        * `spearder_mount/`: Halterung zur Verbindung des H-Rahmens mit einem Stativ.
    * **`/CAD/aluminum_pipe`**: Enthält `.step`-Dateien für alle Aluminiumrohr-/-Vierkantrohr-Komponenten als Referenz und zur Bemaßung.
* **`LICENSE`**: Die Open-Source-Lizenz des Projekts.
* **`README.md`**: Diese Datei (Englisch).
* **`README_zh.md`**: Chinesische Übersetzung.
* **`README_de.md`**: Deutsche Übersetzung.
* **`README_ja.md`**: Japanische Übersetzung.

## Projektstatus

* **Jetzt verfügbar:**
    * Initiale 3D-CAD-Dateien (`.step`) für alle 3D-gedruckten Teile und Aluminiumkomponenten sind im Verzeichnis `/CAD` verfügbar.
    * Elektrische Designdaten (Elementlängen und -positionen) sind in dieser README enthalten.
    * Eine unvollständige Stückliste (BOM) ist jetzt verfügbar.
* **Wird hinzugefügt:**
    * Vollständige Stückliste (BOM) (z. B. spezifische Aluminiumrohrgrößen, Schrauben).
    * Detaillierte Montageanleitungen & Fotos/Videos.
    * Simulationsdateien (z. B. EZNEC/4nec2).
    * Druckfertige `.stl`-Dateien (empfohlen).

## Danksagungen

* **DG7YBN** für das ursprüngliche [GTV 70-14m](https://dg7ybn.de/432MHz/GTV70_14.htm) Antennendesign und die [Boom-Korrektur-Methodik](https://dg7ybn.de/BC_numbers/BC.htm).
* **BI1QGX** für das Grundkonzept des klappbaren H-Rahmens.

## Lizenz

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
