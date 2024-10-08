# TLM_STRASSEN

This table contains the attributes of the road network in the Swiss National Map (TLM) dataset. The table is based on the TLM_STRASSEN table of the official swisstopo database. 
Here is a summary of the attributes found in the document for the class **TLM_STRASSE**:

## Overview

| **Attributname** | **GDB Code**  | **Datentyp / Wertebereich**  | **Definition**  |
|------------------|---------------|------------------------------|-----------------|
| Shape            | -             | Geometry                     | Polyline Z      |
| OBJEKTART        | -             | Long Integer - Coded Subtype  | Type of road or path (e.g., Autobahn, 10m Strasse, Platz) |
| VERKEHRSBESCHRAENKUNG | -         | Long Integer - Coded Value    | Traffic restrictions (e.g., no traffic, footpath, toll road) |
| TLM_STRASSEN_NAME_UUID | -       | Guid                         | Unique identifier for the road name |
| NAME             | -             | Text (300)                   | Name of the object (e.g., a specific road section like tunnels or bridges) |
| STRASSENNAME     | -             | Text (150)                   | Validated street name from the official register |
| BELAGSART        | -             | Long Integer - Coded Value    | Road surface type (e.g., asphalt, natural) |
| KREISEL          | -             | Long Integer - Coded Value    | Indicates whether the road segment is part of a roundabout |
| VERKEHRSBEDEUTUNG | -            | Long Integer - Coded Value    | Importance of the road in the traffic network (e.g., highway, main road) |
| EIGENTUEMER      | -             | Long Integer - Coded Value    | Owner/maintainer of the road (e.g., federal, cantonal) |
| BEFAHRBARKEIT    | -             | Long Integer - Coded Value    | Drivability (e.g., whether a path is drivable by a car) |
| EROEFFUNGSDATUM  | -             | Date                         | Estimated opening date, recorded when the road is under construction |
| STUFE            | -             | Long Integer - Coded Value    | Vertical level of the road relative to intersecting vectors (e.g., underground, elevated) |

## Attributes

### OBJEKTART Attribute

