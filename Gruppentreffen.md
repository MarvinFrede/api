### 1. Gruppentreffen
**Datum und Uhrzeit:** 10.4.17 von 18:00 bis 19:00   
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Brainstorm über verschiedene Projektideen
* Die Ideen "Wetterstation" (Florian Zaschka), "Bewässerungssystem" (Marvin Frede) und "Neigesystem" (Florian Siebert) sollen ausgearbeitet und im nächsten Treffen präsentiert werden. Dann soll eine endgültige Entscheidung gefällt werden.

### 2. Gruppentreffen  
 
**Datum und Uhrzeit:** 15.4.17 von 9:00 bis 12:00   
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Projektvorschläge und Wahl eines Projektes
* Meilenstein "Idee" somit pünktlich erreicht
* Nutzen und Ziele des Projektes
* Anforderungen definieren sowie verteilen
* Festlegen der zu nutzenden Programme   
    
### 3. Gruppentreffen

**Datum und Uhrzeit:** 18.4.17 von 13:00 - 15:00   
**Anwesenheit:** Marvin Frede, Florian Zaschka, Florian Siebert   
**Inhalt:**   
* Anforderungen überarbeiten da Unklarheiten vorhanden sind
* Daraus folgte teilweise Neudefinition des Projektes
* neu Aufteilung der Anforderungen
* Einarbeitung in GitHub
* Problemstellung identifizieren und festhalten (Blockschaltbild)
* Zeitplan Erstellung angefangen
     
### 4. Gruppentreffen   

**Datum und Uhrzeit:** 25.4.17 von 13:00 – 15:00   
**Anwesenheit:** Marvin Frede, Florian Zaschka, Florian Siebert   
**Inhalt:**   
* Zusammenführen der Anforderungen in GitHub
* Einteilung der 3 Zyklen des Spiralmodells
* Verbesserung des 1. Zyklus des Spiralmodells
* Zeitplan fertiggestellt, Meilenstein ein paar Tage zu spät erreicht wegen Wochenende
* Use-Case-Diagramm angefangen, Zeitplan in Verzug aufgrund der zeitaufwendigen Einarbeitung in Git      
     

### 5. Gruppentreffen

**Datum und Uhrzeit:** 1.5.17 von 13:00 – 15:00   
**Anwesenheit:** Marvin Frede, Florian Zaschka, Florian Siebert   
**Inhalt:**   

* Use-Case-Diagramm zusammengeführt, allerdings noch nicht komplett fertig
* Korrekturen an den Anforderungen, Lastenheft damit fertiggestellt, Meilenstein pünktlich erreicht.
* Das Pflichtenheft wird ab jetzt ausgearbeitet, jeder informiert sich, wie die Anforderungen umzusetzen sind.     
     
### 6. Gruppentreffen  
 
**Datum und Uhrzeit:** 09.5.17 von 14:00 bis 14:45  
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Es wurde mit der Erstellung des Codes begonnen. Insbesondere wurde die Anforderung, dass eine Excel-Datei eingelesen werden kann, bereits von Marvin realisiert. Zwar funktioniert das Einlesen nur mit einer .csv Datei aber dafür sind wir flexibel in der Anzahl der Zeilen, die das Programm abarbeiten soll.

* Die Anforderung, dass für unser Programm eine Benutzeroberfläche existieren muss, wird verworfen, da nach momentanem Stand das Programm nur gestarten werden muss. Im Gegenzug dazu wurde Anforderung A06 definiert.

* Es wurde beschlossen, dass der Wert der Zeit aus der .csv Datei dem Namen "Zeitpunkt" im Quellcode zugeordnet werden soll. Der Wert des Scheinlots wird "Scheinlot" genannt.

* Das nächste Treffen wird am nächsten Dienstag nach der API Übung statt finden, damit wir Zeit für ein längeres Treffen haben, da noch viele Punkte zur Aussprache ausstehen

* Da sich die Anforderungen noch ändern und die eigentliche Definition des Projektes sich erst nach und nach ergibt, kann der Meilenstein Pflichtenheft nicht erreicht werden. Aber alle Beteiligten arbeiten an ihren Anforderungen und probieren verschiedene Umsetzungen aus. 
     
### 7. Gruppentreffen  
 
