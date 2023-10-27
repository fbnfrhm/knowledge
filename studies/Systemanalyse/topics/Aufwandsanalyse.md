## Allgemein
- in jeder Herangehensweise (siehe [[Vorgehensmodelle]]) existieren die selben Phasen
	- Anforderung, Analyse, Entwurf, Implementierung, Integration, Wartung

- Hauptbestandteile der Entwicklungskosten --> i.d.R. das **Personal** --> schwierig vorauszusagen
	- Faustformel: 50000€ pro Mitarbeiter im Jahr
	- Entwicklungsabteilung: $1500h * 100\frac{\text{€}}{h} = 150000\text{€}$ 
	- LOC...Lines of Code
		- <span style="color: red">Schwieriges Maß: gute Programmierer, haben relativ wenig Zeilen, dafür gute Logik</span>
		- pro Mitarbeiter: $x\frac{LOC}{Monat}$ 
		- Beispiel:
			- Software-Produkt hat 21000 LOC
			- durchschnittliche Produktivität pro MA: $3500\frac{LOC}{Jahr}$
			- $\frac{21000LOC}{3500LOC}Jahr=6 \text{ Mann-Jahre}$ 

## Magisches Dreieck & Teufels-Quadrat
![[media/pi/modules/Systemanalyse/vorgehensmodelle/spiralenmodell/magisches_dreieck.png]]  
![[media/pi/modules/Systemanalyse/aufwandsanalyse/teufelsquadrat-l.png]]
- Zieldefinition bei Projektstart
- Steuerung von Änderungen

## Einflussfaktoren einer Schätzung
![[media/pi/modules/Systemanalyse/aufwandsanalyse/Schaetzfaktoren.svg]]
- $f(LOC, Q_1, \text{...}, Q_n,param_LS,p_LS, \text{...}, param_{LS_n})$
	- $Q_n$ = Qualitätsmaße
	- hochkomplexes Funktionsgebirge

## Empirische Schätzverfahren
- basierend auf Erfahrungen
	- (Vergleich mit bisherigen Projekten)

### 1. Expertenschätzung
- Vergleich mit möglichst ähnlich gelagerten Projekten
- Mehr-/Minder-Aufwendungen einfließen lassen

| Vorteile | Nachteile |
| :---- | :---- |
| bei Erfahrung mit Projekt-Art<br>==>  gute Schätzung | von **einer** Person abhängig<br>==> krasse Fehler möglich |
| einfach + billig | |

### Delphi-Methode
- mehrere Experten
- mehrere Runden (aber einzeln)

| Vorteile | Nachteile |
| :----- | :----- |
| i.d.R. konvergiert das Verfahren | Aufwand |
| Ausreißer werden eliminiert | Expertenunverfügbarkeit |

### Zerlegung in kleinere Probleme (Divide et impera)
- in kleinere Teilaufgaben zerlegen
	- diese schätzen
	- Summe der Teilaufwände + Zusammenführungsaufwand = Gesamtaufwand

| Vorteile  | Nachteile | 
| :-------- | :--------- |
| Fehlerwahrscheinlichkeit bei kleinen Aufgaben deutlich geringer | Aufwand |
| Fehler gleichen sich gegenseitig aus | Große+Ganze kann aus dem Blick verloren gehen |
| Meilensteine sind gut ableitbar | Zusammenführungsaufwand könnte vernachlässigt werden |

### SCRUM-Poker
#### Nachteile der anderen Verfahren
- Prognosen ==> Puffer werden eingebaut ==> keine exakte Aussage
- je früher im Projekt desto schwieriger
- je komplexer der Betrachtungsgegenstand desto unschärfere Aussagen
- Laien / unbedarfte Stakeholder Forderungen ==> Verfälschung
- Restriktionen von Außen ==> unrealistische Bewertungen
- **Bestimmte Probleme durch SCRUM-Poker verhinderbar**

- Essentielles von SCRUM:
	- kleine Aufgaben
	- keine Beeinflussung von Außen <== viel Kommunikation

#### Planning Poker (SCRUM)
- Schätzmethode, die von agilen Teams kommt
- STORY-Points: XS, S, M, L, XL (T-Shirt-Größen)
- Referenz-Aufgabe mit **einem** Storypoint
- eher eine Metrik statt Maß für Zeit
- Spielgebunden --> Teamspaß
- empfohlene Gruppengröße = $7\pm2$ Mitarbeiter
![[media/pi/modules/Systemanalyse/aufwandsanalyse/SCRUM-Karten.svg]]

