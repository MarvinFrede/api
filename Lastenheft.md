**A01:** Einlesen einer CSV-Datei  
* Es soll eine Datei mit Werten eingelesen werden können.     
* Die Datei enthält diskrete Werte für die Winkel des Scheinlots abhängig von der Zeit.    
* Die Datei enthält die Zeitabstände der Messungen.    
* Es müssen zwei Spalten eingelesen werden können.   
_(Marvin Frede)_

**A02:** Der Nutzer soll die Regelparameter eingeben. Die Regelparameter sind die zwei Proportionalfaktoren des Reglers.  _(Florian Siebert)_

**A03:** Die Regelstrecke soll simuliert werden. Sie weist folgendes Verhalten auf:

* Der Regler regelt proportional zum Winkel zwischen Scheinlot und Wagenhochachse und proportional zur zeitlichen Änderung dieses Winkels.
* Die Strecke wirkt integrierend. Je größer die Stellgröße und je länger sie wirkt, desto größer die Winkeländerung des Fahrzeuges (siehe dazu die [Allgemeine Systembeschreibung](https://github.com/TUBSAPISS2017/projektarbeit-wir-mogen-zuge/wiki/Allgemeine-Sytembeschreibung))
_(Florian Siebert)_

**A04:** Das Ergebnis der Berechnung für einen Zeitpunkt soll in einer Datei gespeichert werden. Es sollen die Werte des aktuellen Scheinlots, des aktuellen Wagenlots und der aktuellen Winkeldifferenz mit Angabe des Zeitpunktes Zeilenweise in eine Excel-Datei oder ähnliches geschrieben werden. Die Ausgabedatei ist entweder schon vorhanden oder wird neu im Programmordner erstellt. Falls sie schon vorhanden ist soll die bisher bestehende Datei überschrieben werden.   _(Florian Zaschka)_

**A05:** Der Nutzer gibt die Nutzerdaten  Name des Nutzers, Zeit und Datum der Simulation, Bezeichnung der Simulation ein. Die Daten werden in die Kopfzeile der Ergebnis-Datei geschrieben. Bei den Vornamen ist darauf zu achten, dass Doppelnamen vorkommen können. Sollten noch weitere Eingaben zu einem späteren Zeitpunkt verlangt werden, dann sollte diese Funktion erweiterbar sein _(Florian Zaschka)_ 

**A06:** Analyse des Fahrkomforts   
*  Am Ende soll das Programm ausgeben, um wie viel ruhiger die Fahrt geworden ist.    
* Dabei gilt folgendes Schema:     
1. Das Zeitinkrement (t[i+1]-t[i]) multipliziert mit der Schräglage hoch einem Exponentialfaktor ergibt eine Referenz für das Wohlbefinden des Fahrgastes.    
2. Die Gesamtreferenz ergibt sich durch summieren aller Einzelreferenzen der Zeitschritte.    
3. Das Programm schafft es zum einen die Gesamtreferenz für eine Fahrt ohne aktives Neigesystem (Schräglage = Scheinlot) und die Gesamtreferenz mit aktivem Neigesystem (Schräglage = Scheinlot - Wagenlot) zu erstellen.    
4.  Aus diesen beiden Werten gibt das Programm aus um wie viel die Fahrt ruhiger geworden ist -->  Um wie viel Prozent die Referenz mit aktivem Neigesystem also kleiner ist als die ohne aktives Neigesystem.    
_(Marvin Frede)_






