# Aufgabe 1 - Node-RED, AAS, REST
In dieser Aufgabe werdet ihr einen AAS Server via REST-API aus Node-RED mit Daten befüllen.

## Grundlagen
* Ihr benötigt eine [lokale Node-RED Instanz](../Installation/node-RED.md)
* Beachtet die [Hinweise zu dem BaSyx Video](../Installation/BaSyx.md)
* Die Daten einer fiktiven [Pumpe](../Dateien/Pumpendaten) werden benötigt
* [Simulations-Flow](../Dateien/node-RED) für Node-RED
* [Konfigurationsdateien](../Dateien/BaSyx) für BaSyx
* [BaSyx AAS Repository HTTP REST-API](https://app.swaggerhub.com/apis/BaSyx/basyx_asset_administration_shell_repository_http_rest_api/v1)
* [AASX Package Explorer Screencasts](https://admin-shell-io.com/screencasts/) 
* Grundsätzlich ist die [Videos.md](../Videos.md) Datei zu beachten
* Folgende Videos stehen in direktem Zusammenhang mit der Aufgabe:
  * E1: [Node-RED - JavaScript Objekt aus XML Datei erzeugen](https://www.youtube.com/watch?v=Lc5fmeFqGl4&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=2)
  * E2: Fraunhofer IESE: [Getting started with Eclipse BaSyx: Easy AAS setup with off-the-shelf components](https://www.youtube.com/watch?v=nGRNg0sj1oY&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=3)
  * E3: [Node-RED - BaSyx AAS Server per REST API mit Daten befüllen](https://www.youtube.com/watch?v=bhNZlhZ4J8s&list=PLzbl7wFtWqTR72ODjOUj5aEGsa4TxXYhy&index=4)
  
## Aufgabenstellung
* Richte anhand der bereitgestellten Daten einen AAS Server für die *Master Pump 420* ein.
  * Nutze den BaSyx AAS Server Docker Container.
* Bilde in dem AAS Server statische sowie dynamische Daten ab.
  * Die statischen Pumpendaten sind aus einer `.xml` Datei auszulesen und dürfen nicht bereits im Modell enthalten sein.
  * Die dynamischen Daten können aus einer Node-RED-internen Simulation entnommen werden, grundsätzlich ist die Quelle jedoch freigestellt.
* Bilde unterschiedliche Merkmals- und Datentypen in dem AAS Server ab.
  * Beispielsweise könnte der Produktname in unterschiedlichen Sprachen vorliegen und somit ein Multi Language Property sein.
* Erkunde den AAS HTTP Server mit einem Browser, um sicherzustellen, dass alle Daten korrekt angezeigt werden.
* Erstelle einen weiteren Node-RED Flow und ließ die AAS aus.
  * Optional kannst du ausprobieren, die ausgelesenen Daten in eine neue Datei zu schreiben.
* Füge das Node-RED contribution package für Modbus hinzu und analysiere die verfügbaren Nodes
  * node-red-contrib-modbus ist [hier](https://flows.nodered.org/node/node-red-contrib-modbus) verfügbar. Es wird entweder über das Node-RED CLI via `npm install node-red-contrib-modbus` oder über das [Node-RED UI](https://nodered.org/docs/user-guide/runtime/adding-nodes) hinzugefügt.

## Hinweise
* Für die Projektarbeit im Labor wird das Informationsmodell vorgegeben.
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit Node-RED sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
   <li>Kannst du Docker Desktop nicht nutzen, lassen sich Node-RED sowie BaSyx AAS Server auch 'stand-alone' betreiben. Siehe dazu: <a href="https://nodered.org/docs/getting-started/local">Node-RED</a>, <a href="https://github.com/thcologne-gart/git-project/blob/main/Vorbereitung/Installation/BaSyx.md#ohne-docker-desktop">BaSyx AAS Server</a></li>
   <li>Kannst du den AASX Package Explorer nicht auf deinem System nutzen, bitte eine Kommilitonin oder einen Kommilitonen mit dir zusammenzuarbeiten.</li>
   <li>Der AASX Package Explorer muss genutzt werden um eine `.aasx` Datei zu erstellen. Diese `.aasx` Datei muss das Informationsmodelle der Pumpe abbilden und darf keine Werte enthalten.</li>
   <li>Die `.xml` Datei mit den statischen Pumpendaten muss von dir erstellt werden. Diese `.xml` Datei muss die Werte zu den Merkmalen aus dem Informationsmodell enthalten.</li>
   <li>Die Simulation darf beliebig erweitert oder ersetzt werden.</li>
   <li>Nutzt du die Server.jar Datei anstelle des Docker Containers, müssen `context.properties` sowie `aas.properties` in dem Ordner `resources` liegen. Die `.aasx` Datei muss in demselben Ordner wie die `Server.jar` Datei liegen.</li>
  </ul>
</details>


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
