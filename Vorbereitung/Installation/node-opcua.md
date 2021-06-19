# Installation von NodeOPCUA

Dieses Dokument dient als Anleitung zur Installation von NodeOPCUA auf Windows 10.

:information_source: **Diese Anleitung wurde mit der offiziellen NodeOPCUA v2.43.0 getestet.**

### Vor der Installation
* NodeJS muss installiert sein

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

:information_source: `<...>` dient als Platzhalter für einen bestimmten Wert. Hier muss entweder ein bereits bekannter Wert eingegeben oder ein neuer Wert festgelegt werden (ohne `<` und `>`)!

### Installation
* Erstelle einen lokalen Ordner für den OPC UA Server. Bsp.: `C:\opcua-server`
  * im Folgenden `<local-folder>` genannt
* Öffne die Eingabeaufforderung (cmd)
* Navigiere in der Eingabeaufforderung zum `<local-folder>`
* `npm init` ausführen und die geforderten Daten eingeben
  * Was konkret eingegeben wird hat auf das Beispiel keinen Einfluss
* `npm install node-opcua --unsafe-perms` ausführen und Fertigstellung abwarten
* `npm i axios` ausführen und Fertigstellung abwarten
* `model` Ordner aus diesem Repository kopieren und in `<local-folder>` einfügen
  
Damit ist die Installation von NodeOPCUA abgeschlossen.
