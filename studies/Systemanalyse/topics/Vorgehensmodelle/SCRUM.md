## SCRUM
### empirische Prozess Kontrolle
- Beispiel: Magic Ball
	1. jeder berührt den Ball direkt
	2. Ball muss zwischendurch in der Luft sein
	3. keine direkte Übergabe in die Hand des Nachbarn
		--> Schätzungen der schaffbaren Runden waren anfangs extrem unrealistisch, später relativ genau

### Plan->Do->Check->Act (PDCA)
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/PDCA.drawio.svg]]   
--> Schätzfähigkeit erhöht sich durch PDCA

### SCRUM-Prozess
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/SCRUM-Prozess.drawio.png]]  
### Ablauf der Retrospektive
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/Retrospektive.drawio.svg]]  
--> [Retromat](https://retromat.org): Seite mit Anregungen für Retrospektiven
### USER-Story
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/User-Story.drawio.svg]]  
Erklärung eines Features aus Sicht  
einer Person, die es verwenden möchte  
--> Wert  
--> Ziel

### Burndown-Chart
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/SampleBurndownChart.png]]  
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/Burn_down_chart.png]]  
Statistische Übersicht über geschaffte Storypoints
zur Analyse des Fortschritts und der Geschwindigkeit des Teams

### Rollen im SCRUM
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/SCRUM_Rollen.png]]
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/SCRUM_Rollen_Zusammenspiel.png]]  

### Vorgehen im SCRUM
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/Vorgehen_SCRUM.drawio.svg]]  

### Planing Event
1. realistisches Sprintziel wird formuliert und wie es erreicht werden kann
	- Product Owner + SCRUM Master + Team: **WAS** soll entwickelt werden?
	- Team + SCRUM Master: **WIE** wird entwickelt
	- <span style="color: red">Bekenntnis von jedem Teammitglied</span>

#### Pairing Tabelle
| | MA1 | MA2 | MA3 | MA4 | MA5 | MA6 | MA7 | Anzahl Arbeiter | Anzahl Leiter | 
| :-------- | :--------: | :-------: | :--------: | :-------: | :-------: | :--------: | :---------: | :----------: | :---------: |
| Thema 1 | | leitet | X | X | | | | 3 | 1 |
| Thema 2 | X | X | leitet | | | | X | 4 | 1 |
| Thema 3 | leitet | | | | X | X | | 3 | 1 |
| Anzahl X | 1 | 1 | 1 | 1 | 1 | 1 | 1 | | |
| Anzahl "leitet" | 1 | 1 | 1 | | | |

- mögliche Fragen:
	- Was ist eine Pairing Tabelle?
	- Warum so wenig Themen? --> optimaler Wissensaustausch

### Daily-SCRUM-Event
**verantwortlich: SCRUM-Master**
- Koordination des Teams, um Sprint-Ziel zu erreichen
- Product Owner darf teilnehmen (nur als Zuhörer)
- zu beantwortende Fragen:
	- **WAS** habe ich gemacht?
	- **WAS** werde ich tun?
	- **WAS** hat mich behindert?
- findet am Kanboard statt
- Timebox (15min)

### Retrospektive Event
- mögliche Fragen:
	- PDCA in Retrospektive?
		- entweder:
			- P = Planung durch SCRUM-Master
			- D = Aufzeigen der gesammelten Karten
			- C = Clustern der Karten
			- A = Umsetzung der Punkte
		- oder:
			- Retrospektive = Teil von Check und Act

### Sprint-Review-Event
**verantwortlich: Product Owner**
- Was wollte das Team erreichen?
- Was hat das Team erreicht?
- Gab es Differenzen?
- Teilnehmer:
	- Product Owner, SCRUM-Master, Team, Kunde

### POLICIES
#### Definition of Done (DoD)
- Checkliste
- Festlegung wann <span style="color: red">Einzelaufgabe</span> erledigt ist
- Ziel: Qualitätssteigerung
- Synthese aus TEAM-Anspruch und Unternehmens Quality Management
- Wann bin ich mit jeder Einzelaufgabe fertig?
- Struktur:
	- falsch:
		-  [ ] Nutzer hat Lösung gesehen
	- richtig:
		- [ ] Nutzer: \_\_\_\_ am: \_\_\_\_ hat 

**Aufbau:**

| Kategorie | Aufgaben | <span style="color: red">leicht messbare Kriterien</span> |
| :--------: | :--------- | :----------- |
| A | 1)\_\_\_\_  <br> 2)\_\_\_\_  <br> 3)\_\_\_\_ | Nutzer \_\_\_\_ am \_\_\_\_ <br>Anzahl der Rückfragen \_\_\_\_
| B | 1)\_\_\_\_<br> 2)\_\_\_\_ <br> 3)\_\_\_\_  | |
| C | 1)\_\_\_\_<br> 2)\_\_\_\_<br> 3)\_\_\_\_| |

#### Definition of Ready (DoR)
- Dokumente gehören dem Team!
- Wann kann ich mit einer Einzelaufgabe anfangen (wieder auf jede Karte anwendbar!)
- Aufbau: 

| Kategorie | Aufgabe | <span style="color: red">leicht messbare Kriterien</span> | 
| :----- | :------ | :------ |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |

#### SCRUM-Manifest
- 2001 formuliert
- öffentliches Bekenntnis zu Zielen / Absichten
- dient als Entscheidungshilfe (bei Priorisierung, kein Ausschlussverfahren!)
![[media/pi/modules/Systemanalyse/vorgehensmodelle/scrum/SCRUM_Manifest.png]]  

### Vor- und Nachteile von SCRUM
| Vorteile | Nachteile |
| :------ | :------ |
| Offenheit im Prozess<br>(MA fokussiert) | längere Eingewöhnungsphase |
| Team steht im Vordergrund | für kleine Projekt ungeeignet |
| frühes Scheiter wird unterstützt | hoher Zeitbedarf für Meetings |
| schnelle Reaktion auf neue Anforderungen  | |
| keine Schulden für die Zukunft | |

