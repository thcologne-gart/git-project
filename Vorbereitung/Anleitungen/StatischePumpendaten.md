# Statische Pumpendaten über die XML einfügen
Die VM verfügt über eine XML Datei, die die statischen Pumpendaten enthalten soll. Aktuell ist dort nur ein statischer Wert als Platzhalter hinterlegt.

## Speicherort und Bearbeitungsmöglichkeiten
Die Datei ist innerhalb der VM unter dem PFad `~/node-red-files` abgelegt und kann mit dem Ubuntu Text-Editor bearbeitet werden. Ein XML-Editor ist nicht vorgesehen und angesichts des minimalen Umfangs der Datei auch nicht notwendig. Eine XSD Datei muss *nicht* erstellt werden.

Um das Beispiel zu erhalten, sollte eine Kopie der Datei erstellt werden, die in demselben Ordner unter einem anderen Namen abgelegt wird. Diese Datei kann dann nach Wunsch angepasst werden und in einem eigenen OPC UA Server referenziert werden.

## Aufruf aus Node-Red
Innerhalb des Node-Red Flows sind zwei Nodes vorgesehen, die sich mit dem Aufruf und der Konvertierung der XML Datei beschäftigen. Diese zu identifizieren und zu verstehen ist ein wichtiger Schritt. Außerdem kann das Ergebnis der zweiten Node in einer Debug Node ausgegeben werden, um die Struktur des erzeugten JS Objekts zu analysieren.

## Hinweise
* Trotz der geringen Komplexität der Vorbereitung macht es unter Umständen Sinn, sich Gedanken über die Datenstruktur und Möglichkeiten zur Skalierung zu machen
