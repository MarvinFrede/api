![Regelkreis](images/Regelkreis.PNG)

Züge können für schnellere Kurvenfahrten mit einem Neigesystem ausgerüstet werden. Dieses sorgt in einer Kurvenfahrt dafür, dass sich der Zug in die Kurve legt und somit die Fliehkräfte parallel zur Wagonhochachse liegen.

Ein solches System wurde nun für einen Zug entwickelt aber noch nicht gebaut. Vorher soll durch eine Simulation getestet werden, ob die vorher festgelegten Parameter für das Neigesystem richtig festgesetzt wurden. Regelbar ist bei einem solchen System generell nur das vom Neigesystem erzielbare Drehmoment, welches für die Winkelbeschleunigung des Wagons sorgt.

Wir werden mit festgelegten Parametern eine Proportionalregelung für das Neigesystem simulieren, das in einer Kurvenfahrt entsprechend die Fliehkräfte ausgleichen soll. Fatal wäre hier, wenn es zu einer Schwingungsanregung in bestimmten Situationen kommen könnte. Zwar sind die Regelparameter theoretisch berechenbar, aber im Gegensatz zu den sonst üblichen verwendeten mathematischen Methoden in der Regelungstechnik kann unser Regler nur diskrete Werte als Input erhalten. Wir können mit dieser Software also sowohl die Regelungsparameter optimieren, sowie den Einfluss der zeit- und wertediskreten Eingaben überprüfen.

