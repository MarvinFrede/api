## Review Marvin Frede  
   
**Name Reviewer:** Marvin Frede   
**Name Entwickler:** Marvin Frede  
**Dateiname:** einlesen.cpp    
 **git-Revision:** b926f2961918573f8b628570169237b5af10be29  
**Funktionalität:**    
Öffnen der Datei,   
Überspringen einer bestimmten Anzahl an Zeilen,    
Änderung der Trennzeichen korrekt durchgeführt,    
Wurde der string korrekt aufgeteilt und in den Variablen gespeichert,   
Funktioniert die Testrechnung,    

**Ergebnis:**   
Der Code funktioniert wie erwartet. Die Daten die in der CSV-Datei stehen, werden korrekt eingelesen und ausgegeben. Durch die Bildschirmausgabe lässt sich dieser Umstand gut kontrollieren. Auch eine Beispielrechnung führt zu dem gewünschten Ergebnis.  
Dadurch ergibt sich, dass die Trennzeichen erfolgreich zu einem Leerzeichen geädert worden sind. Genauso wurden die Zahlen die zuvor in einem String standen, durch die Stringstreamfunktion erfolgreich in zwei Variablen gespeichert. Da es keine Fehlermeldung gibt, wurde die Datei korrekt geöffnet und gelesen.  
Wünschenswert wäre eine bessere Kommentierung, da einige Kommentare nicht zum Verständnis beitragen, da sie Teile aus dem Quellcode beschreiben, welche schon selbsterklärend sind.    
Des Weiteren wären Funktionen hilfreich, da sie Quellcode aus der main Funktion entfernen, den Quellcode einfacher kontrollieren lassen, man einzelne Funktionen einfacher auf ihre Aufgaben testen kann sowie es der Objektorientiertheit von C++ entsprechen würde. Wünschenswert wäre außerdem eine Headerdatei und weitere .cpp Datei in denen die Funktionen ausgelagert werden.   
Außerdem wäre es sinnvoll, den Block in dem die Trennzeichen geändert werden zu verkleinern beziehungsweise Funktionen zu suchen die diese Aufgabe der Änderung übernehmen.
Ebenso wäre es eine Überlegung wert, die Daten in ein Array zu speichern, damit man nicht die ganzen Rechnungen in der while-Schleife durchführen muss, sowie flexibler auf Wert aus der Datei zugreifen kann, da sie momentan nur bei einem Schleifen Durchlauf vorhanden sind.    
Dafür wurden die Konventionen für Variablennamen in C++ korrekt umgesetzt und sind eindeutig.    
     
## Review Florian Zaschka
   
**Name Reviewer:** Florian Zaschka  
**Name Entwickler:** Florian Zaschka    
**Dateiname:** speichern2.cpp   
 **git-Revision:** 43ff4fc13e4b5bcc22b36d4f87106adcbc69fdc7 

**Funktionalität:**    
Der Quellcode hat die Aufgaben Daten in eine CSV Datei zu schreiben und Daten beim Programmablauf vom Anwender abzufragen. Dazu überprüft der Code zunächst wie viele Zeilen die Ausgabe maximal haben muss. Mit dieser Anzahl der Zeilen wird ein Speicher dynamisch angefordert, in dem dann die Daten für die Datei gesammelt werden. Diese Vorgehensweise funktioniert zwar aber man kann sich hier durch ein direktes beschreiben der CSV Datei sobald die Daten im Programmablauf zur Verfügung gestellt werden den Zwischenschritt mit dem Speichern in einem Feld sparen. Dies spart vor allem wenn viele Zeilen eingelesen werden enorm viel Speicherplatz und vereinfacht die Funktionsweise des Codes.

**Ergebnis:**   
Zu Beginn der Main-Funktion wird bereits die Ergebnisdatei erstellt. Diese wird dann während dem kompletten Programmdurchlauf offen gelassen, damit sie immer direkt dann beschrieben werden kann, wenn die entsprechenden Werte bei der Berechnung zur Verfügung stehen. Dadurch sparen wir uns das Zwischenspeichern aller Daten und der Programmcode wird einfacher und intuitiver.

## Review Florian Siebert 
   
**Name Reviewer:** Florian Siebert   
**Name Entwickler:** Florian Siebert  
**Dateiname:** Strecke.cpp    
 **git-Revision:** ac72edfc6f1ee58a654f36a1c5597dbe25cd6c12 

**Funktionalität:**    
Eingabe der Regelparameter und des Zeitinkrements, Eingabe der Iterationsschritte für die dynamische Speicheranforderung, zyklische Eingabe der Eingangswerte, Berechnung und Ausgabe der Ausgangswerte.    

**Ergebnis:**   
Einrückungen des Codes machen den Quelltext übersichtlich aber bei den Kommentaren gibt es je nach Editor willkürliche Einrückungen. 
Die Benennung der Variablen ist meist sinnvoll, aber die Kennzeichnung der Indizes durch Unterstriche (z.B. _alt) nicht entsprechend der Richtlinien, jedoch sind die Bezeichnungen so übersichtlicher als mit Worttrennung durch Großbuchstaben. Das Feld zum Speichern der Ergebnisse ist mit "feld" nicht verständlich benannt.
Es gibt keine veralteten Kommentare. Die Kommentare in Zeile 31 und 52 sind redundant. Ein erklärender Kommentar zur Zeile 37 fehlt.
Der dynamischer Speicher ist korrekt angefordert und freigegeben. 
Unsinnvolle Eingaben von n sind möglich. Dies führt zu einer fehlerhaften Speicheranforderung (nichtpositive Feldgrößen) und dazu, dass die for-Schleifen nicht aufgerufen werden, da i=0 größer als n ist. Also muss eine Überprüfung der Eingabe von n auf Sinnhaftigkeit implementiert werden.
Keine einzige Fehlermeldung vorgesehen. 
Keine objektorientierte Programmierung - alles als eine einzige main-Funktion, kein Auslagern von Funktionen. Mindestens die Berechnung könnte als Funktion ausgelagert werden. 

