# Fernwartung

Auch wenn alles perfekt automatisiert ist, werden Sie von Zeit zu Zeit einen Blick auf den Computer Ihres Public Displays werfen wollen, um z.B. System-Updates einzuspielen, neue Software zu installieren etc.

Die einfachste Art dies zu tun, ist es, sich mit einer Fernwartungssoftware auf den jeweiligen Rechner draufzuschalten. Windows bringt von Hause aus das Werkzeug Remotedesktopverbindung mit. Im Folgenden beschreiben wir, wie Sie diese nutzen können.

## Remotedesktop

### Aktivierung auf Ihrem E-Board

> #### primary::Hinweis
>
> Alle von uns ausgelieferte Rechner sind mit Remotedesktop darauf aktiviert worden. Wenn Sie einen Rechner von uns gekauft haben, können Sie diesen Schritt überspringen.

In Windows ist standardmäßig die Remotedesktop-Funkion deaktiviert, so dass man sie auf einem Rechner erst konfigurieren muss, um den Zugriff zu ermöglichen. 

* Drücken Sie die Tastenkombination `[Windows]` + `[R]`, um das Dialogfenster `Ausführen` zu öffnen. Dort geben Sie den Befehl `sysdm.cpl` ein und bestätigen mit `OK`.

![](/images/sysdm.jpg)

Unter der Registerkarte `Remote` findet man die Option `Remoteverbindung mit diesem Computer zulassen`. Markieren Sie diese und klicken Sie anschließend auf `OK`.

![](/images/sysdm-remote.jpg)

### Eine Verbindung mit Ihrem E-Board aufbauen

* Um sich mit Ihrem E-Board zu verbinden, öffnen Sie die Client-Software `Remotedesktopverbindung`, indem Sie die Tastenkombination `[Windows]` + `[R]` drücken, um das Dialogfenster `Ausführen` zu öffnen. Dort geben Sie den Befehl `mstsc` ein und bestätigen mit `OK`.

![](/images/mstsc.jpg)

Im Computerfeld geben Sie den Namen Ihres Displayrechners ein und klicken anschließend auf `Verbinden`.

![](/images/RDC-Computername.jpg)

Sie werden nun aufgefordert, Ihre Anmeldeinformationen einzugeben. Bei Rechnern von uns geben Sie die unten gezeigten [Zugangsdaten](#Zugangsdaten) ein.

![](/images/Anmeldeinformationen_eingeben.jpg)

Falls Sie einen eigenen Rechner verwenden und den Rechnernamen nicht wissen, finden Sie ihn unter Systemeigenschaften:

* Drücken Sie die Tastenkombination `[Windows]` + `[R]`, um den Dialog Ausführen zu öffnen. Dort geben Sie den Befehl `sysdm.cpl` ein und bestätigen mit `OK`.

![](/images/Systemeigentschaften.png)

## Zugangsdaten {#Zugangsdaten}

Alle von uns ausgelieferte Rechner sind mit dem Benutzernamen **User** und keinem Kennwort eingestellt, damit er sich automatisch anmelden kann. Das Konto Administrator ist deaktiviert und hat ebenfalls kein Kennwort.

Für Rechner mit Windows 10 Professional stellen wir meistens den Rechnernamen **W10PPC** ein. Dies kann allerdings je nach Rechnermodell variieren. 

![](/images/W10PPC.jpg)

Für Rechner mit Windows 7 Embedded stellen wir meistens den Rechnernamen **WE7PC** ein. Dies kann allerdings je nach Rechnermodell variieren.

![](/images/WE7PC.jpg)

## Sperrung des Bildschirms verhindern, wenn man unterbricht

Mit Remotedesktop-Verbindung wenn Sie als Administrator sich zu einem entfernten Computer verbinden, sperrt die Anzeige des Remotedesktops, sobald die Verbindung beendet worden ist. Es wird dann notwendig, dass jemand die Anzeige direkt am entfernten Computer entsperrt, um das den Inhalt der Anzeige wieder anzuzeigen.
 
Es gibt keine Option im normalen Interface von Remotedesktop-Verbindung, um dies zu verhindern. Microsoft macht das aufgrund der Sicherheit. Eine Batchdatei unterbricht jedoch die Remotedesktopsitzung ohne die Anzeige zu sperren. Außerdem  kann der Benutzer vorher (innerhalb von 30 Sekunden gibt) das SHOWTIME-Projekt starten, bevor anschließend die Remotedesktopsitzung unterbrochen wird.

* Downloaden Sie und extrahieren Sie die Zip-Datei [Trennen.zip](https://download.stueber.de/bin/de/windowsembedded/Trennen.zip) auf den Desktop des Player-Rechners (Anzeige-Display). Wenn Sie die Remote-Verbindung unterbrechen möchten, wählen Sie per Rechtsklick die Batch-Datei Trennen.bat und klicken Sie auf "Als Administrator ausführen".
 
![](/images/Trennen_als_administrator_ausführen.jpg)

* Ein schwarzes Fenster wird sich anschließend öffnen, das Ihnen 30 Sekunden gibt, um Ihr SHOWTIME-Projekt auszuführen, bevor es die Remote-Sitzung unterbricht. Der ganze Vorgang kann durch Drücken der Tastenkombination `[Strg]` und `[C]` abgebrochen werden.

![](/images/Trennen_30Sek.jpg)

> #### primary::Hinweis
>
> Am besten ist es, wenn Ihr Projekt im SHOWTIME-Player ausgewählt und betriebsbereit ist, so dass Sie nur `Ausführen` klicken müssen.

![](/images/SHOWTIME-starten.jpg)




