# Automatisierung

Automatisierung bedeutet, bestimmte immer wiederkehrende Aufgaben von einem Computer völlig selbständig ausführen zu lassen. Im Folgenden werden Möglichkeiten beschrieben, wie Sie mit Hilfe von CONFIRE SHOWTIME bzw. den Boardmitteln von Windows einen Public Display-Computer vollständig automatisieren können.

## Automatische Anmeldung

[Microsoft Autologon](https://docs.microsoft.com/de-de/sysinternals/downloads/autologon) erlaubt Ihnen die Zugangsdaten eines belibigen Windows-Accounts (Lokal oder Domäne) zum automatischen Anmelden zu bestimmen. Weitere Informationen zu diesem Thema finden Sie [hier](autologon.md)

## Computer hochfahren

Sie haben folgende Optionen, einen Computer automatisch zu starten, ohne dass Sie explizit den Anschaltknopf drücken müssen.

### Wake on Power

Das Hochfahren des Computers sobald Strom fließt (Wake on Power) ist eine Einstellung, die von Ihrem BIOS unterstützt werden muss. Nutzen Sie unsere [CONFIRE E-BOARDS], ist diese Einstellung in der Regel schon voreingestellt. Weitere Details zu unseren CONFIRE E-BOARDS finden Sie in der [CONFIRE E-BOARD Dokumentation].

Der Vorteil von Wake on Power ist, dass in der ausgeschalteten Phase absolut kein Strom fließen muss.

### Wake on LAN

Das Hochfahren eines Computers kann auch durch einen dedizierten Netzwerkbefehl erfolgen (Wake on LAN). Dabei wird von einem aktiven Computer im Netzwerk ein kleines Datenpaket an die Netzwerkkarte des ausgeschalteten Computers gesendet. Dieser startet sich dann selbst. Wake on LAN ist ein Industriestandard und muss von der Netzwerkkarte unterstützt werden. 

Bei Wake on LAN wird der Computer nicht komplett ausgeschaltet, die Netzwerkkarte benötigt eine minimale Stromzufuhr, um auf Befehle reagieren zu können. 

### Wake on Standby

CONFIRE SHOWTIME unterstützt [Wake on Standby]. Sie können im Zeitplan eines Projektes eine Aufgabe definieren, welche das automatische Herunterfahren des Systems zu einem bestimmten Zeitpunkt festlegt. Optional können Sie für diese Aufgabe auch das Neustarten via Wake On Standby konfigurieren.

## Player starten

Ist der Computer hochgefahren, muss der CONFIRE SHOWTIME PLAYER gestartet und das passende Projekt ausgeführt werden. Auch dies lässt sich komplett automatisieren. Dazu stellen Sie im CONFIRE SHOWTIME PLAYER im Dialogfenster `Autostart-Einstellungen` ein, welches Projekt automatisch gestartet werden soll. Haben Sie dies gemacht, verhält sich CONFIRE SHOWTIME PLAYER beim nächsten Start des Computers wie folgt:

1. Unmittelbar nach dem Start von Windows wird der Player gestartet.

2. Das gewählte Projekt wird geladen.

3. Der diesem Projekt zugeordnete Showcase oder Zeitplan wird ausgeführt.

Weitere Details finden Sie im Kapitel [Player starten].

## Inhalte aktualisieren

Wird ein Projekt auf einem Public Display ausgeführt und ändert sich zwischenzeitlich der Inhalt des Projektes, kann der CONFIRE SHOWTIME PLAYER automatisch darauf reagieren:

1. Abonnieren Sie das Projekt, das Sie ausführen möchten.

2. Konfigurieren Sie, dass in regelmäßigen Abständen auf eine Aktualisierung des veröffentlichten Projektes geprüft werden soll.

Stellt der CONFIRE SHOWTIME PLAYER fest, dass sich das Projekt geändert hat, wird es automatisch im Hintergrund heruntergeladen und vorbereitet. War dieser Vorgang erfolgreich, beendet der Player das laufende Projekt und startet die aktuellere Version. 

Details zum Abonnieren von Projekten finden Sie im Kapitel [Projekte abonnieren], Details zum Publizieren von Projekten im Kapitel [Projekte publizieren].

## Computer herunterfahren

Um einen Computer automatisiert herunterzufahren, haben Sie in der Regel drei Möglichkeiten:

* Sie schalten den Strom für alle Computer zentral aus. 

* Sie richten in der Aufgabenverwaltung von Windows eine Aufgabe ein, die den Rechner zu einem bestimmten Zeitpunkt herunterfährt.

* Sie richten in CONFIRE SHOWTIME für das auf dem Public Display gezeigte Projekt einen Zeitplan ein, der u.a. eine Aufgabe zum Herunterfahren des Systems definiert. 

Der Vorteil der letzten Vorgehensweise ist, dass Sie das Herunterfahren des Systems bequem auf Ihrem Laptop konfigurieren können. Durch Publikation des Projektes werden auch die Einstellungen des Zeitplaners auf alle Public Displays verteilt. Zudem können Sie optional Wake on Stand By konfigurieren. 

Details zum Einrichten von Zeitplänen finden Sie im Kapitel [Zeitpläne verwalten].

[CONFIRE E-BOARDS]: http://eboard.stueber.de
[CONFIRE E-BOARD Dokumentation]: http://doc.eboard.stueber.de
[Wake on Standby]: ../simple-glossary.md#wakeonstandby
[Player starten]: ../howto/play-projects/start-player.md
[Projekte abonnieren]: ../howto/play-projects/subscribed-projects.md
[Projekte publizieren]: ../howto/publish-projects/README.md
[Zeitpläne verwalten]: ../howto/create-projects/manage-schedules/README.md