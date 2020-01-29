# FTP

Das File Transfer Protocol (kurz FTP) ist ein recht altes aber immer noch populäres Netzwerkprotokoll zur Übertragung von Dateien über IP-Netzwerke. 

Zum Publizieren und Abonnieren per FTP benötigen Sie zunächst einen FTP-Server. Entweder können Sie auf einen bereits vorhanden FTP-Server zurückgreifen oder Sie müssen einen FTP-Server installieren. Bevor Sie dies tun, sollten Sie zunächst überprüfen, ob Sie nicht einen anderen bereits verfügbaren Publikationsort nutzen können:

* Dateiordner im Netzwerk
* WebDAV
* Cloud-Speicher (DropBox, Microsoft OneDrive, Google Drive)

Ist dies nicht der Fall, dann können Sie einen eignen FTP-Server aufsetzen. Windows-Server bringen einen eigenen FTP-Serverdienst von Hause aus mit. Sie müssen diese Funktion lediglich aktivieren. Möchten Sie beispielsweise einen FTP-Server unter Windows 2012 installieren, googlen Sie einfach "ftp windows server 2012 einrichten" für entsprechende Anleitungen.

Sie können einen FTP-Server aber auch unter Linux einrichten. 

Steht der FTP-Server bereit, können Sie publizieren bzw. abonnieren. In beiden Fällen, also sowohl im CONFIRE SHOWTIME DESIGNER als auch im CONFIRE SHOWTIME PLAYER, müssen Sie einmalig konfigurieren, wo sich Ihr FTP-Server befindet und wie auf ihn zugegriffen werden soll.

Dazu gehen Sie wie folgt vor:

1. Klicken Sie auf `Projekt > Publikationsziele verwalten > FTP- und WebDAV-Server`.

2. Klicken Sie auf `Hinzufügen`.

3. Vergeben Sie einen Namen für Ihren neuen Publikationsort und wählen Sie unter `Typ` die Angabe `Ordner auf einem FTP-Server`.

4. Geben Sie unter `Basis-URL` die URL ein, unter welcher der gewünschte Ordner zu erreichen ist.
   
   Beispiele:
   
   ```
   ftp://ftp.myserver.de
   ftp://ftp.myserver.de/shared
   ftp://192.168.0.21
   ftp://192.168.0.21/shared
   ```

5. Der Portangabe unter `Port` ist der Standard-Netzwerkport für das FTP-Protokoll. In der Regel gibt es keinen Grund diesen zu ändern. 

6. Entfernen Sie die Option `Passiver Übertragungsmodus`, wenn Sie eine aktive Übertragung wünschen. Erfahrungsgemäß macht ein passiver Übertragungsmodus aber weniger Probleme.

7. Ist der Zugriff geschützt, entfernen Sie die Option `Anonym anmelden` und tragen Sie Benutzername und Kennwort ein.

8. Klicken Sie auf `FTP-Server überprüfen`, um den Zugriff auf den FTP-Server zu testen. 

9. War der Verbindungstest erfolgreich, klicken Sie auf `OK`. 


