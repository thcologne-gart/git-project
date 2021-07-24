# Aufgabe 2 - OPC UA
In dieser Aufgabe werdet ihr einen OPC UA Server auf Grundlage von NodeOPCUA erstellen und diesen mit Modellen sowie Daten aus dem AAS Server aus Aufgabe 1 befüllen.

## Grundlagen
* Ihr benötigt den [AAS Server aus Aufgabe 1](Aufgabe1.md)
* NodeOPCUA muss [installiert](../Installation/node-opcua.md) sein
* [UaExpert](https://www.unified-automation.com/de/produkte/entwicklerwerkzeuge/uaexpert.html) und [UaModeler](https://www.unified-automation.com/de/produkte/entwicklerwerkzeuge/uamodeler.html) werden benötigt
  * Für beide Programme ist eine kostenlose Registrierung bei Unified Automation notwendig
* Die XML-Dateien bestimmter OPC UA Modelle werden benötigt:
  * [GitHub der OPC Foundation](https://github.com/OPCFoundation/UA-Nodeset)
  * [Beispielhaftes Pumpenmodell](../Dateien/UaModeler/Opc.Ua.Pumps.NodeSet2.xml)
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E4: [OPC UA - NodeOPCUA Server erstellen und erkunden](https://www.youtube.com/watch?v=5lWk-aKc0uw&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=5)
  * E5: [OPC UA - Informationsmodell in UaModeler erstellen und exportieren](https://www.youtube.com/watch?v=CrCrjT1zP1s&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=6)
  * E6: [OPC UA - NodeOPCUA Server per REST API mit Daten aus BaSyx AAS Server befüllen](https://www.youtube.com/watch?v=DVMfyJXxlR4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=7)
  
## Aufgabenstellung
* Erstelle anhand der bereitgestellten Daten und auf Grundlage einiger OPC UA Modelle ein OPC UA Informationsmodell für die *Master Pump 420*. Folgende Modelle sind als Grundlage zu nutzen:
  * OPC 10000-100 - Part 100: Device Information Model
  * OPC 40001-1 - UA CS for Machinery Part 1 - Basic Building Blocks
  * [Beispielhaftes Pumpenmodell](../Dateien/UaModeler/Opc.Ua.Pumps.NodeSet2.xml)
* Nutze NodeOPCUA, um einen OPC UA Server mit dem Informationsmodell zu erstellen und befülle diesen mit den Daten aus dem AAS Server.
* Erkunde den OPC UA Server mit einem OPC UA Client, beispielsweise UaExpert und stelle sicher, dass alle Daten aus dem AAS Server auch korrekt abgebildet sind.
* Überlege dir eine Möglichkeit, Daten aus dem OPC UA Server auf den AAS Server zu schreiben und implementiere diese als schreibbare Variable.

## Hinweise
* Für die Projektarbeit im Labor wird das Informationsmodell vorgegeben.
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit NodeOPCUA sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
    <li>Der UaModeler muss genutzt werden, um eine XML-Datei zu erstellen</li>
	<li>Wenn du an die Grenzen des kostenlosen UaModelers stößt, exportiere die maximale Node-Anzahl und setze die Bearbeitung im XML-Editor fort</li>
    <li>Der HTTP Client im OPC UA Server (hier Axios) muss genutzt werden um das [BaSyx API](https://app.swaggerhub.com/apis/BaSyx/basyx_asset_administration_shell_repository_http_rest_api/v1) umzusetzen</li>
  </ul>
</details>