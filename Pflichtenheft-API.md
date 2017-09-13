# Pflichtenheft         
    
## Projektbeschreibung     
**Musskriterien:**    
* Das Programm muss eine CSV-Datei öffnen und eine CSV-Datei erstellen bzw. falls schon vorhanden überschreiben können
* Es müssen Daten aus einer CSV-Datei eingelesen werden können.   
* Das Programm muss mit den Regelparametern und vorgegebenen Zeitabschnitten die resultierenden Winkelwerte berechnen
* Ein- und Ausgaben der CSV-Dateien richten sich stets nach der in Deutschland üblichen Dezimalschreibweise von Gleitkommazahlen mit einem Komma als Trennzeichen


**Wunschkriterien:**  
* Der Nutzer soll den Dateinamen der Ausgabedatei selbstständig wählen können.   
* Die Ergebnisse der vorherigen Rechnungen sollen mit dem aktuellen Ergebnis verglichen werden.  
* Der Anwender soll die Regelparameter und die Zeitrechenschritte selbst bestimmen können.   
* Daten sollen nacheinander eingelesen werden, um einer Simulation nahe zukommen (while-Schleife).
* Am Ende soll berechnet werden, ob eine Verbesserung des Fahrverhaltens vorliegt

**Abgrenzungskriterien**    
* Eine Überprüfung von den Eingaben des Anwenders (Name, Uhrzeit, Datum, Beschreibung) ist nicht notwendig, da eine Fehleingabe des Anwenders keine Auswirkungen auf das Testergebnis hat.
* Die CSV Datei wird im Anschluss an den Programmablauf nicht automatisch geöffnet
* Um den Programmablauf zu beschleunigen wird auf detaillierte Erklärungen beim Programmablauf verzichtet. Es wird stattdessen ein Handbuch zum Programm erstellt. Der spätere Anwender muss in das Programm angewiesen werden und kann anschließend schneller Auswertungen fahren, als es der Fall wäre, wenn wir das Programm mit Erklärungen überladen würden

**Produkteinsatz**   
Der Anwendungsbereich befindet sich im Maschinenbau und speziell im Zugbau.
Das Programm richtet sich an Ingenieure, um sie bei der Beurteilung ihrer konstruierten Neigevorrichtung eines Zuges zu unterstützen und erste Entscheidungen zu treffen.  Es soll zu jeder Uhrzeit benutzbar sein und manuell gestartet werden.
Das Programm hat nicht das Ziel detaillierte Ergebnisse zurückzugeben sondern nur eine erste Beurteilung der Konstruktion zu ermöglichen.   


## Funktionsbeschreibungen    
     
### Funktionsbeschreibung Marvin Frede    
   
|  **Funktionsbeschreibung** 	|   **Beschreibung**	|
| ---                           |---                    |
| **Funktionsname:**	|  einlesen()               	|
| **Kategorie:**  	|  primär 	                |
| **Nachbedingung Erfolg:**  	| Wenn die eingelesenen Daten korrekt verarbeitet wurden, stehen zwei Variablen mit den, benötigten Zahlenwerten zur Verfügung und können von weiteren Anwendungen genutzt werden.  	|
| **Nachbedingung Fehlschlag:**  	| Sollte die Funktion nicht korrekt ausgeführt werden, können verschiedene, Probleme auftreten. Es können keine Daten abgespeichert werden und es kommt zu Speicher- und verarbeitungsfehlern. Damit kann der Rest des Programmes nicht mehr ausgeführt werden  	|
| **Akteure:**  	| Der Nutzer hat keinen direkten Zugriff auf die Funktion. Der Nutzer kann allerdings indirekt die erfolgreiche oder nicht erfolgreiche Bearbeitung der Funktion beeinflussen (falsche Datenformatierung).  	|
| **Auslösendes Ereignis:**  	|  Beim Start des Programms wird die Funktion automatisch ausgeführt. 	|
| **Beschreibung:**  	|In der Funktion werden die eingelesen Zeilen, die in einem String „zeile“ stehen, aufgespalten. Dies ist notwendig da in dem String zwei Zahlen stehen die separat für eine Berechnung benötigt werden. Um dies, zuerreichen wird der String als erstes an eine weitere Funktion übergeben (trennzeichenAendern). In dieser Funktion wird die Zeichenfolge in „zeile“ umformatiert. In dem String „zeile“ steht nun die selben Daten, nur mit der überarbeiteten Formatierung. Nun wird der überarbeitet String an einen Stringstream übergeben, der durch die neue Formatierung die beiden separaten Zahlen in dem string erkennt und diese in jeweils eine eigene Variablen vom Datentyp float speichert.     |
| **Erweiterung:**      |  Die Funktion kann überarbeitet werden, sodass mehr als nur zwei Zahlen in dem String stehen dürfen und somit Textdateien mit mehr Zahlen pro Zeile verarbeitet werden können. |    
   
