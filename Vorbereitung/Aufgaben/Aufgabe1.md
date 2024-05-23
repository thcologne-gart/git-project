# Aufgabe 1 - Node-RED, OPC UA
In dieser Aufgabe werdet ihr einen OPC UA Server in Node-Red anlegen und mit statischen sowie dynamischen Daten befüllen.

## Grundlagen
* Die [Anleitungen](../Anleitungen)
* Die Ubuntu VM wird benötigt
  * Das Passwort zum Nutzer `GIT` lautet `git`
* [UaExpert](https://www.unified-automation.com/de/produkte/entwicklerwerkzeuge/uaexpert.html) ist optional auf der Host-Maschine zu installieren
  * Hier ist eine kostenlose Registrierung bei Unified Automation notwendig
* Die Daten einer fiktiven [Pumpe](../Dateien/Pumpendaten) werden benötigt
* Das Dokument [OPC UA Server starten](../Aufgaben/OPCUAServer.md") führt euch durch den Start nach erfolgreicher Einrichtung der VM.
  
## Aufgabenstellung
* Richte anhand der bereitgestellten Daten einen OPC UA Server für die *Master Pump 420* ein.
  * Die Beispiel Nodes im Flow "OPC UA Server" sollen dabei eine Hilfestellung sein. Bestenfalls erstellst du einen neuen Flow, damit die Beispiele erhalten bleiben.
* Bilde in dem OPC UA Server statische sowie dynamische Daten ab.
  * Die statischen Pumpendaten sind aus der `.xml` Datei auszulesen und dürfen nicht "hardcoded" sein.
    * Die `.xml` Datei ist bereits in der VM unter dem Pfad `~/node-red-files` zu finden und kann dort auch bearbeitet werden.
  * Die dynamischen Daten können aus einer Node-RED-internen Simulation entnommen werden.
    * Auch hierfür ist ein Beispiel bereitgestellt.
* Bilde unterschiedliche Datentypen in dem OPC UA Server ab.
  * Beispielsweise könnten der Produktname als `String` und das Datum als `DateTime` Datentyp vorliegen.
* Erkunde den OPC UA Server, um sicherzustellen, dass alle Daten korrekt angezeigt werden.
  * Dies ist in Grafana oder über den, auf der Host-Maschien installierten UaExpert möglich

## Hinweise
* Denke daran, dass nach dem *automatischen* und *erfolgreichen* start des OPC UA Servers die Objekte, Variablen und Daten erst erstellt/eingelesen werden müssen.
* Für die Projektarbeit im Labor wird ein Informationsmodell vorgegeben.
* Tauscht euch untereinander aus!
* Im Rahmen der Aufgabe bietet es sich an, verschiedene Methoden und Herangehensweisen zu testen und grundsätzlich mit Node-RED sowie den Daten *zu spielen*.

## Tipps
<details>
  <summary>Hier findest du ein paar Tipps</summary>
  <ul>
   <li>Die IP-Adresse der VM kann über den Terminal mit dem Kommando `ifconfig` ermittelt werden.</li>
   <li>Die `.xml` Datei kann direkt in der VM im Text-Editor bearbeitet werden.</li>
   <li>Die Simulation darf beliebig erweitert oder ersetzt werden.</li>
  </ul>
</details>