| GDB Code | Value | Definition |
|-----------|-------|-----------|
| 0 | Ausfahrt | Richtungsgetrennte (baulich getrennt) Ausfahrt ab Autobahnen und Autostrassen. Gerichtet, kann nur in einer Richtung befahren werden. (-) Anschlüsse, die nicht an eine Autobahn oder Autostrasse gekoppelt sind. |
| 1 | Einfahrt | Richtungsgetrennte (baulich getrennt) Einfahrt auf Autobahnen und Autostrassen. Gerichtet, kann nur in einer Richtung befahren werden. (-) Anschlüsse, die nicht an eine Autobahn oder Autostrasse gekoppelt sind. |
| 2 | Autobahn | Autobahnen gemäss Anhang 1 der Durchgangsstrassenverordnung. Es sind die mit der grünen Signalisationstafel (weisses Symbol auf grünem Grund) gekennzeichneten Hochleistungsstrassen. (-) Autostrasse |
| 3 | Raststaette | Transit- und Verkehrsachsen innerhalb von Rastplatzarealen (Infrastruktur zur Verpflegung und zum Ausruhen). Ausschliesslich an Autobahnen und Autostrassen vorkommend. |
| 4 | Verbindung | Dient als virtuelles Verbindungsstück zwischen Achsen, die sich nicht schneiden (z. B. zwischen zwei parallelen Achsen), damit ein geschlossenes Strassennetz dargestellt werden kann. |
| 5 | Zufahrt | Nichtrichtungsgetrennter Strassenabschnitt zwischen Ein- oder Ausfahrt auf, respektive ab einer Hochleistungsstrasse und dem Anschluss an eine Hauptachse. |
| 6 | Dienstzufahrt | Zufahrten zu Hochleistungsstrassen, welche ausschliesslich dem Unterhalt und den Rettungsdiensten dienen, sowie Anschlüsse zu Warteräumen und Zufahrten für die Anlieferung von Raststätten. Alle Arten von Werkzufahrten sind für den privaten Verkehr gesperrt und meistens mit Durchfahrtssperren abgesichert. |
| 8 | 10m Strasse | Alle Strassen, welche überdurchschnittlich breit sind. Es sind vorwiegend blau markierte Hauptstrassen (Ausnahme: Breite Zufahrtstrassen, Fussgängerzone, Industriestrassen, usw.) mit meistens mehr als einer Fahrspur in einer Fahrrichtung, aber keine Autobahnen oder Autostrassen. Breite: > 10.20 m Minimallänge: > 50 m |
| 9 | 6m Strasse | Alle Strassen, auf welchen der Verkehr ungehindert fliessen kann (Ausnahme: Breite Zufahrtstrassen, Fussgängerzone, Industriestrassen, usw.). Es sind vorwiegend Hauptstrassen (blaue Signalisierung) und Quartierstrassen, aber keine Autobahnen oder Autostrassen. Breite: 6.21 - 8.20 m Minimallänge: 50 m |
| 10 | 4m Strasse | Alle Strassen, auf welchen der Personenwagenverkehr ungehindert kreuzen kann (Ausnahme: Verkehrsbeschränkungen). Es sind vorwiegend gut ausgebaute Nebenstrassen (weisse Signalisierung) und Quartierstrassen. Breite: 4.21 - 6.20 m Minimallänge: 50 m |
| 11 | 3m Strasse | Schmale Nebenstrassen, welche meistens mit Fahrzeugen aller Art befahrbar sind. Sie können aber auch unbefahrbar und breiter sein. Breite: 2.81 - 4.20 m Minimallänge: 50 m (+) Unbefahrbare Abschnitte mit einer variablen Breite > 2.80 m (-) Strassen bei landwirtschaftlichen Betrieben (Hofumfahrten). |
| 12 | Platz | Achsen innerhalb von Verkehrsflächen, öffentlichen Parkplatzarealen und privaten Parkplatzarealen, die bezüglich Breite und Lage nicht genau definiert werden können. (-) markierte oder baulich sichtbare Achse auf dem Areal |
| 13 | Autozug | Strecken zwischen den Verladestationen von Autozügen. |
| 14 | Faehre | Strecken zwischen den Anlegestellen von Autofähren. |
| 15 | 2m Weg | Wege, die mit ein- oder mehrachsigen Fahrzeugen (Personenwagen) befahrbar sind. Teilweise können sie aber nur mit Allradantrieb (4WD) oder mit Traktoren befahren werden. Breite: 1.81 - 2.80 m Siedlungsgebiet: alle Wege > 50m Ländliches Gebiet: alle Wege mit Verbindungscharakter; Erschliessungswege zu Objekten > 100m; alle übrigen permanenten Wegstücke > 200m |
| 16 | 1m Weg | Breite: < 1.80 m Siedlungsgebiet: Wege von öffentlichem Interesse (z.B. Verbindungswege) Ländliches Gebiet: alle Wege mit Verbindungscharakter; Erschliessungswege zu Objekten > 100m; alle übrigen permanenten Wegstücke > 200m (+) Alle markierten Wanderwege (keine Minimallänge) (-) Wege der Feinerschliessung zwischen Häusern im Siedlungsgebiet |
| 17 | 1m Wegfragment | Isolierte Wegstücke ohne Anschluss an das übrige Strassen- und Wegnetz. Breite: < 1.80 m Minimallänge: 100 m, wobei Unterbrechungen < 25 m ignoriert werden. |
| 18 | 2m Wegfragment | Isolierte Wegstücke ohne Anschluss an das übrige Strassen- und Wegnetz. Breite: 1.81 - 2.80 m Minimallänge: 200 m, wobei Unterbrechungen < 25 m ignoriert werden. |
| 19 | Markierte Spur | Kein sichtbarer Weg, aber Träger eines markierten Langsamverkehrweges. Minimallänge der Elemente > 25m |
| 20 | 8m Strasse | Hauptstrassen mit blauer Signalisation (Ausnahmen: Breite Zufahrtstrassen, Fussgängerzonen, Industriestrassen, usw...). Autobahnen und Autostrassen sind nicht Teil dieser Objektart. Breite: 8.21 m - 10.20 m Minimallänge: 50 m |
| 21 | Autostrasse | Autostrassen gemäss Anhang 1 der Durchgangsstrassenverordnung. Es sind die mit grünen Signalisationstafeln (weisses Auto auf grünem Grund) gekennzeichneten Hochleistungsstrassen. (-) Autobahn |
| 22 | Klettersteig | Es ist ein mit Eisenleitern, Eisenstiften, Klammern (als Trittstufen) ausgerüsteter Kletterweg. Ein durchgehendes Stahlseil bietet die nötige Sicherheit für Personen mit geeigneter Ausrüstung. (+) Offizielle Klettersteige des Schweizerischen Alpenklubs (SAC). (-) Gesicherte Kletterpartie (-) Ungesicherte Kletterpartie, schwierige Passagen wie exponierte, gefährliche Wege. |
| 23 | Provisorium | Von Kantonen gelieferte Langsamverkehrsachsen (Fuss-, Mountainbike- oder Velowege), die anhand der verfügbaren Luftbilder noch keiner TLM-Objektart zugewiesen werden konnten. |

---

### KUNSTBAUTE Attribute

