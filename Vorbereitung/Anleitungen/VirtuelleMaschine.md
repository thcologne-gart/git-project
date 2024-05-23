# Virtuelle Maschine
Zur Durchführung der Vorbereitung wird euch auf eurer Lernplattform eine Virtuelle Maschine auf Ubuntu Basis bereitgestellt. Diese enthält bereits alle notwendigen Komponenten und bedarf keiner Installation.

## Entpacken
Die Virtuelle Maschine wurde in zwei ZIP Dateien aufgeteilt, um die Verteilung zu vereinfachen. Diese müssen *gemeinsam* entpackt werden, damit ein vollständiger Ordner mit allen notwendigen Dateien entsteht.

## Starten
Um die VM zu starten, benötigt ihr einen VM Player. Ich empfehlen den [VMware Workstation Player](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html). Dieser ist für private Zwecke kostenlos einsetzbar und startet die VM ohne Probleme.

Nach der Installation des Players, kann dieser gestartet werden. Über einen Klick auf "Open a Virtual Machine" kann die `GIT 2024.vmx` Datei im **entpackten** Ordner ausgewählt werden. Anschließend startet die VM. Auf nachfrage, ob die VM verschoben oder kopiert wurde bitte mit "copied" antworten.

Der Start kann ein paar Minuten dauern. Je nach Leistungsfähigkeit des Host-Systems.

## Handhabung
Die VM wurde mit dem Betriebssystem Ubuntu erstellt. Dies ist eine Windows-ähnliche Linux Distribution und kann dank des Desktops größtenteils mit der Maus bedient werden.

Nach dem Start der VM starten alle nötigen Komponenten automatisch. Es kann notwendig sein, die beiden sich öffnenden Browser Fenster zu aktualisieren, damit der Inhalt angezeigt wird. Auch dies kann ein paar Minuten dauern. Wenn alles erfolgreich gestartet und aktualisiert wurde, sind der Beispiel Node-Red Flow und das Beispiel Dashboard in Grafana zu sehen.

## Hinweise
* Der Terminal für Kommandozeileneingaben befindet sich am linken Rand, ebenso wie die gesamte "Taskleiste".
* Im Umgang mit Linux ist peinlich genau auf Groß- und Kleinschreibung sowie Dateiendungen zu achten, da dies hier eine größere Rolle als bei Windows spielt.
* Unvorsichtiger Umgang mit dem Terminal kann schnell das gesamte System lahmlegen, also vor dem *Enter* darüber nachdenken, was man eingegeben hat.
* Die VM kann, bevor Änderungen vorgenommen werden, lokal kopiert werden, um ein Backup zu haben. Dazu einfach, bei abgeschalteter VM, den gesamten Ordner kopieren und umbenennen.