##### Ablauf
1. Scrum-master liest Aufgabe vor
2. stellen von fachlichen Fragen ($\le$ 1min) (optionale)
3. jeder wählt für sich
4. alle Karten werden gleichzeitig nach oben gehoben
5. bei Einigkeit ==> gehe zu 1.
	sonst: Aussprache zwischen dem der den kleinsten Wert und dem, der den größten Wert gezeigt hat (<span style="color:red">Rest der Mitarbeit hat Sendepause</span>)
6. maximal noch einmal zu Punkt 3. gehen (Kleingruppen)

- Best-Practice:
	- Timeboxen einhalten
	- $\le$ 10 Mitarbeiter
	- KISS (*Keep It Short and Simple*)

| Vorteile | Nachteile |
| :------- | :--------- |
| keine Alpha-Tier Meinungen | hoher Zeitaufwand |
| Team besser als Experte | fähiger Scrum-Master(Moderator) notwendig |
| Wissenstransfer | (für ein Team ohne Fachwissen nutzlos) |
| keine Zeitschätzung<br>sondern Komplexität | keine Stundenschätzung |
| "blinde Flecken" können sichtbar weredn | |
| Team-Gedanke |  |
| keine Diskussion bei Einigkeit  | |

#### High-Low-Showdown
- **Ziel:** Stories in S, M, L, XL aufteilen
##### Ablauf
1. jeder bekommt Päkchen (z.B. 5) mit Aufgaben
2. jeder erhält seine Aufgabe und ordnet diese zu
3. jeder kommt nacheinander ran, liest seine Aufgabe vor,
	begründet Zuordnung + legt eine schon zugeordnete Aufgabe um und begründet
==> Entstehen von Gruppen mit ähnlichen Aufwand (Komplexität)

- bei Gruppen mit ähnlichem Hintergrund können auch die [[SCRUM-Karten.svg | SCRUM-Karten]] verwendet werden

## Algorithmische Schätzverfahren
- Kosten-Funktion
- Durchlauf-Funktion

- **Vorher:** Eingangsgrößen richtig schätzen
	- benötige viel Erfahrung
	- bei richtiger Kalibrierung ==> sehr gute Prognose
- Lösungs- / Ergänzungsansatz:
	- COCOMO
	- Function-Point-Methode

### COCOMO-Methode
- COCOMO = Constructive Cost Method  
![[media/pi/modules/Systemanalyse/aufwandsanalyse/COCOMO.drawio.svg]]  
==> $MM_{\text{korrigiert}}=K_{\text{Unternehmen}}*K_{\text{Projekt}}*MM$  
==> <span style="color: red">keine gute Schätzformel</span>

### COCOMO II (© Boehm)
- $MM=2.45*\frac{LOC}{1000}^{1.01+0.01\sum f_i}*K_1*K_2*...*K_{17}$
- $f_i$ = Skalierungsfaktoren
- $K_{1}...K_{17}$ = Kostenfaktoren --> Zuverlässigkeit, Datenbankgröße, Komplexität, Wiederverwendbarkeit

| Skalierungsfaktoren | sehr gering | gering  | OK | hoch | sehr hoch | extra hoch |
| :----- | :------ | :----- | :----- | :------ | :------ | :------ |
| Präzedenzfall | ... | ... | ... | ... | ... | ... |
| Flexibilität | |
| Team | |
| Technologie | |
| Risiko |  |
| Entwicklungsprozess | |

### Function-Point-Methode
- statt Code-Zeilen so schätze werden Function-Points verwendet
- anwendbar als relatives Maß zur Bewertung von (zwei) Funktionen
- © Albrecht, 1977, IBM 
- IPFUG: International Funciton Point User Group
![[media/pi/modules/Systemanalyse/aufwandsanalyse/Function-Point-Methode.drawio.svg]]
- und diese werden klein, mittel, groß zugeordnet  

| Anzahl der Dateneingaben/<br>Anzahl der Datenbestände | 1-4 | 5-15 | \>15 |
| :--: | :--: | :--: | :--: |
| 0-1 | S | S | M |
| 2 | S | M | L |
| \>2 | M | L | L |

### Schätzkriterien
| | S | M | L | $\sum$ |
| :--: | --: | --: | --: | --: | 
| Dateneingabe | \_x3 | \_x4 | \_x6 |
| Datenausgabe | \_x4 | \_x5 | \_x7 | 
| Anfragen | \_x3 | \_x4 | \_x6 | 
| Externe Schnittstellen | \_x5 | \_x7 | \_x10 | 
| Interne Schnittstellen | \_x7 | \_x10 | \_x15 |
| | | | $\underset{\text{Zeilen}}{\sum}$| <span style="color:red">Roh-Function-Point-Wert</span> |
- Menschen-Monate = $FP^{0.4}$
- $\text{MA}_{\text{Anzahl}}=\frac{FP}{150}$ --> Anzahl der Mitarbeiter
