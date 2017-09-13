## Bug Report 1    

**Autor:** Marvin Frede

**Modul:** In der Datei einlesen2.0.cpp, Funktion "ersetzen"

**Git-Reversion:** c3a07d76d049bb3a19a83c6137c5d9588a3344b9

**Fehler Beschreibung:**

Es tritt ein Fehler bei der Ausführung der Funktion "ersetzen" auf.
Die Funktion beinhaltet eine for_Schleife in der eine If-Abfrage die Trennzeichen in den eingelesenen Strings in Leerzeichen umwandelt. In der Terminalausgabe des Programmes sieht man, dass ohne die Funktion (Funktion auskommentieren und die For-Schleife in der Main Funktion wieder entkommentieren), eine korrekte Ausgabe erfolgt in die Zahlen fehlerfrei ausgegeben werden und die Beispiel Addition korrekt ausgeführt wird.

Ist nun die Funktion aktiviert, sind die Zahlen die in der zweiten Spalte der Ecxel-Datei stehen beziehungsweise hinter dem Trennzeichen in der CSV-Datei allesamt Null. Es gibt Ausnahmen und zwar die Zeilen, die als Trennzeichen einen Tabulator oder Leerzeichen haben, werde korekt ausgewertet. Das bedeutet dass dort die zweite Zahl korrekt ausgelesen und abgespeichert wurde. Dies zeigt mir, dass die Funktion im Grunde funktioniert, es allerdings zu Problemen bei Kommatas, Leerzeichen und Semikolons kommt. Dieser Fehler ist klar reproduzierbar, da man beliebig viele Werte in der Datei speichern kann und es wiederholt zu dem selben Ergebnis/ Fehler kommt.         
     
**Fehlerbehebung:**    
Der Fehler wurde in einer späteren Version beseitigt (3e8639c9f4ea0f515fbc2302d1e048dd39e7a944). Wo genau der Fehler lag konnte ich nicht herrausfinden. Durch weiteres auslagern in Funktionen und Nutzung von bereits vorhanden Funktionen aus der Standardbibliothek verschwand der Fehler und tauchte nicht mehr auf. Damit ist für mich der Bug beseitigt und nicht mehr reprodozierbar.    


## Bug Report 2   
**Autor:** Marvin Frede   
    
**Modul:** einlesen.cpp   
   
**Git-Reversion:** 8c2ecb972c97640328e2ed669bd0b62f5233f9d8

**Fehler Beschreibung:**

Ein Fehler tritt auf, wenn mehr als die ersten Zeilen aus Text oder Buchstaben bestehen. Der Text oder Buchstabe kann nicht korrekt angegebn werden, da der string später in zwei Variabeln aufgespalten wird. Diese Variablen sind allerdings vom Datentyp float. Dadurch ist der Fehler, dass zwei Nullen angezeigt werden.   

Ein weiterer Fehler tritt  auf, wenn als Trennzeichen kein Leerzeichen, Tabulator, Kommata oder Semikolon benutzt wurden ist. Dieser Fehler sollte abgefangen werden bzw. eine kurze Nachricht mit einer Fehlermeldung ausgegeben werden, damit der User weiß wo der Fehler liegt.   

Kein Fehler, allerdings fehlt nach der if-Anweisung eine Abbruchbedingung. Hat im Programm keine schweren Auswirkungen, allerdings könnte es zu Problemen führen.    
    
**Fehlerbehebung:**     
Es wurde in einer späteren Programmversion (17b1b829601086c278db5c93b1474b1d5aedd2e3) eine Abbruchbedingung in die if-Anweisung integriert um mögliche Fehler zu umgehen und eine guten Programmierstil zu wahren.    
Das Problem mit den Trennzeichen bin ich nicht angegangen, da wir dem Nutzer sagen werden, dass nur bestimmte Trenzeichen verwendet werden dürfen.    
Des Weiteren ist der oberste der drei Fehler nicht leicht zu beseitigen. Ich habe keine bessere Möglichkeit gefunden die ersten Zeilen solange zu überspringen bis die Zahlenwerte erreicht sind. Die ignore() Funktion brachte für dieses Problem keine Lösung und war auch nicht erfolgreich um zum Beispiel pauschal die ersten beiden Zeilen zu überspringen. Deswegen bleibt die ursprüngliche Lösung weiterhin im Programm erhalten.

## Bug Report 3   
**Autor:** Florian Siebert   
    
**Modul:** Strecke.cpp   
   
**Git-Reversion:** 7e1babf4d63ffa77eb3379892dd06883224509bb

**Fehler Beschreibung:**
Fehler zur Kompilierzeit; Code lässt sich nicht kompilieren.  Ursache: Syntax. In Zeile 11 steht statt eines Semikolons ein Komma, sodass die Variable alpha_neu nicht definiert wurde und somit auch in Zeile 34 zu einer Fehlermeldung führt. Außerdem fehlt in Zeile 45 ein Leerzeichen zwischen "int" und "i".

**Fehlerbehebung**
Syntax in Revision ac72edfc6f1ee58a654f36a1c5597dbe25cd6c12 korrigiert, Kompilieren möglich. 

## Bug Report 4   
**Autor:** Florian Siebert   
    
**Modul:** main.cpp   
   
**Git-Reversion:** 28b4f3c275946e01fb2cc274c2ee0a03fd46f4c9

**Fehler Beschreibung:**
Fehler zur Kompilierzeit; Code lässt sich nicht kompilieren.  Ursache: Syntax. Die von Florian S. eingefügten Codeteile tragen die von ihm gewählten Bezeichnungen, die nicht mit den von Marvin und Florian Z. gewählten übereinstimmen. 

**Fehlerbehebung**
Variablennamen in Revision 815b573b6531618d5fe16cc889c3c6b54aa931b9 gändert, Kompilieren möglich. 


## Bug Report 5    

**Autor:** Florian Zaschka

**Modul:** main.cpp

**Git-Reversion:** 8193f76fa25d606b26b3adf4308197b9f39a9f60

**Fehler Beschreibung:**
In der Funktion abfrage () kann der Anwender zwar seine ganzen Daten eingeben (Doppelnamen, Sonderzeichen sind möglich) jedoch können keine Umlaute eingelesen werden. Diese werden in der späteren Ausgabe falsch dargestellt. Da die Beseitigung des Bugs in unserer momentanen Projektphase nicht mehr durch eine Änderung des Codes durchgeführt werden kann, wird dieser Umstand mit ins Handbuch aufgenommen


**Fehlerbehebung**   
Im Handbuch am 05.07.2017 aufgenommen

## Bug Report 6    

**Autor:** Florian Zaschka

**Modul:** speichern2.cpp

**Git-Reversion:** 43ff4fc13e4b5bcc22b36d4f87106adcbc69fdc7

**Fehler Beschreibung:**
Das Erstellen von Zeigern für die Wertespeicherung ist speicherintensiv und fehleranfällig. Weiterhin gab es keine Freigabe des Speicherplatzes am Ende des Programms. Als einfachere Lösung bietet es sich an, die Werte direkt in dem Moment, in dem sie im Programmablauf errechnet werden, in die Ergebnistabelle zu schreiben. 

**Fehlerbehebung**    
In Revision 4b2cffcb1c8aa67fb65c864ded8c37c76e01a574 ist die Speicherlogik geändert worden