**Datum und Uhrzeit:** 16.05.2017 von 18:30 bis 19:30  
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Der Branch "Daten einlesen" wird mit dem Branch "Master" gemerged
* Marvin stellt die aktuelle Lösung für das Einlesen der Daten vor. 
* Unstimmigkeiten bezüglich der Anforderungen wurden beseitigt. 
* Mittlerweile sind alle mit Git und der C++ Programmierung gut vertraut. Entsprechend des Zeitplans soll begonnen werden, die anderen Anforderungen zu erfüllen. 
* Der Meilenstein Pflichtenheft steht noch aus, da erst in dieser Woche alle Anforderungen voll definiert werden konnten.
      
### 8. Gruppentreffen  
 
**Datum und Uhrzeit:** 31.5.17 von 18:30 bis 20:00  
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Es wurde nochmals darauf Eingegangen, dass wir bei unserem Regelkreis keine Störgrößen berücksichtigen. Die Annahme ist eine Aufhängung des Wagons im Schwerpunkt und ein reibunsfreies Verfahren des Wagons.
* Die Regelung stellt sich als recht komplex heraus, da für den Differentialregler das System nicht nur die Werte der letzten Schleife benötigt, sondern auch die Werte davor (Änderung der Regelungsabweichung). Dies müssen Florian Siebert und Florian Zaschka bei der weiteren Programmierung berücksichtigen.
* Florian Siebert hat für seine Arbeiten einen Branch erstellt und mit dem Programmieren begonnen
* Marvin hat im Zuge eines Reviews beim Einlesen der Datei die Lines of Code (LoC) reduziert

      
### 9. Gruppentreffen     

**Datum und Uhrzeit:** 13.6.17 von 17:30 bis 20:00 Uhr
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede   
**Inhalt:**   

* Florian Siebert konnte den Teilcode für seine beiden Anforderungen vorläufig fertigstellen. Der Regler regelt proportional zur Abweichung und zur Änderung der Abweichung, außerdem können Regelparameter aufgenommen werden. Es muss noch eine automatische Erfassung des Zeitinkrements implementiert werden.
* Marvin hat seinen Code überarbeitet und in Funktionen ausgelagert. Allerdings sind die eingelesenen Daten nicht global verfügbar. Hier ist eine Absprache mit Florian Siebert nötig, wo und wie die eingelesenen Daten für die Rechnung zur Verfügung stehen sollen. Dazu gibt es am 15.06. ein Treffen zwischen den beiden. Der Meilenstein Pflichtenheft kann damit noch nicht erreicht werden. Ansonsten wird der Zeitplan erfüllt.
* Da der zweite Zyklus vor der Fertigstellung steht, wird Florian Siebert den dritten Zyklus nun ausformulieren.
   
     
### 10. Gruppentreffen    

**Datum und Uhrzeit:** 19.6.17 von 17:30 bis 18:30 Uhr 
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede 
**Inhalt:**

* Marvin und Florian S. haben in der vergangenen Woche eine Absprache getroffen, wie die eingelesenen Daten in der main-function verfügbar sein sollen, was nun möglich ist. 
* Florian Z. plant, die berechneten Werte in einem Feld zu speichern. Der Speicherplatz muss dynamisch angefordert werden, wofür vor der Berechnung feststehen muss, wie groß das Feld sein muss, d.h. wie viele Berechnungsschritte es gibt. Es ist fraglich, ob dies im Sinne einer Echtzeitsimulation ist und ob dies von uns überhaupt gewollt ist, da unser Programm ohnehin auschließlich darauf ausgelegt ist, fertige Sensordaten als Datei einzuspeichern. Dennoch soll geprüft werden, ob die Ergebnisse statt im RAM gespeichert zu werden, direkt in die Ausgabedatei geschrieben werden kann, sodass diese bei jeder Berechnung um eine Zeile ergänzt wird. 
* Florian Z. stellt außerdem sein Bewertungsschema vor, das bewerten soll ob und wie sehr die gewählte Regelung den Fahrgastkomfort verbessert. Die anderen stimmen seinem Vorschlag zu. 
* Somit kann der Meilenstein Pflichtenheft nun erreicht werden. Abgesehen davon wird der Zeitplan eingehalten.

### 11. Gruppentreffen
**Datum und Uhrzeit:** 27.6.17 von 18:15 bis 19:00 Uhr 
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede 
**Inhalt:**

