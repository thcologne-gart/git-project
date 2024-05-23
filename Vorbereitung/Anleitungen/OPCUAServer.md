# OPC UA Server
Der Beispiel OPC UA Server startet automatisch, verfügt jedoch über keine Daten. Um ihn mit Objekten und Daten zu füllen, sollte folgender Anleitung gefolgt werden.

## Startvorgang
Sobald die VM und Node-Red vollstädnig gestartet sind, startet auch der OPC UA Server. All das dauert ein paar Minuten, wenn Node-Red oder der Server nicht sofort erreichbar sind, einfach kurz warten.

Wurde der Server erfolgreich und vollständig gestartet, kann dieser mit Objekten, Variablen und Daten befüllt werden. In dem Beispiel sollten dazu die Nodes am linken Ran von oben nach unten durch geklickt werden (außer der Restart!). Dabei werden folgende Operationen durchgeführt:
* das Objekt "VendorName" wird gelöscht, welches standardmäßig in diesem OPC UA Server vorhanden ist
* der Ordner "Objects" wird als Ziel für folgende Operationen selektiert
* das Objekt "Asset" wird in "Objects" erstellt
* das Objekt "Asset" wird als Ziel für folgende Operationen selektiert
* Die Variablen "DoubleVariable", "StringVariable" und "BooleanVariable" werden im Objekt "Asset" erstellt
* Für die Variable "DoubleVariable" wird der historisierungs Dienst installiert
  * Dieser speichert in einem Ring-Buffer die letzten 1000 Werte
* Die Variablen werden mit Daten befüllt
  * "StringVariable" mit einem String aus der XML-Datei
  * "DoubleVariable" sekündlich mit einem Zufallswert
  * "BooleanVariable" kann per Node von false auf true gewechselt werden und umgekehrt

## Verbindung zu dem Server
Der OPC UA Server kann mit einem OPC UA Client wie dem [UaExpert](../Linkliste.md) erkundet werden. Der Server wird über das `+` in der Symbolleiste hinzugefügt. Wenn UaExpert in der VM installiert wird, kann als Adresse `opc.tcp://localhost:53880` verwendet werden, ist UaExpert auf der Host-Maschine installiert, muss statt `localhost` die IP der VM eingegeben werden. Diese kann innerhalb der VM im Terminal durch das Kommando `ifconfig` ermittelt werden.

Nach Einrichtung des Servers als Data source in Grafana, können die Daten auch direkt mit Grafana erkundet werden.

## Weitere Hinweise
* Die Beispiel Nodes sind kommentiert und erläutern ihre Funktionsweise.
* Die restart Node kann verwendet werden, um den OPC UA Server neu zu starten, ohne die VM neu zu starten
  * Dies kann bei Veränderung der Parameter nötig werden
* Der Netzwerk Port des Servers wird in der Server Node selbst eingestellt
  * Ebenso wie einige weitere Merkmale
