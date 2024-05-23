# Zusammenfassung
Anhand der hier abgelegten Anleitungen können der Beispielserver mit Beispielvisualisierung in Betrieb genommen werden. Außerdem sind Hinweise hinterlegt, anhand derer eigene Server erstellt und visualisiert werden können.

## Beispielserver
Nachdem der Beispielserver in Node-Red gestartet ist und erfolgreich mit Objekten, Variablen und Daten befüllt wurde, kann dieser über den UaExpert und Grafana erkudnet werden. Der genutzte Port ist ´53880´.

## Beispieldashboard
In Grafana ist ein Dashboard vorbereitet, dass den Beispielserver aufgreift und die verfügbaren Daten anzeigt. Dieses Dashboard kann als grundlage für eigene Dashboards dienen. Wenn der OPC UA Server vollständig läuft, läuft das Dashboard automatisch.

## XML Datei
Die XML Datei enthält nur eine minimale Struktur und einen Datenpunkt, um für den Beispielserver zu agieren. Hier sollte jeder eine eigene Datei für den eigenen Server erstellen.

## Eigener Server, eigenes Dashbaord, eigene XML Datei
Um die Beispielelemente zu erhalten, sollte für alle Komponenten ein eigenes Pendant erzeugt werden. In Node-Red also ein separater Flow, als statische Datengrundlage eine separate XML Datei und in Grafana ein separates Dashboard.

## Hinweise
* *Spielt* so viel wie möglich mit den Komponenten rum und versucht die Grenzen zu finden. In der Projektarbeit vor Ort werden neue Elemente und Arbeitsschritte eingeführt, sodass die hier erworbenen Kompetenzen vorausgesetzt werden.
