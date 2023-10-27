## E*x*treme *P*rogramming (XP)
- leichtgewichtiges Vorgehensmodell
- für kleine / mittlere Teams
- für Projekte mit vagen Anforderungen
- für Projekte mit sich schnell / häufig ändernden Randbedingungen
- verbindet bewährte Techniken des Programmierens in der Arbeitsweise

### bewährte Techniken der Programmierung
| | Programmierung | Testen | Review | Design / Redesign | kurze Releasezyklen |
| :----- | :------ | :------ | :------ | :------- | :------- |
| **Extreme** | Pair-Programming | Test-Driven<br>Development | Pair-Programming | intrinisches Refactoring | Feedback von Kunden<br>ständig einfordern |

### Vorteile Pair-Programming
- Bsp. Experiment in Utah, USA:
	- 13 Einzelprogrammierer
	- 14 Paar-Programmierer
	- 6 Wochen Zeit zur Entwicklung eines Programms
- Ergebnis: **Die Paare waren besser und schneller**
	- bessere Qualität des Programms, mehr Vertrauen in das eigene Programm
	- früher fertig, mehr Spaß, effizienter

### Testen
- Testfälle immer vor der Implementierung erstellen
- Tests laufen automatisch ab --> CI/CD
- Fehlerfall: zuerst neuen Test erstellen, danach Bug beheben
- Testbarkeit

### Design / Redesign
- **alte Zöpfe abschneiden!**
- XP = so einfach wie möglich Programmieren
- Design ist richtig, wenn alle Tests OK sind
- systematisches Redesign
	- `switch/case`-Syntax ==> Polymorphismus statt Conditionals
	- Datenbank-Abfragen nicht in Schleifen
	- Code-Wiederholung vermeiden ==> Extract Method
	- keine globalen Variablen
	- keine Magic Numbers
	- Move Methods  

![[media/pi/modules/Systemanalyse/vorgehensmodelle/xp/Extreme_Programming.drawio.svg]]