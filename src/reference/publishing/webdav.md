# WebDAV

WebDAV (Web-based Distributed Authoring and Versioning) ist eine Erweiterung des HTTP-Protokollstandards zum Bereitstellen und Organisieren von Dateien im Internet.

Zum Publizieren und Abonnieren per WebDAV benötigen Sie zunächst einen WebDAV-Server. Entweder können Sie auf einen bereits vorhanden WebDAV-Server zurückgreifen oder Sie müssen einen WebDAV-Server installieren. Bevor Sie dies tun, sollten Sie zunächst überprüfen, ob Sie nicht einen anderen bereits verfügbaren Publikationsort nutzen können:

* Dateiordner im Netzwerk
* FTP
* Cloud-Speicher (DropBox, Microsoft OneDrive, Google Drive)

Ist dies nicht der Fall, dann können Sie einen eignen WebDAV-Server aufsetzen. Aktuelle Windows-Server bringen einen eigenen WebDAV-Serverdienst von Hause aus mit. Sie müssen diese Funktion lediglich aktivieren. Möchten Sie beispielsweise einen WebDAV-Server unter Windows 2012 installieren, googlen Sie einfach "webdav windows server 2012 einrichten" für entsprechende Anleitungen.

Sie können einen WebDAV-Server aber auch unter Linux einrichten. 

Steht der WebDAV-Server bereit, können Sie publizieren bzw. abonnieren. In beiden Fällen, also sowohl im CONFIRE SHOWTIME DESIGNER als auch im CONFIRE SHOWTIME PLAYER, müssen Sie einmalig konfigurieren, wo sich Ihr WebDAV-Server befindet und wie auf ihn zugegriffen werden soll.

Dazu gehen Sie wie folgt vor:

1. Klicken Sie auf `Projekt > Publikationsziele verwalten > FTP- und WebDAV-Server`.

2. Klicken Sie auf `Hinzufügen`.

3. Vergeben Sie einen Namen für Ihren neuen Publikationsort und wählen Sie unter `Typ` die Angabe `Ordner auf einem WebDAV-Server`.

4. Geben Sie unter `Basis-URL` die URL ein, unter welcher der gewünschte Ordner zu erreichen ist.
   
   Beispiele:
   
   ```
   http://www.myserver.de
   http://www.myserver.de/shared
   http://192.168.0.21
   http://192.168.0.21/shared
   ```

5. Der Portangabe unter `Port` ist der Standard-Netzwerkport für das WebDAV-Protokoll. In der Regel gibt es keinen Grund diesen zu ändern. 

7. Ist der Zugriff geschützt, tragen Sie Benutzername und Kennwort ein.

8. Klicken Sie auf `WebDAV-Server überprüfen`, um den Zugriff auf den WebDAV-Server zu testen. 

9. War der Verbindungstest erfolgreich, klicken Sie auf `OK`. 


