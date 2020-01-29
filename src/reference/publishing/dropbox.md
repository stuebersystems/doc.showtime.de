# DropBox

Dropbox ist ein Internetdienst zum Verwalten und Freigeben von Dateien. Sie können sich unter https://www.dropbox.com kostenlos registrieren und danach sofort Dateien hochladen.

Besitzen Sie ein DropBox-Konto, können Sie publizieren bzw. abonnieren. In beiden Fällen, also sowohl im CONFIRE SHOWTIME DESIGNER als auch im CONFIRE SHOWTIME PLAYER, müssen Sie einmalig den Zugriff auf Ihr DropBox-Konto konfigurieren.

Dazu gehen Sie jeweils wie folgt vor:

1. Klicken Sie auf `Projekt > Publikationsziele verwalten > Cloud-Speicher`.

2. Klicken Sie auf `Hinzufügen`.

3. Vergeben Sie einen Namen für Ihren neuen Publikationsort und wählen Sie unter `Provider` die Angabe `DropBox`.

4. Klicken Sie auf `Autorisieren`, um sich mit CONFIRE SHOWTIME an ein DropBox-Konto anzumelden. Es öffnet sich ein Dialogfenster. 

5. Melden Sie sich nun an DropBox an, indem Sie E-Mail und Kennwort eingeben and dann mit `Sign in` bestätigen. War die Anmeldung erfolgreich, können Sie CONFIRE SHOWTIME den Zugriff auf Ihr DropBox-Konto erlauben.

6. DropBox generiert nun einen Zugriffsschlüssel (Access-Token), der zukünftig den sicheren Zugriff auf DropBox ohne manuelles Anmelden erlaubt.

7. Klicken Sie anschließend auf `OK`. 
   
Die gesamte Autorisierung erfolgt auf Basis des OAuth2-Standards. Bei einer erfolgreichen Anmeldung erzeugt DropBox einen Access-Token und schickt diesen an CONFIRE SHOWTIME zurück. Ein Access-Token ist ein zeitlich beschränkter Schlüssel, der zukünftig zur Autorisierung mit DropBox verwendet wird. Möchten Sie einen neuen Access-Token generieren, klicken Sie im Dialogfenster erneut auf `Autorisieren`.
