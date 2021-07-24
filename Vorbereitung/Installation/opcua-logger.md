# Installation des opcua-loggers

Dieses Dokument dient als Anleitung zur Installation des opcua-loggers auf Windows 10.

:information_source: **Diese Anleitung wurde mit einer modifizierten Version des opcua-loggers 2.0.0-alpha getestet.**

### Vor der Installation
* NodeJS muss installiert sein

:information_source: Notiert euch alle wichtigen Daten, insbesondere Zugangsdaten und Datenbanknamen.

:information_source: `<...>` dient als Platzhalter für einen bestimmten Wert. Hier muss entweder ein bereits bekannter Wert eingegeben oder ein neuer Wert festgelegt werden (ohne `<` und `>`)!

### Installation
* Besuche das [GitHub Repository des modifizierten opcua-loggers](https://github.com/Eichi87/node-opcua-logger) und lade  alle Dateien in einen lokalen Ordner. Bsp.: `C:\opcua-logger`
  * im Folgenden `<local-folder>` genannt
* Öffne die Eingabeaufforderung (cmd)
* Navigiere in der Eingabeaufforderung zum `<local-folder>`
* `npm install` ausführen

### Hinweise
* Der verlinkte opcua-logger ist leicht modifiziert. Neben den drei Standard-Datentypen `string`, `number` und `boolean` ist nun auch der Datentyp `localizedText` verfügbar. Dieser Datentyp ermöglicht den Upload von Nodes des OPC UA Datentyps `localizedText` indem der Wert der zuerst eingetragenen Sprache gelesen und als String hochgeladen wird.
  * Bsp.: Verfügt ein Merkmal über den Value `[locale: en, text: Pump; locale:de, text:Pumpe]`, wird der String `Pump` in die Datenbank hochgeladen.
* Das [originale GitHub Repository des opcua-loggers](https://github.com/coussej/node-opcua-logger) enthält einige nützliche Informationen

Damit ist die Installation des opcua-logger abgeschlossen. 