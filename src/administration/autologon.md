# Automatische Anmeldung

Es ist eine häufige Nachfrage, dass der Windows-PC des E-Boards sich Abends automatisch [herunterfährt und Morgens hochfährt](/howto/create-projects/manage-schedules/shutdown-system.md). Bei einer Domäne und Kennwort geschützten lokalen Windows-Accounts muss ein Benutzername und ein Kennwort beim Startup eingegeben werden.

[Microsoft Autologon](https://docs.microsoft.com/de-de/sysinternals/downloads/autologon) erlaubt Ihnen die Zugangsdaten eines belibigen Windows-Accounts (Lokal oder Domäne) zum automatischen Anmelden zu bestimmen. Daten werden in der Windows-Registierung verschüsselt, um den angegebenen Benutzer anzumelden.

Die Bedienung von Autologon ist ganz einfach:

* Führen Sie die `autologon.exe` aus

* Füllen Sie das Dialogfenster aus. Befindet sich der Computer in einer Domäne geben Sie den Namen der Domäne im Feld `Domain` ein. Wenn es sich um einen lokalen Windows-Account handelt, geben Sie den Computernamen auch im Feld `Domain` ein. 

* Um Auto-Logon zu deaktivieren wählen Sie `Disable`.

![](/images/autologin.jpg)

