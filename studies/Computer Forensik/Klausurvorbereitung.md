## IT-Sicherheitsgesetz
- SIEM-Systeme = Security Information and Event Management
		- Zentralisierung, Korrelierung, Analyse der Daten im gesamten System
		- Logverwaltung / -zentralisierung
## Meldepflichten kritischer Infrastrukturen
- „Störungen der Verfügbarkeit, Integrität, Authentizität und Vertraulichkeit ihrer informationstechnischen Systeme, Komponenten oder Prozesse, die zu einem Ausfall oder zu einer erheblichen Beeinträchtigung der Funktionsfähigkeit der von ihnen betriebenen Kritischen Infrastrukturen geführt haben, erhebliche Störungen der Verfügbarkeit, Integrität, Authentizität und Vertraulichkeit ihrer informationstechnischen Systeme, Komponenten oder Prozesse, die zu einem Ausfall oder zu einer erheblichen Beeinträchtigung der Funktionsfähigkeit der von ihnen betriebenen Kritischen Infrastrukturen führen können."
- Die Meldung muss unverzüglich, d.h. ohne schuldhaftes Zögern, erfolgen
- KRITIS-Unternehmen:
	- 1. den Sektoren Energie, Informationstechnik und Telekommunikation, Transport und Verkehr, Gesundheit, Wasser, Ernährung, Finanz- und Versicherungswesen sowie Siedlungsabfallentsorgung angehören und
	- 2. von hoher Bedeutung für das Funktionieren des Gemeinwesens sind, weil durch ihren Ausfall oder ihre Beeinträchtigung erhebliche Versorgungsengpässe oder Gefährdungen für die öffentliche Sicherheit eintreten würden.
- Das Melden eines IT-Sicherheitsvorfalls ist für einen Forensiker nicht verpflichtend. Er kann den Prozess aber anstoßen und mit Genehmigung durchführen. 
- Vorfälle sind nur meldepflichtig, sobald personenbezogene Daten oder eines der Schutzziele betroffen sind.

## Digitale Forensik
>„IT-Forensik ist die streng methodisch vorgenommene Datenanalyse auf Datenträgern und in Computernetzen
   zur Aufklärung von Vorfällen unter Einbeziehung der Möglichkeiten der strategischen Vorbereitung insbesondere aus der Sicht des Anlagenbetreibers eines IT-Systems. “

- Ziele der forensischen Analyse:
	- Identifikation des Angreifers
	- Erkennen der Methode
		- Sicherheitslücke schließen
	- Ermittlung des Schadens
		- relevant für Versicherung und Strafverfahren
		- Ermittlung des Ausmaßes
	- Sicherung der Beweise
		- relevant für Strafrecht, Dokumentation und Nachweis
- Multimedia-Forensik:
	- Auswertung von Bildern & Videos
	- Detektion von Manipulationen
	- Detektion von Personen anhand von Laufverhalten
- Herausforderungen
	- Datenmenge
	- Zeit (Entdeckung eines Vorfalls)

### Digitale Spuren
- Spuren...
	- materielle Veränderungen an Personen oder Objekten
	- stehen im Zusammenhang mit relevanten Ereignissen
	-  können zur Tataufklärung beitragen, da sie Rückschlüsse auf den Tatablauf und den Täter geben
- Digitale Spuren...
	-  basieren auf Daten, welche in Computersystemen gespeichert sind oder übertragen wurden
	- … werden erst durch ihre Interpretation von physischen Spuren über unterschiedliche Interpretationsebenen zu verwertbaren Spuren
- Es gibt keinen Tatort ohne Spuren!

### Locard'sche Prinzip
![[Locardsches Prinzip.png]]
- Alles / Jeder / Immer hinterlässt Spuren!
- Alles kann Spuren enthalten

### Einordnung
- Modell
	- genereller Ablauf einer Untersuchung
- Prozess
	- detaillierter Ablauf einer Untersuchung
	- Reproduzierbarkeit
- Methode
	- Herunterbrechen der Schritte auf Werkzeuge oder verwendete Tools

### Der forensische Prinzip
- Anforderungen an die Vorgehensweise:
	- Akzeptanz : Methoden sind in der Fachwelt anerkannt
	- Glaubwürdigkeit: Funktionalität der Methoden ist nachweisbar
	- Wiederholbarkeit: Ergebnisse ist durch Dritte reproduzierbar
	- Integrität: Spuren werden durch Untersuchung nicht verändert
	- Ursache und Auswirkungen: Verbindung zwischen digitalen Spuren, Ereignissen und Personen sind herstellbar
	- Dokumentation: Ermittlungsprozess ist nachvollziehbar dokumentier

## Forensic Readiness
> ...  beschäftigt sich mit Maßnahmen zur Vorbereitung auf digitale forensische Untersuchungen innerhalb Organisationen

