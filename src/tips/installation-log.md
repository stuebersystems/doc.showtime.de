# Ein Installationsprotokoll erstellen

Sollten während der Installation von CONFIRE SHOWTIME Probleme auftreten, ist es ratsam ein Installationsprotokoll (setup log) anzulegen. Dies ist eine Textdatei, in die alle Schritte der Installation mitprotokolliert werden.

1. Kopieren Sie das Installationspacket (`confireshowtime64.msi` oder `confireshowtime32.msi`) in einen Ordner Ihrer Wahl.

2. Öffnen Sie die Windows-Eingabeaufforderung und tippen Sie folgenden Befehl ein:
   
   ````
   msiexec /i "C:\Setups\confireshowtime64.msi" /L*V "C:\Setups\showtime.log"
   ````
   
   Natürlich sind die Pfad- und Dateiangaben nur beispielhaft und können auch anders lauten.
   
3. Bestätigen Sie mit `[Enter]`. Die Installation wird gestartet.

4. Folgen Sie nun wie gewohnt den Anweisungen des Assistenten. Wird die Installation vorzeitig abgebrochen, erscheint im letzten Fenster die Option `Log anzeigen`.
   
   ![Option zum Anzeigen des Protokolls](/images/setup-log.png)

5. Kreuzen Sie diese Option an und klicken Sie auf `Fertigstellen`. Der Windows-Editor öffnet sich und zeigt Ihnen nun das Protokoll der Installation an.

Sie können diese Protokolldatei jetzt an unser [Support Team] schicken, damit wir zusammen das Problem diskutieren können.

> #### Info::Hinweis
> 
> Die Installation von CONFIRE SHOWTIME basiert auf der Windows-Installer-Technologie. Diese stellt eine Laufzeitumgebung (msiexec) zur Verfügung, mit der MSI-Pakete ausgeführt werden können.

[Support Team]: http://showtime.stueber.de/support.php