* Der Code ist fertiggestellt und lauffähig. 
* Die Testfunktionen werden in der kommenden Woche in die main.cpp implementiert. Der erfolgreiche Test wird per Screenshot im Wiki festgehalten. Anschließend werden die Testfunktionen in der main.cpp auskommentiert. Sie können somit bei Bedarf jederzeit wieder zugeschalten werden.
* Marvin passt die Protokolle im Wiki an. Alle Protokolle sollen auf einer Seite zu finden sein.
* Florian Z. überarbeitet die Einleitungsseiten unseres Wikis
* Das Layout und die übergeordneten Punkte des Pflichtenhefts erstellt Marvin. Jeder erarbeitet anschließend eine Funktionsbeschreibung und eine Funktionsspezifikation
* Florian S. und Florian Z. müssen ihr externes Review noch durchführen
* Florian Z. wird beginnen ein Handbuch zu unserem Programm aufzusetzen

### 12. Gruppentreffen
**Datum und Uhrzeit:** 4.7.17 von 18:15 bis 19:30 Uhr 
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede 
**Inhalt:**

* Alle Testfunktionen wurden implementiert und erfolgreich ausgeführt, die Tests wurden dokumentiert.
* Der Code ist damit fertiggestellt, der Meilenstein Programmfertigstellung wurde also mit vier Tagen Verzug erreicht. Grund für die Verzögerung ist die längere Abwesenheit von Florian Siebert aufgrund einer Konzertreise der Braunschweiger Domsingschule.
* Statt des Handbuches von Florian Z. wird Marvin die Readme erweitern. 
* Florian Z. erstellt eine Präsentation mit den Ergebnissen des Projektes.
* Florian S. überarbeitet das Wiki an schwachen Stellen. Insgesamt soll das Projekt am nächsten Dienstag fertiggestellt sein.

### 13. Gruppentreffen
**Datum und Uhrzeit:** 13.7.17 von 19:30 bis 20:30 Uhr 
**Anwesenheit:** Florian Zaschka, Florian Siebert, Marvin Frede 
**Inhalt:**

* Die Readme und die Präsentation wurden erstellt.
* Das Wiki ist vollständig, es wird ein letztes Protokoll geschrieben, der letzt Meilenstein wird dokumentiert und der 3. Zyklus des Vorgehensmodell gereviewt.

Das gesamte Projekt wird reflektiert:

* Es hat sehr lange gedauert, unsere Problemstellung zu definieren. Gründe dafür sind unsere mangelnde Erfahrung mit der Programmierung und die geringen Kenntnisse über das Themengebiet des Projektes. Es mussten im Laufe der Bearbeitung die Anforderungen geändert werden, sodass sich das Ziel unseres Projektes mit der Zeit noch verschoben hat. 
* Es gab einige Verständnisprobleme mit den geforderten Dokumentationen, zum Beispiel haben wir zunächst ein Use-Case-Diagramm erstellt, das eigentlich keines war. Insbesondere aber das Use-Case-Diagramm hilft aber bei der Definition des Problems. 
* Unser Projekt nahm dann richtig Fahrt auf, als wir anfingen schriftlich und namentlich festzuhalten, was in der nächsten Woche zu tun ist und wer dafür verantwortlich ist. 
* Die drei Mitglieder der Gruppe sind sehr unterschiedlich in ihren Fähigkeiten und Stärken, was im Projekt genutzt werden konnte, indem die Aufgaben und Anforderungen entsprechend der Stärken verteilt wurden. Insgesamt konnten sich alle Mitglieder aufeinander verlassen und jeder hat sich gegenüber den anderen verantwortlich gefühlt, sodass Aufgaben immer zum vereinbarten Zeitpunkt erledigt wurden und auch dadurch Verzögerungen vermieden wurden. 
* Die gemeinsame Arbeit wurden auf ein Minimum reduziert, damit jeder eigenverantwortlich und effizient Aufgaben erledigen konnte und Konflikte vermieden wurden. Es gab wenig Diskussionen darüber, wie eine Anforderung zu erfüllen ist, da sich jeder auf die Arbeit des anderen verlassen konnte. Wir hatten viel Vertrauen ineinander, dass die Ergebnisse nach bestem Wissen und Gewissen erstellt wurden. 

