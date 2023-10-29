--> Zerlegung in eigenständige Funktionalitäten ohne Aussage über physische Verteilung


## Blockdiagramme
![[media/pi/modules/Systementwicklung/Block-Diagramme.drawio.svg]]

![](https://www.plantuml.com/plantuml/png/NO_1geCm44NtynKNbmy4uUsB9lqBwsAmKvN6ACbqKKh_lP66jiWm3EVUivawAWUzpOvYpqxmNrL_QIbU9xzou1bkygBtLR047HUY8Bso7v9xn8E0BnSdtQPvdm8SqUm5amkpBsmkB17QfaDP7j2QxWVi1YP1c8PHFubDYPEBPlz9L8i_fuzU)

![](https://planttext.com/api/plantuml/png/RL8nRiCm3Dpr2bQxXtWkYWnTCXWDuW9UkgWsOmcrQODYKXI5VzDdTCl7gifkdJY1008y7e_aGMilXkNGDig_EUeDcnOQHoWVFKB7OZkbxYhS1mXyRqhqy2BBfnHZAORg1c6xILVmgG1cA4FofKMAy7b1JufRxlReVSVJ20rc12DVkXh58a_j5mBjwOkeSK4TSZbKI88KkxFycloExlKMjxZ1hTmHsI-PZoDpY366toqXIHx-1lxdnIAVMcF8ShXFsDLMPc9nZatax0Qcnl4N1c_e67OqV6Nmiml6BqtFvVHj6um7fVcYkiFI4lAyQvG0dUfmnHFebHvx1ZKefTP8LVWxFm00)


## Komponenten-Diagramm 
![[media/pi/modules/Systementwicklung/Komponentendiagramm.drawio.svg]]

![](https://www.plantuml.com/plantuml/png/nP11QiCm44NtSuff32KjDOYMRjfDBFiMJGd2ciGYziX8Oq9lNn6CwxPedTNZw_qFWtPHJ91fw26sfYTyLGelpae7yUnuDC4Cs3ic-He9VP3E0znPEgOdZADfAU9zeTJBy_kDy7EE1DUU3yU9ma47Sh8S-0i0hHz6pyI2csPnUMpGH6pMgohVgzOzFPizx_bgzThMVsqDqA0lIwmI7nFrp2GgB4hhBwmUoWBr4hSgnHfqYX_5AH3napMn8_iPtAcJQxl6j_zVavriLNO2Es8x3Vqt)

## Architektur-Muster für die strukturelle Sicht
- Kette
- Repository
- Schichten
- Interpreter

### Kette
![](https://www.planttext.com/api/plantuml/png/RT0n3i8m38NXtQUmkXUfoOwwiESAXfea8asgn0pS7a837Thjbpxh3HwBK9Rd723mNL0IPc-TuEGptyId2ENXuqAPPWm-ihmMnfJ59O1wGT46niuuAen3XrJG37jHfsRg45L3TOIweTvZ8mrW1kpxytV_dsfB3HzPkwRQKlyIp9gNRFaQVG4OEKxrCsy0)

Beispiele:
1. Ablauf in der Mensa: (Reingehen, Essen wählen, Bezahlen)
2. Abfolge von Transformationen von Eingabe-Daten
	- z.B. Website --> JSON --> DB
	- Linux-Pipes  
![[media/pi/modules/Systementwicklung/Linux-Pipes.drawio.svg]]

### Repository
- lat. *Repositorium:* Lager, Depot
- digitales Archiv
- häufig inklusive Funktionen zur Versionsverwaltung
- Daten sind passiv
- <b><ins>Vorteil</ins></b>: Klienten sind unabhängig
	- können unabhängig voneinander geändert werden

![](https://www.planttext.com/api/plantuml/png/TP4_Ry903CLtVmh3pa2oLeYz6mD8WGu7vrnE9EV8vr1Hn7Vd0cbL_idR-zdFp_8ygX7jcXgKMrJ6BQjoWzOBxTHpWBZteJLY6gnzeAZ7cf15AmOOMIgJXh4rEuguqLizwDaVI2YjSQGL2Pu0iTzXWakEunN9_eSwXzCnceYhp-aRdWqyUyFpWUTm1lZNC8GiEYU-BEE1vDlKsWKtnBoE5SldaGmNr7BqodByFUdQl018CV5ZigwyjHI-9hFU84LxeULFMh6ybv8Tm9o2xRzn0G00)

### Schichten-Muster
Jede Schicht bietet einen Dienst nach oben und nutzt Dienst von unten  
![](https://www.planttext.com/api/plantuml/png/RT0n3iCW30NGtQTmisS8oLXLkGDh5nTeWWeu0cV8xKk4rA6Al7pz9_t1Sn7AiiS0jotJ4Wa37RmBbkY44e7mXiBuOX6EQ7rsHZmdA1-VDieKCVZaYXp18MTP6U1ctRjsM3Oohk1JsltrwWULu9objDIHJflLcrLmwf0AwkdAncRZbQbcwig6PWE0dkwzxHzrGeyjAT2gfSgpI_RyoXS0)

#### 3-Schichten-Architektur
![](https://www.planttext.com/api/plantuml/png/RP2x3eCm34LtVuLXPs6kAWOM95QsBYunD8B4A343Vz-0QAK-9jl7ntTm5PM2hcw6R0aqEiAPDbaLesCbJw2oe0hUHLKS6XkuLoiUucJzGe4SpjPpr6rcbA0F0SWC3ubXNAZdY3Vz8cL22S8UHNvCX_cfTf53qNZbCAJvr7Eaj6b-zH9R6UtqIZsyzfzMaxB_q6g0hhaKfhYsq1ur4O2AlTb_yMwU)
![](https://www.planttext.com/api/plantuml/png/RP0n3i8m301tlyAmT-cC40DBfKv8R2o6cX8riQF47VeVViB7I14W14oEJfUpv4qsIZO63ukOg0-4dYOT3NDW8o4mZMYAHpNJW9rBV3Ad0dbm4YbHGE-4iqsUKPDT563HyRamp95EdF5WNwGkg42OKoHz-RXygZkEwNRDB4RpagU_HCguRtxz6bljtV3AFhpsJtPBnd8XRwFqdyqjmBvPLLsrRg5zp480DYpTV97tumu0)

<ins><b>Vorteile:</b></ins>
- separate Änderung möglich
- übersichtlicher Quellcode
- fein granularer erweiterbar

### Interpreter-Muster
- z.B. Python, (Java), PHP, bash, BAT
- ist vergleichbar mit dem Factory-Muster

#### Muster:  
![[media/pi/modules/Systementwicklung/Interpreter.drawio.svg]]

#### Vorteil:
- plattformunabhängig (brauche nur Interpreter)

## Vorteile von Mustern
- Zeitersparnis / generische Lösung für häufige Probleme
- größere Übersichtlichkeit bei Standard-Mustern
- Wiederverwendbarkeit
- Vereinheitlichung
- Unterstützung nicht funktionaler Anforderungen
- Dokumentation
- Kommunikation
- Dinge sichtbar machen