| GDB Code | Value | Definition |
|-----------|-------|-----------|
| 100 | Keine | - |
| 200 | Bruecke | Brücke |
| 300 | Bruecke mit Galerie | Brücke mit Galerie |
| 400 | Gedeckte Bruecke | Gedeckte Brücke |
| 450 | Bruecke mit Treppe | Brücke mit Treppe |
| 500 | Staudamm | Staudamm |
| 600 | Steg | Steg |
| 700 | Galerie | Galerie |
| 800 | Staumauer, Wehr | Staumauer, Wehr |
| 900 | Treppe | Treppe |
| 1000 | Tunnel | Tunnel zur Unterquerung von topografischen Hindernissen (Berge, Hügel, Felsen) oder andere Unterquerung mit einer Länge > 100m. |
| 1100 | Unterfuehrung | Kurze künstliche Passage zur Unterquerung anderer Verkehrsträger. Gesamtlänge bis 100m. |
| 1200 | Unterfuehrung mit Treppe | Unterführung mit Treppen > 5m auf beiden Seiten. |
| 1300 | Furt | Untiefe in einem Bach- oder Flusslauf, an der das Gewässer mit Fahrzeugen durchquert werden kann. |
| 1400 | in/auf Gebaeude | Strassen- und Wegverbindungen, die auf oder in Gebäuden verlaufen. Häufig kann der Streckenverlauf innerhalb von Gebäuden nicht klar definiert werden. |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### VERKEHRSBESCHRAENKUNG Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 100 | Keine | Keine |
| 200 | Allgemeines Fahrverbot | Allgemeines Fahrverbot |
| 300 | Fussweg | Fussweg |
| 400 | Fussgaengerzone | Fussgängerzone |
| 500 | Gebuehrenpflichtig | Gebührenpflichtige Strassen |
| 600 | Gesicherte Kletterpartie | Gesicherte Kletterpartie |
| 700 | Lastwagenfahrverbot | Lastwagenfahrverbot |
| 800 | Militaerstrasse | Militärstrasse |
| 900 | Radweg | Radweg |
| 1000 | Radweg und Fussweg | Radweg und Fussweg |
| 1100 | Reitweg | Reitweg |
| 1200 | Reitweg und Fussweg | Reitweg und Fussweg |
| 1300 | Rennstrecke | Rennstrecke |
| 1400 | Panzerpiste | Panzerpiste |
| 1500 | Wohnstrasse | Strassen mit Verkehrsberuhigungsmassnahmen |
| 1600 | Teststrecke | Teststrecke |
| 1700 | Wintersperre | Wintersperre |
| 1800 | Zeitlich geregelt | Zeitlich geregelt |
| 1900 | Allgemeine Verkehrsbeschraenkung | Allgemeine Verkehrsbeschränkung |
| 2000 | Gesperrt | Gesperrte Brücken |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### RICHTUNGSGETRENNT Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 1 | Falsch | Falsch |
| 2 | Wahr | Wahr |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### BELAGSART Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 100 | Hart | Hartbelag (z.B. Asphalt oder Beton) |
| 200 | Natur | Naturbelag (z.B. Kies oder Gras) |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### KREISEL Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 1 | Falsch | Falsch |
| 2 | Wahr | Wahr |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### VERKEHRSBEDEUTUNG Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 100 | Hochleistungsstrasse | Alle Ein-, Aus- und Zufahrten auf Autobahnen und Autostrassen, sowie die Autobahnen und Autostrassen selber gelten als Hochleistungsstrassen. |
| 200 | Durchgangsstrasse | Alle Strassensegmente, die gemäss Tabelle „TLM_STRASSENROUTE“ (siehe Kap. 3.4) als „Hauptstrasse A“ oder „Hauptstrasse swisstopo rot“ deklariert sind. |
| 300 | Verbindungsstrasse | Alle Strassensegmente, die gemäss Tabelle „TLM_STRASSENROUTE“ (siehe Kap. 3.4) als „Hauptstrasse B“, „Hauptstrasse C“ oder „Hauptstrasse swisstopo gelb“ deklariert sind. |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### EIGENTUEMER Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 100 | Bund | Bund |
| 200 | Kanton | Kanton |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### BEFAHRBARKEIT Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| 1 | Falsch | Falsch |
| 2 | Wahr | Wahr |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |

---

### STUFE Attribute

| GDB Code | Value | Definition |
|-----------|-------|------------|
| -2 | -2 | Unterirdisch (2. Stufe) |
| -1 | -1 | Unterirdisch (1. Stufe) |
| 0 | 0 | Ebenerdig. Defaultwert für alle Strassen und Gleise. Bei einer Furt erhalten beide sich kreuzenden Achsen (Verkehrsachse/Fliessgewässer) den Wert 0. |
| 1 | 1 | Erhoben oder schwebend (1. Stufe) |
| 2 | 2 | Erhoben oder schwebend (2. Stufe) |
| 999997 | ub | Unbekannt |
| 999998 | k_W | Kein Wert |
| <NULL> | | Nicht erfasst |
