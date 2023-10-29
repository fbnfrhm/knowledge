- Erfahrungen in OO-Entwurf werden anderen zur Verfügung gestellt
- Wiederverwendung (Klassen + Beziehungen zueinander)

| Prozess der Erzeugung | Komposition von Klassen | Verhalten |
| :---- | :---- | :----- |
| Singleton | Proxy | Interpreter |
| Factory | Adapter | Command |
| Builder | Bridge | Iterator | 
| | Composite | |
- Literatur: [Design Patterns (Gamma, Helma, Johnson, Vlissides)(GoF)](https://en.wikipedia.org/wiki/Design_Patterns)
## Model-View-Controller
- Die Daten sind genau einmal vorhanden  
![[media/pi/modules/Systementwicklung/MVC_1.drawio.svg]]
![[media/pi/modules/Systementwicklung/MVC_2.drawio.svg]]  
![[media/pi/modules/Systementwicklung/MVC_3.drawio.svg]]
- Vorteil:
	- getrennte Datenhaltung
		- mehrere Views für gleiche Daten möglich

## Factory-Muster
> Schnittstelle wird zur Verfügung gestellt mit der eine Familie von Objekten erzeugt werden können.
> (konkrete Klasse muss nicht bekannt sein)

![[media/pi/modules/Systementwicklung/Factory-Muster.drawio.svg]]
 - Warum funktioniert das Factory-Muster?
	 - Polymorphismus

## Singleton
> Instanz erzeugen wird verhindert (private)!

```c++
class DHGE {
private:
	// Instanz erzeugen wird VERHINDERT!
	DHGE(DHGE&){}
	DHGE(){}
	Operator=(DHGE&);

public:
	static DHGE& getInstance(){
	// ...
	// some code
	// ...
	}
}
```
- z.B. für Log-Dateien verwendbar

## Proxy-Muster
> d.h. Steuerung eines Objektes wird auf ein vorgelagertes Objekt verschoben

<span style="color:red;font-weight:bold">Nicht zu verwechseln mit Web-Proxy!</span>  

![[media/pi/modules/Systementwicklung/Proxy_Muster_1.drawio.svg]] 
![[media/pi/modules/Systementwicklung/Proxy_Muster_2.drawio.svg]]  
![[media/pi/modules/Systementwicklung/Proxy_Muster_3.drawio.svg]]
- Es können Anfragen manipuliert werden

## Wrapper (Adapter)
> übersetzt eine Schnittstelle in eine andere Schnittstelle

![[media/pi/modules/Systementwicklung/Wrapper.drawio.svg]]

## Interpreter-Muster
> definiert die Repräsentation einer Sprache (Grammatik) und ermöglicht die Sätze der Sprache zu interpretieren

Bsp: $(7+3)+(2 * 6)$  
![[media/pi/modules/Systementwicklung/Interpreter-Muster.drawio.svg]]

### Umgekehrte polnische Notation
++ 7 3 * 2 6  
--> ++ 7 3 * 12  
--> +10 12  
--> 22  

![[media/pi/modules/Systementwicklung/umgekehrte_polnische_Notation.drawio.svg]]
```c++
class TermAusdruck {
	return 5; // 5 hierbei als Beispiel
}

class NichtTermAusdruck {
	Ausdruck a;
	Ausdruck b;

	return interpretiere(
		a.interpretiere(+), 
		b.interpretiere(*)
	);
}
```

## Iterator
> Es kann auf Bestandteile eines aggregierten Objektes zugegriffen werden, **ohne** die interne Repäsentation zu kennen.

![[media/pi/modules/Systementwicklung/Iterator.drawio.svg]]

```C++
List l;
List Iterator it;

for(it=l.begin(); it <> l.end(); it=it.next()) {
//...
// do something
//...
}
```
![[media/pi/modules/Systementwicklung/Iterator_2.svg]]
### Vorteile
- einheitliche Schnittstelle zum Traversieren (=> Übersichtlichkeit)
- kann mit mehreren Iteratoren zugreifen,
	- um auf unterschiedliche Art und Weise durch die Datenstruktur gehen zu können
- innere Struktur muss nicht bekannt sein

### Nachteile
- Ein Programmierer achtet ggf. nicht auf die Komplexität beim Zugriff auf Datenstruktur