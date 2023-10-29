1. Oberflächen zum Benutzer (GUI, CLI , GUI+CLI, Toolbox, UX, ...)
2. Reichweite (Sprache, Nutzungsintensität)
3. Datenhaltung
4. vorhandene Systemumgebungen nutzbar (?)
5. Hilfesystem
6. Ausbaustufen gewünscht?
7. Verteilung im Netz (Client-Server vs Web-Applikationen)
8. Kostenrahmen

## Hauptaufgabe beim Entwurf einer Software-Architektur
![[media/pi/modules/Systementwicklung/Hauptaufgabe_Entwurf.drawio.svg]]

## Qualitätssicherung
1. Review
2. Tests --> Vergleich mit Zweitlösung
	- mittels Szenarien
		- direkte
		- indirekte: solche, die erst nach Modifikation umgesetzt sind

### Metriken
- Metriken = Messwerte / Ansammlung von Daten

#### [[Entwicklungskonzepte|Kriterien für einen guten Entwurf]]
1. **Verständlichkeit + Präzision**
2. **Anpassbarkeit**
3. **Korrektheit + Vollständigkeit**
4. **Wiederverwendbarkeit**
5. **hohe Kohäsion**
6. **schwache Kopplung**

- 6 Metriken wären formulierbar (Beispiele:)
	- Metrik für Vollständigkeit
		- Anzahl der Anforderungen die unerfüllt sind
		- Anzahl der externen Dienste größer 3
		- Anzahl der unnützen externen Dienste
		- Wie viele Elemente von 3 Schichten-Architektur
	- Metrik für Anpassbarkeit
		- Anzahl involvierter Dateien (elektrisch vorhanden?)
	- Metrik für Verständlichkeit
		- Verwendung von min. 3 Farben


