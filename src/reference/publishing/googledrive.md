# Google Drive

Google Drive ist ein Internetdienst von Google zum Verwalten und Freigeben von Dateien. Sie können sich unter https://www.google.com/intl/de_de/drive kostenlos registrieren und danach sofort Dateien hochladen.

Sind Sie in Google Drive registriert, können Sie publizieren bzw. abonnieren. In beiden Fällen, also sowohl im CONFIRE SHOWTIME DESIGNER als auch im CONFIRE SHOWTIME PLAYER, müssen Sie einmalig den Zugriff auf Ihr Google-Konto konfigurieren.

Dazu gehen Sie jeweils wie folgt vor:

1. Klicken Sie auf `Projekt > Publikationsziele verwalten > Cloud-Speicher`.

2. Klicken Sie auf `Hinzufügen`.

3. Vergeben Sie einen Namen für Ihren neuen Publikationsort und wählen Sie unter `Provider` die Angabe `Google Drive`.

4. Klicken Sie auf `Autorisieren`, um sich mit CONFIRE SHOWTIME bei Google Drive anzumelden. Es öffnet sich ein Dialogfenster. 

5. Melden Sie sich nun an Google Drive an, indem Sie Ihre E-Mail eingeben, auf `Next` klicken, danach  Ihr Kennwort eingeben and dann mit `Sign in` bestätigen. War die Anmeldung erfolgreich, können Sie CONFIRE SHOWTIME den Zugriff auf Ihr Google-Konto erlauben.

6. Google generiert nun einen Zugriffsschlüssel (Refresh-Token), der zukünftig den sicheren Zugriff auf Google Drive ohne manuelles Anmelden erlaubt.

8. Klicken Sie anschließend auf `OK`. 
   
Die gesamte Autorisierung erfolgt auf Basis des OAuth2-Standards. Bei einer erfolgreichen Anmeldung erzeugt Google einen Refresh-Token und schickt diesen an CONFIRE SHOWTIME zurück. Ein Refresh-Token ist ein zeitlich beschränkter Schlüssel, der zukünftig zur Autorisierung mit Google Drive verwendet wird. Möchten Sie einen neuen Refresh-Token generieren, klicken Sie im Dialogfenster erneut auf `Autorisieren`.