### Ablaufdiagramm Marvin Frede     
     
![Ablaufdiagramm Marvin Frede](images/ablaufdiagrammMarvin.jpg)      
    
          
### Funktionsbeschreibung Florian Zaschka      
   
    
   
| **Funktionsbeschreibung**     |   **Beschreibung** |
| ---                           |---                 |
| **Funktionsname:**      |floatzustring ()|
| **Kategorie:**  	        | primär |
| **Nachbedingung Erfolg:**  	| Es stehen die der Funktion überreichten Floats als Stings zur verfügung. Als Trennzeichen der Gleitkommazahlen wurde ein Komma gesetzt |
| **Nachbedingung Fehlschlag:** | Der Anwender öffnet die CSV Datei und das Programm versucht mit den Werten mit Punkt als Trennzeichen ein Datum o.Ä. in die Eingabe zu interpretieren. Die Ergebnisdatei ist somit nicht verwertbar |
| **Akteure:**  	        | Der Nutzer erkennt eine falsche Funktionsweise in der Ergebnisdatei |
| **Auslösendes Ereignis:**  	| Automatisch. Keine Beeinflussung nach Programmstart möglich |
| **Beschreibung:**  	        | die Funktion bekommt als Argument eine Float Zahl überreicht. Diese wird in einen String umgewandelt. In diesem schaut die Funktion anschließend, ob ein Punkt als Trennzeichen vorkommt. Falls ja, so wandelt die Funkion den Punkt in ein Komma um |
| **Erweiterung:**              | Die Strings werden auf eine bestimmte Länge beschränkt, um unnötig viele Nachkommastellen zu vermeiden |     

![](images/UML_Nutzerinfos.PNG)
     
        
### Funktionsbeschreibung Florian Siebert     
     
| **Funktionsbeschreibung**     |   **Beschreibung** |
| ---                           |---                 |
| **Funktionsname:**       	| berechne() |
| **Kategorie:**  	        | primär |
| **Nachbedingung Erfolg:**  	| Die Variablen t, winkeldif, moment und wagenlot wurden auf die akutellen, entsprechend der Eingangswerte korrekten Werte gesetzt. |
| **Nachbedingung Fehlschlag:** | Mindestens eine der Variablen t, winkeldif, moment oder wagenlot wurde nicht auf den aktuellen, entsprechend der Eingangswerte korrekten Wert gesetzt |
| **Akteure:**  	        | Hauptprogramm  |
| **Auslösendes Ereignis:**  	| Aufruf in der main()-Funktion |
| **Beschreibung:**  	        | Die Funktion berechnet zunächst das aktuelle Zeitinkrement aus der Differenz von aktuellem Zeitpunkt und vorherigem Zeitpunkt, sowie die aktuelle Winkeldifferenz zwischen dem Scheinlot und der Wagenhochachse. Anschließend wird die Winkelbeschleunigung der Wagenhochachse berechnet. Dazu wird die aktuelle Winkeldifferenz mit dem Faktor p beaufschlagt und die Differenz aus aktueller Winkeldifferenz und vorheriger Winkeldifferenz mit dem Faktor d. Zuletzt ergibt sich der neue Winkel der Wagenhochachse (relativ zum Lot des Erdbodens) durch integrieren der Winkelbeschleunigung. Diese ist konstant, also gilt folgende Formel: ![Formel](images/Formel.png)|
| **Erweiterung:**              | keine | 

![Ablaufdiagramm](images/PAP.jpg)