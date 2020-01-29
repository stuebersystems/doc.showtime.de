# Microsoft OneDrive

OneDrive ist ein Internetdienst von Microsoft zum Verwalten und Freigeben von Dateien. Sie können sich unter http://www.onedrive.de kostenlos registrieren und danach sofort Dateien hochladen.

Sind Sie in OneDrive registriert, können Sie publizieren bzw. abonnieren. In beiden Fällen, also sowohl im CONFIRE SHOWTIME DESIGNER als auch im CONFIRE SHOWTIME PLAYER, müssen Sie einmalig den Zugriff auf Ihr Microsoft-Konto konfigurieren.

Dazu gehen Sie jeweils wie folgt vor:

1. Klicken Sie auf `Projekt > Publikationsziele verwalten > Cloud-Speicher`.

2. Klicken Sie auf `Hinzufügen`.

3. Vergeben Sie einen Namen für Ihren neuen Publikationsort und wählen Sie unter `Provider` die Angabe `OneDrive`.

4. Klicken Sie auf `Autorisieren`, um sich mit CONFIRE SHOWTIME bei OneDrive anzumelden. Es öffnet sich ein Dialogfenster. 

6. Melden Sie sich nun an Microsoft OneDrive an, indem Sie E-Mail und Kennwort eingeben and dann mit `Sign in` bestätigen. War die Anmeldung erfolgreich, können Sie CONFIRE SHOWTIME den Zugriff auf Ihr Microsoft-Konto erlauben.

7. Microsoft generiert nun einen Zugriffsschlüssel (Access-Token), der zukünftig den sicheren Zugriff auf OneDrive ohne manuelles Anmelden erlaubt.

8. Klicken Sie anschließend auf `OK`. 
   
Die gesamte Autorisierung erfolgt auf Basis des OAuth2-Standards. Bei einer erfolgreichen Anmeldung erzeugt Microsoft einen Access-Token und schickt diesen an CONFIRE SHOWTIME zurück. Ein Access-Token ist ein zeitlich beschränkter Schlüssel, der zukünftig zur Autorisierung mit OneDrive verwendet wird. Möchten Sie einen neuen Access-Token generieren, klicken Sie im Dialogfenster erneut auf `Autorisieren`.