- Ziele der Forensic Readiness
	- Systeme sollen in der Lage sein, bessere und belastbarere digitale Spuren zu sammeln
	- Die Kosten für eine forensische Untersuchung sollen verringert werden

- technische Maßnahmen: Konfiguration für umfangreiches Logging zur vereinfachten Analyse des Systems
### Dimensionen 
- Grundlage:
	- rechtlich
- Maßnahmen & Methoden:
	- personell 
	- technisch
	- organisatorisch

### forensischer Arbeitsplatz
- 3 Rechner für unterschiedliche Aufgaben
	- Forensische Workstation
		- bessere HW auf aktuellem Stand der Technik
		- Dualboot 
		- Virenscanner und Firewall
	- Office Computer für Schriftsachen
		- Verschlüsselung notwendig
		- Interne Netzwerkanbindung, kein Internetzugang!
	- Internet Computer
		- keine sensiblen Daten eingeben oder speichern
		- Aktuelle Anti-Viren-SW
		- auch als VM einsetzbar!

## Datensammlung
- Vorauswahl an geeigneten Werkzeugen für ausgewählte Datenquellen treffen
- eigene Forensik-Datenträger: von Daten aus früheren Vorgängen "säubern
- Forensisches Duplikat der Daten erstellen
- Integrität der Beweiskette sichern und somit Sicherung der Beweiskraft!

### Beweisführung im Zivil- oder Strafverfahren
- Die Sicherung von digitalen Beweisspuren kann auf zwei Arten geschehen:
![[Beweisführung.png]]

### Post Mortem Forensics
- Physikalsiche Ebene
- Datenträgerkopie

| Vorteile                             | Nachteile               |
| ------------------------------------ | ----------------------- |
| Vollständiges Abbild                 | Datensicherungsdauer    |
| Virtualisierung nachträglich möglich | Größe                   |
| Formatwandelbarkeit                  | Externe Spezialhardware |

- Wie und wohin?
	- Schreibgeschützt extern auf extern
	- Schreibgeschützt intern auf extern
	- Live Boot CD / USB

### Live Forensik
- Dateien
- gelöschte Daten?
- Datenbanken
- Cloud Speicher
- Entschlüsselte Inhalte
- RAM
- Netzwerkverbindungen

| Vorteile                     | Nachteile                 |
| ---------------------------- | ------------------------- |
| Schnell und effizient        | Veränderung am System     |
| geringe Größe                | Selektierter Datenbestand |
| Ohne externe Spezialhardware | Formatauswahl             |
| Sicherung flüchtiger Daten   |                           |
- Wie und wohin?
	- logisch / physikalisch selektiv
	- Externe Datenträger / Netzwerk

### Sicherung digitaler Beweismittel und Spuren
- keine Veränderungen am System + Dokumentation
- forensische Untersuchungen müssen nachvollziehbar und reproduzierbar sein!

### Analyse digitaler Beweismittel
- mögliche forensische Methoden
	- Wiederherstellen gelöschter Objekte
	- Hashwertüberprüfungen
	- File Carving
		- Untersuchung von Dateien anhand der reinen Dateiinformationen / -daten, ohne Verwendung des Betriebssystems
	- Textsuchen
	- Slack-Untersuchungen
		- Chatverläufe und Co. untersuchen

# Wiederholung I
- Schreibschutzadapter
	- HW-Bauteil, das nur einen Lesezugriff auf das angeschlossene System ermöglicht, verhindert eine Veränderung der Daten auf ebendiesen.
- Post-mortem Forensik
	- Analyse von Datenträgern, derer Trägersystem nicht mehr läuft. Bspw. über Live USB Stick
- Live Forensik
	- Analyse auf aktivem System, Analyse & Sicherung von flüchtigen Daten, Umgehen möglicher Sicherheitsmaßnahmen (Anmeldung + Verschlüsselung)
- Forensic Readiness
	- Vorbereitung eines Systems zur Erleichterung der Analyse, Konfiguration von Logging
- Digitale Spuren
	- Veränderungen / Hinterlassenschaften an physischen / virtuellen Objekten
	- Auswertung von Daten auf zu untersuchenden Geräten und Netzwerken, können teilweise flüchtig sein
- Locard'sche Prinzip
	- Jede Interaktion hinterlässt Spuren
	- kein Tatort kann ohne Spuren von Täter / Opfer / Anderen verlassen werden
- S-A-P-Modell
	- Secure: Daten sichern & Erfassen
	- Analyse: Auf die relevanten Daten spezifizieren, analysieren und Fehler / Probleme / Spuren finden
	- Present: Rückschlüsse darstellen und dokumentieren
- Dunkelfeld
	- nicht-gemeldete Vorfälle, aus Angst vor Konsequenzen (Prestigeverlust) oder für die schnellere Lösung
- Multimedia-Forensik
	- Analyse von Multimedia-Inhalten (Bilder / Videos)
	- Erkennen von Manipulation, Personen, etc.