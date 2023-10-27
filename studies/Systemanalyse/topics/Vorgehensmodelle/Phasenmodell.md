## Phasenmodell (Wasserfallmodell)
```mermaid
flowchart TD
A["Analyse"]
A-->B["Design"]
B-->C["Programmierung"]
C-->D["Integration / Test"]
D-->E["Einsatz / Wartung"]
```
### 2.1.1. Analyse-Phase
- Bestimmung des Funktionsumfangs
- User-Interface
- Leistungsverhalten
- Termine
--> **Ergebnis:** Lastenheft
--> **Problem:** Fehlerfortpflanzung

### 2.1.2. Design-Phase
- innere Struktur der Software nach Produktdefinition  
--> Zerlegung in Komponenten  
--> **Ergebnis:** Pflichtenheft

### 2.1.3. Programmierung
- Implementierung der Komponenten anhand des Entwurfs
- Programmieren im Kleinen  
--> einzeln getesten Module (sind noch nicht lauffähig)

### 2.1.4. Integrations- und Test-Phase
- nacheinander werden Einzelkomponenten hinzugefügt
- weitere Tests
- Abnahme-Tests
- Installation  
--> Gesamtsystem, mit abschließenden Systemtest, der Konsistenz zur Produktdefinition prüft

### Vor- und Nachteile
| Vorteile | Nachteile |
| :------- | :-------- |
| wenige/einfache Schritte <br>klare Struktur<br>Ende des Projektes fixiert/absehbar<br>weniger komplex | Anforderungsänderungen nicht möglich<br>MVP fehlt<br>Wissenstransfer nicht unterstützt<br>ohne Rückkopplungen<br>kein experimentelles Vorgehen<br>Testen erst am Ende |

## iteriertes Phasenmodell
```mermaid
flowchart TD
A["Anforderung"]
A-->B["Design"]
B-->A
B-->C["Umsetzung"]
C-->B
C-->D["Integration / Test"]
D-->C
D-->E["Auslieferung / Wartung"]
E-->D
```
--> hat sich nicht durchgesetzt
