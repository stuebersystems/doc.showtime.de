# Energie sparen

Hier zeigen wir Ihnen wie Sie das Ein- und Ausschalten Ihres Public Displays automatisieren lassen. Betrachten wir als Beispiel verwenden die Betriebszeit **Montag bis Samstag 7 Uhr - 20 Uhr** und stellen dazu einen [Giada Rechner](https://doc.eboard.stueber.de/setup-computer/Giada-D67-N1/) und [NEC P553](https://www.nec-display-solutions.com/p/de/de/support/productsupport/rp/P553.xhtml) ein. Im Grunde genommen wird der Rechner per SHOWTIME [Zeitplan](/howto/create-projects/manage-schedules/README.md) herunterfahren. Wenn anschließend kein Bildsignal vom Rechner anliegt, wechselt der Bildschirm in den Energiesparmodus.

# Zeitplan im Designer erstellen

Um mit Zeitplänen arbeiten zu können, müssen Sie in der linken Navigationsleiste des Designers auf `Zeitpläne` klicken.

![Die Zeitpläne-Ansicht im Designer](/images/designer-schedules.png)

Zuallererst erstellen Sie einen neuen Zeitplan:

1. Klicken Sie `Zeitplan` oben links. Ein Dialogfenster öffnet sich.

2. Vergeben Sie einen Namen für Ihren neuen Zeitplan z.B. 'Mein Zeitplan' und bestätigen Sie mit `OK`.

Nun erstellen Sie vier Aufgaben wie unten abgebildet:

![](/images/Zeitplan.png)

## Aufgabe 1: Showcase starten

1. Klicken Sie auf `Aufgabe > Showcase starten`. Ein Dialogfenster öffnet sich.

2. Vergeben Sie einen Namen für die Aufgabe z.B. **Showcase starten**.

3. Wählen Sie den gewünschten `Showcase` aus und bestätigen Sie mit `OK`.

![](/images/Showcase_zuweisen.png)

## Aufgabe 2: Herunterfahren (Mo bis Fr Abend)

1. Klicken Sie auf `Aufgabe > Energie sparen / Aufwachen`. Ein Dialogfenster öffnet sich.

2. Vergeben Sie einen Namen für die Aufgabe z.B. **Herunterfahren (Mo bis Fr Abend)** und bestätigen Sie mit `OK`.

![](/images/aufgabe1-Mo-bis-Fr-Abend.png)

* Unter `Startparameter` der Aufgabe wählen Sie folgende Optionen aus:

![](/images/herunterfahren-Mo-bis-Fr-Abend.png)

## Aufgabe 3: Energie sparen (Sa bis Mo)

1. Klicken Sie auf `Aufgabe > Energie sparen / Aufwachen`. Ein Dialogfenster öffnet sich.

2. Vergeben Sie einen Namen für die Aufgabe z.B. **Energie sparen (Sa bis Mo)**.

3. Bearbeiten Sie den `Auslöser`. Wichtig sind folgende Zeiteinstellungen:

![](/images/Standby-Sa-bis-Mo.png)

* Bestätigen Sie beide Dialogfenster mit `OK`.

* Unter `Startparameter` der Aufgabe wählen Sie folgende Optionen aus:

![](/images/wakeup-montag.png)

## Aufgabe 4: Herunterfahren (Mo früh)

1. Klicken Sie auf `Aufgabe > Energie sparen / Aufwachen`. Ein Dialogfenster öffnet sich.

2. Vergeben Sie einen Namen für die Aufgabe z.B. **Herunterfahren (Mo früh)**.

3. Bearbeiten Sie den `Auslöser`. Wichtig sind folgende Zeiteinstellungen:

![](/images/Auslöser_Montag.png)

* Bestätigen Sie beide Dialogfenster mit `OK`.

* Unter `Startparameter` der Aufgabe wählen Sie folgende Optionen aus:

![](/images/herunterfahren-Mo-bis-Fr-Abend.png)

# Aufwecken im BIOS einstellen

Unter der Option `Wake system from RTC` im BIOS kann man eine Uhrzeit einstellen, zu der, das System täglich hochgefahren wird d.h. 7 Uhr.

Diese Option befindet sich in der Regel unter der Registerkarte `Advanced` und `Wake system from RTC` Ihres Rechners.

![](/images/BIOS_Giada-D67-N1_RTC-Wake.jpg)

Die meisten modernen Computer unterstützen einen Zeitgeber. Unsere Industriecomputer unterstützen dies auch. Falls Ihr Computer die notwendige Fähigkeit nicht besitzt, [setzen Sie sich mit uns in Verbindung](https://www.stueber.de/contact.php) und wir unterstützen Sie gerne beim Kauf eines Industriecomputers.

# Energiesparmodus am Bildschirm einstellen

Die meisten Monitore wechseln automatisch in den Energiesparmodus und kehren zurück in den Normalmodus, sobald wieder ein Signal anliegt, ohne den Modus aktivieren zu müssen.

Bei Bildschirmen von NEC stellen Sie sich sicher, dass Sie unsere empfohlene Einstellungen für die [P/V/X-Series](https://doc.eboard.stueber.de/tips/NEC-Bildschirm-einrichten/#pvx-series) (z.B. P553/V463/X551S) und [E-Series](https://doc.eboard.stueber.de/tips/NEC-Bildschirm-einrichten/#e-series) (z.B. E506) beachtet haben.

# Den Zeitplan im Player auswählen

1. Im Player klicken Sie in der linken Navigationsleiste auf `Projekte`, falls Sie die Ansicht Projekte nicht sehen.

2. Markieren Sie nun das gewünschte Projekt und klicken Sie auf `Ausführen`. Ein Dialogfenster öffnet sich.

3.  Wählen Sie den gewünschten `Zeitplan` aus und bestätigen Sie mit `Übernehmen`.

![](/images/einen-zeitplan-ausfuehren.png)

# Autostart im Player einstellen

Damit der Player das Projekt nach dem Neustart automatisch startet:

1. Im Player klicken Sie auf `Umgebung > Autostart-Einstellungen`. Ein Dialogfenster öffnet sich.

2. Unter `Projekt automatisch ausführen` wählen Sie Ihr Projekt aus und bestätigen Sie mit `OK`:

![](/images/Autostart-Einstellungen.png)

# Automatische Anmeldung

Bei einer Domäne bzw. bei passwortgeschützten lokalen Windows-Accounts muss ein Benutzername und ein Kennwort beim Startup eingegeben werden.

[Microsoft Autologon](https://docs.microsoft.com/de-de/sysinternals/downloads/autologon) erlaubt Ihnen die Zugangsdaten eines beliebigen Windows-Accounts (Lokal oder Domäne) zum automatischen Anmelden zu bestimmen. Daten werden in der Windows-Registierung verschüsselt, um den angegebenen Benutzer anzumelden.

Die Bedienung von Autologon ist ganz einfach:

* Führen Sie die `autologon.exe` aus

* Füllen Sie das Dialogfenster aus. Befindet sich der Computer in einer Domäne, geben Sie den Namen der Domäne im Feld `Domain` ein. Wenn es sich um einen lokalen Windows-Account handelt, geben Sie den Computernamen auch im Feld `Domain` ein. 

* Um Autologon zu deaktivieren, wählen Sie `Disable`.

![](/images/autologin.jpg)





