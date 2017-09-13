## Pflichtenheft   

**Aufgabe 01: (Marvin Frede)**   
Erstellen eines Quellcodes der es ermöglicht Daten aus einer Excel Datei an eine Rechnung im Programm weiterzugeben.   
   
**Umsetzung:**   
* Programmiersprache wird C++ und C sein.   
* Es wird nicht direkt aus einer Excel-Datei eingelesen werden.
* Daten werden aus einer CSV Datei (Textdatei) eingelesen.   
* Daten werden nicht in ein Array eingelsen.   
* Zahlen werden als float Datentyp abgespeichert.   
* Die Datei wird zeilenweise mit einer while-Schleife eingelesen.   

**Aufgabe**
* Speichern von verschiedenen Winkelwerten

**Umsetzung**
* zunächst schaut sich das Programm an, wie viele Zeilen die einzulesende Datei insgesamt hat. Anschließend wird für jeden einzulesenden Winkel ein Feldzeiger mit der Dimension der Zeilenanzahl erstellt. Die Zeilen, die im Hauptprogramm nicht eingelesen werden dienen im jeweiligen Feld als Puffer.

**Aufgabe**
* Abfrage von Nutzerdaten

**Umsetzung**
* Es wird eine Klasse mit den Nutzerdaten erstellt. Diese werden als strings zwischengespeichert. Beim beschreiben der .csv Datei werden Sie dann wieder mit ausgegeben und in einzelne Zellen geschrieben.

**Aufgabe**
* Schreiben in eine Excel-Liste

**Umsetzung**
* Es wird eine Excel-Liste erstellt. Sollte bereits eine Datei mit deren Namen existieren, so wird diese beim öffnen zunächst geleert. Anschließend wird eine einheitliche Überschrift in der ersten Zeile stehen. In der nächsten Zeile werden die Nutzerdaten eingeschrieben. Anschließend kommen die Spaltenüberschriften für die Winkel und Zeitpunkte und zuletzt in den jeweiligen Spalten die Winkel.    
     
**Aufgabe 06: (Marvin Frede)**
* Erstellen einer kleinen Analyse, ob das Neigesystem den Fahrkomfort verbessert oder verschlechter hat.   

**Umsetzung**    
* Es werden zwei Variablen benötigt, in denen eine Referenz in Form eines Zahlenwertes gespeichert werden.    
* Bei jedem Schleifeindurchlauf wird die alte Referenz um den neuen Wert erhöht mittels einer Addition.    
* Für die Bewertung wird eine Funktion erstellt, die als Parameter die beiden Gesamtreferenz übergeben bekommt.    
* In der Funktion wird ein prozentualer Wert ermittelt der angibt um wie viel sich die Fahrt verbessert hat und gibt aus ob sich die Fahrt verbessert oder verschlechtert hat.  

  
