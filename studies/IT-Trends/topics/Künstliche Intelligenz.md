# Begriff
> [...] ist ein Teilgebiet der Informatik, das sich mit der Automatisierung intelligenten Verhaltens und dem maschinellen Lernen befasst.
> Meist bezeichnet künstliche Intelligenz den Versuch, bestimmte Entscheidungsstrukturen des Menschen nachzubilden, indem z.B. ein Computer so gebaut und programmiert wird, dass er relativ eigenständig Probleme bearbeiten kann.
> --- Wikipedia

## Beispiele
- KI-unterstütze Oberflächen
- KI-unterstützte Prozessautomatisierung
- **Sprachautomatisierung**

### Big Data
- KI-unterstützte IT-Operationen
- KI-unterstützte IT-Tools
- KI-unterstützte IT-Prozesse
- z.B. Kartenzahlung

# Machine Learning
--> künstliche Intelligenz, Neuronale Netze, Machine Learning, Deep Learning

> Computer bekommen die Fähigkeit zu lernen
>und sich durch Experimente zu verbessern
>--- Arthur Samuel

> [...] ein Programm-System um autonom zu lernen
> und sich durch Experimente zu verbessern.
> --- Tom M. Mitchell

- Beispiele:
	- Bilderkennung
	- Prinzipien in Daten folgen
	- natürliche Sprache erkennen  
- Beispiel:
	- Eingabe: Computerbild
	- Ausgabe:
		- Objekte erkennen und zählen
		- Szenen erkennen
		- Personen erkennen
		- semantische Einteilung
		- Bilder deuten

## mathematischer Hintergrund
![[ML_math_1.drawio.svg]]
- Menge von Funktionen (parametrisiert)  $F=\{f_p: f_p: \Omega \rightarrow \Psi\}$
- Es gibt eine Güte-Funktion  (Fehler, Verlust, Risiko, ...)
	- $L(y,f_p(x))$  
- Vorstellung von dieser Güte-Funktion:  
![[ML_math_2.drawio.svg]]
- $f_p(x)=\tilde y$, eigentlich will ich bei $y$ landen ==> Güte-Funktion gibt an, wie weit $\tilde y$ von $y$ weg ist.
- Ziel: Suche die beste Funktion $f_*$, die den kleinsten Fehler macht
	- $f_* =\underset{f_p \in F}{\text{argmin}} \int_{\Omega} \int_{\Psi}L(y,f_p(x))\space p(x,y) \,dy\,dx$
	- Beispiel: Menge aller `.jpg`-Bilder  
![[ML_math_3.drawio.svg]]
- Wir haben ein Cluster für $\underset{y_1}{\text{Frauen}}/\underset{y_2}{\text{Männer}}$
- <span style="color: red">Suchen über gesamten</span> $\Psi$ <span style="color: red">und über gesamten</span> $\Omega$ <span style="color: red">die Funktionen mit dem kleinsten Fehler</span>

## DeepLens-Beispiel
![[DeepLens.drawio.svg]]

## Datenanalyse-Paradigmen
1. Erkennen ohne zu lernen
![[DAP_Zelle.drawio.svg]]
2. Erkennen mit Anlernphase durch Feature-Design
- **Ablauf:**
	- $f(x,para_1)=z_1$ 
		- $\tilde{f}(z_1,para_2)=z_2$ 
			- $\tilde{f}(z_2,para_3)=y$

- Best Practice:
	1. Repräsentation von Layern verstehen (statt selber zu designen)
	2. Layer kombinieren ==> Modell für unseren Fall *"entdecken"*

## Schwierigkeiten beim Deep Machine Learning
- Nur Zahlen als Input
- Hintergrundbilder und Vordergrundbilder mischen sich
- große Variabilität 
	- z.B. Auto ==> Blickrichtung; Modelle mit 3, 4 oder 6 Rädern; Beleuchtung
	- z.B. PKW$\ne$LKW für Techniker, aber für Biologen: PKW$=$LKW
- kleine Unterscheidungseigenschaften
	- z.B. Mountainbike, City-Bike, E-Bike
- <span style="color:red;font-weight:bold">! WIR HABEN NIE GENUG DATEN !</span> 

## Beispiele und Unterscheidung von ML-Anwendungen
### Klassifikation
- z.B. AWS Detection, [ClarifAI](https://clarifai.com) 
- Erkennung von Eigenschaften in einem Bild (Was ist das für ein Bild? / Wie sieht die Person aus? (glücklich, alt, usw.))

### Objekt-Erkennung
- z.B. AWS Rekognition
- Image Captioning / Gesichtserkennung

### Text-Erkennung
- z.B. Amazon-Textract
- Erkennung und Übersetzung von (handschriftlichen) Texten in digitale Formate (z.B. Word, .txt-Datei, usw.)

### ML-Algorithmen bei NVIDIA (lokale Lösungen)
- Texterkennung über Leistung der Grafikkarte durch Nutzung eines Dockers und Python
- (Stichwörter: nvidia, devblogs)

# Deep Learning
![[Deep_Learning.drawio.svg]]

## Aufbau eines Neuronen in einem Layer
![[DL_Neuronen_Aufbau.drawio.svg]]

## Aufbau eines Layers
![[DL_Layer_Aufbau.drawio.svg]]

## Neuronales Netz - Layer
![[NN_Bestandteile.drawio.svg]]

## Neuronales Netz - Aufbau
![[Neuronales_Netz.drawio.svg]]
- **Empfehlung:** Erfahrungen für ähnliche Probleme aus Communitys holen
	- deeper ... viele Eingangsdaten
	- flacher ... Laufzeit bei Nutzung relevant
	- **vortrainiertes Netzwerk ist immer zu bevorzugen !!!**
- Software-Beispiele:
	- Coffee (Borklay)
	- Tensorflow (Google)
	- C++
	- Python
	- NVIDIA-CUDA