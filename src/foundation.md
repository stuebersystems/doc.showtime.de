# Grundlagen

CONFIRE SHOWTIME besteht aus einem Designer und einem Player. Der Designer erstellt und bearbeitet Projekte, der Player liest diese Projekte und spielt die dort definierten Inhalte auf einem Display ab.

CONFIRE SHOWTIME ist ein dezentrales System, es benötigt keinen zentralen Applikationsserver und auch keine zentrale Datenbank. Selbst ein funktionierendes Netzwerk ist nicht zwingend notwendig (erleichtert allerdings die Arbeit).

## Projekte

Ein SHOWTIME-Projekt besteht aus mehreren Elementen:

* Einer Projektdatei mit der Dateiendung `.shtproj`
* Einem speziellen Projektordner, der alle im Projekt eingebetteten Ressourcen enthält

Die Projektdatei ist eine XML-Datei, in der Ressourcen, Layouts, Showcases und Zeitpläne definiert sind.  Ressourcen verweisen entweder auf eingebettete Dateien (als Teil des Projektes) oder auf externe Dateien (nicht Teil des Projektes)

## Projektarchive

Ein Projekt in seiner ursprünglichen Fassung ist nicht so einfach zu kopieren, denn es reicht nicht aus, nur die XML-Projektdatei zu kopieren. Es muss auch der Inhalt des korrespondierenden Projektordners beachtet werden. Aus diesem Grund gibt es Projektarchive. 

Ein Projektarchiv ist ein Zip-Archiv, das alle relevanten Dateien eines Projektes in einer komprimierten Datei zusammenfasst. Projektarchive haben die Dateiendung `.shtarc` und können problemlos kopiert oder als E-Mail verschickt werden.

Der CONFIRE SHOWTIME DESIGNER kann jedes Projekt auf Wunsch auch als Projektarchiv speichern. Umgekehrt kann er auch jedes Projektarchiv als Projekt einlesen. Auch der CONFIRE SHOWTIME PLAYER kann Projektarchive direkt öffnen.

Projektarchive sind übrigens auch das Publikationsformat für SHOWTIME-Projekte, d.h. jedes Mal wenn Sie ein Projekt mit CONFIRE SHOWTIME publizieren, wird technisch gesehen ein Projektarchiv erstellt.

## Ressourcen

Ressourcen sind Dateien, Dateigruppen, Ordner, Texte, Wiedergabelisten oder Datenbankverbindungen. Ressourcen bilden im strukturellen Aufbau eines Projektes die Basisebene.

Es können folgende Arten von Ressourcen definiert werden:

Art                 | Bedeutung
------------------- | ---------
Grafikdatei         | PNG-, JPEG-, GIF- oder Bitmap-Datei
Grafiksammlung      | Ein Ordner mit Grafikdateien
Videodatei          | WebM- oder MP4-Datei
Videosammlung       | Ein Ordner mit Videodateien
Audiodatei          | WebM- oder MP3-Datei
Audiosammlung       | Ein Ordner mit Audiodateien
SVG-Datei           | SVG-Datei
HTML-Seite          | Ein Ordner mit allen Dateien der HTML-Seite
PDF-Datei           | PDF-Datei
Text                | Markdown-formatierter Text
Wiedergabeliste     | Sequenz aus Grafiken, Videos, Audios und/oder PDF-Seiten
JSON-Datei          | JSON-Datei
XML-Datei           | XML-Datei
CSV-Datei           | CSV-Datei
Datenbankverbindung | Datenbankverbindung zu MS Access, MS SQL Server, PostgreSQL, Firebird, MySQL oder ODBC
Eigene App          | Ordner mit HTML-/CSS-/Javascript-Dateien

Dateibasierte Ressourcen werden unterschiedlich eingebunden:

* *Eingebettete Ressourcen* sind Ressourcen, deren Dateien Teil des Projekts sind. Beim Erstellen einer eingebetteten Ressource werden diese Dateien in einen speziellen mit dem Projekt verbundenen Systemordner kopiert. Publizieren Sie das Projekt oder speichern Sie das Projekt als Projektarchiv ab,  dann sind diese Dateien auch Teil der Publikation bzw. des Projektarchivs.

* *Externe Ressourcen* sind Ressourcen, deren Dateien lediglich durch einen Verweis eingebunden werden. Sie werden nicht kopiert und werden auch beim Publizieren oder Erstellen von Projektarchiven nicht berücksichtigt. Zu beachten ist dabei, dass der Pfad zu den Dateien bzw. Ordnern global im Netzwerk erreichbar sein muss. In der Regel werden externe Ressourcen in einem Netzwerkordner abgelegt und sind per UNC-Pfad (z.B. `\\MeinServer\MeinOrdner`) adressierbar.

Standardmäßig sollten Sie Ressourcen einbetten. Gründe für externe Ressourcen wären:

* Dateien bzw. Ordner, die Sie unabhängig vom Projekt ändern möchten. Beispiele hierfür wären Dateiinhalte, die sich regelmäßig ändern. Das Ändern einer externen Ressource hat den großen Vorteil, dass das entsprechende Projekt nicht neu publiziert werden muss.

* Dateien, deren Größe das Publizieren und Abonnieren unnötig in die Länge ziehen. Beispiele hierfür wären sehr große Videodateien oder große Bildsammlungen mit vielen hochauflösenden Fotos.

* Dateien, die von einem Benutzerkreis bearbeitet werden sollen, die keinen Zugriff auf das Projekt haben sollen.

Einige weitere Formate können per Konvertierung als Ressource integriert werden:

* Mircrosoft Office: Konvertierung von WinWord-Dokumenten und Powerpoint-Präsentationen als PDF-Ressource.

* OpenOffice/LibreOffice: Konvertierung von Writer-Dokumenten und Impress-Präsentationen als PDF-Ressource.

## Layouts

Layouts sind Designvorlagen für spätere Showcases. Layouts sind hierarchisch angeordnet, beginnend mit einem Masterlayout. Das Masterlayout definiert die Auflösung des Zielbildschirms (z.B. 1920 x 1080 Bildpunkte für Full-HD). Es können beliebig viele Masterlayouts in einem Projekt definiert werden. Jedes Masterlayout kann beliebig viele Unterlayouts enthalten. Jedes Unterlayout kann selbst wiederum beliebig viele Unterlayouts enthalten. In jedem Layout (Masterlayout oder Unterlayout) können Sie grafische Element erstellen und positionieren.  

Jedes grafische Element kann per Drag & Drop positioniert, in seiner Größe verändert oder durch Drehung in einem anderen Winkel dargestellt werden. Weitere Aspekte wie Farbe, Durchlässigkeit, Schriftart, Hintergrund, Rahmen und Abstände können bequem durch passende Editoren definiert werden.

Es stehen Ihnen folgende grafische Elemente zur Verfügung:

### Bilder

Bild-Elemente visualisieren Bild-Ressourcen, d.h. Sie können mit diesem Element PNGs, JPEGs, GIFs oder Bitmaps anzeigen. 

### Text

Text-Elemente visualisieren entweder Text-Ressourcen oder direkt eingegebenen Text. Mit Hilfe von Text-Ressourcen können Sie ein und denselben Text in unterschiedlichen Text-Elementen verwenden.

### Multimedia 

Multimedia-Elemente visualisieren Wiedergabelisten. Sie können damit also eine Sequenz von Bildern, Videos und/oder PDF-Seiten anzeigen. Mit Hilfe einer Wiedergabeliste könnnen Sie ein und dieselbe Sequenz in unterschiedlichen Multimedia-Elemente verwenden. 

### SVG   

SVG-Elemente visualisieren SVG-Ressourcen, d.h. Sie können mit diesem Element verktorbasierte Grafiken anzeigen, deren Qualität unabhängig von der Auflösung immer gleich bleibt. 

### Website

Website-Elemente visualisieren entweder HTML-Ressourcen oder eine direkt eingegebene URLs. Sie können also ganze Webseiten einbinden und deren Interaktivität zulassen oder unterbinden. 

### Shapes 

Shape-Elemente sind geometrische Elemente ohne Inhalt. Allerdings können sie wie jedes andere Element auch einen Hintergrund und einen Rahmen besitzen. Sie dienen zur grafischen Unterstützung. Beispielsweise können Sie mit einem Panel-Element einen bestimmten Layout-Bereich durch geschicktes Setzen von Farbe und Durchlässigkeit einfärben.

### Apps

Apps sind grafische Elemente mit beliebig komplexem Inhalt. Wir liefern aktuell die folgenden Apps mit:

Name           | Bedeutung
-------------- | ---------
Rss-Ticker     | Anzeige von Meldungen bzw. Nachrichten
Wetter         | Wetteranzeige
Uhr            | Zeitanzeige
DAVINCI-WEBBOX | Anzeige von DAVINCI-Stundenplänen, -Vertretungsplänen und -Gebäudeplänen

Darüber hinaus können Sie auch eigene Apps implementieren. Dazu benötigen Sie lediglich Kenntnisse in HTML/CSS/Javascript.

> Wir planen, zukünftig noch mehr Apps zu integrieren.

## Showcases und Szenen

Showcases definieren den zeitlichen Ablauf einer Präsentation von Layouts. Dazu wird jedem Showcase zunächst ein Masterlayout zugeordnet. Damit ist die Auflösung des Zielbildschirms definiert. Nun können innerhalb eines Showcases beliebig viele Szenen angelegt werden. Eine Szene verweist auf genau ein Layout aus der Layouthierarchie des Masterlayouts und definiert jeweils Dauer und Übergang der Layoutanzeige. Das Ergebnis ist eine Sequenz von Szenen. Die Summe der Spielzeiten aller Szenen ergibt die Dauer des Showcases.

Durch das Anlegen beliebig vieler Showcases mit jeweils unterschiedlichen Zielauflösungen können die Inhalte aller Public Displays in einem Projekt verwaltet werden. Und dabei können Ressourcen oder Layouts bei Bedarf auch noch gemeinsam genutzt werden. 

## Zeitpläne

Mit Zeitplänen können mehrere Showases aus einem Projekt zeitlich synchronisiert werden. Es kann auch das automatisierte Herunterfahren des Computers zeitlich verplant werden. Dazu werden Aufgaben erstellt, die mit einem zeitlichen Auslöser versehen werden. Dieser zeitliche Auslöser kann der Start des Projektes durch den Player sein (in diesem Fall wird die Aufgabe sofort gestartet) oder aber ein späterer Zeitpunkt, der durch gewohnte Zeitmuster (Datum, Uhrzeit sowie tägliche, wöchentliche oder monatliche Wiederholungen) definiert werden kann. 

Jeder Zeitplan kann beliebig viele Unterzeitpläne enthalten. Jeder Unterzeitplan kann selbst wiederum beliebig viele Unterzeitpläne enthalten. Dies erlaubt ein Gruppieren von Aufgaben bei größeren Zeitplänen.

Es stehen Ihnen folgende Aufgaben zur Verfügung:

### Showcase starten

Diese Aufgabe startet die Präsentation eines Showcases zu einem bestimmten Zeitpunkt.

### Zeitplan starten

Diese Aufgabe startet einen Unterzeitplan zu einem bestimmten Zeitpunkt. Es können nur Zeitpläne relativ  zum Zeitplan, in dem die Aufgabe definiert ist, gestartet werden.

### System herunterfahren

Diese Aufgabe fährt den Computer herunter. Dabei können Sie wählen, ob Sie den Computer komplett herunterfahren, in den Energiesparmodus wechseln oder in den Ruhezustand wechseln möchten. Optional können Sie festlegen, ob Sie den Wake On Stand By-Modus aktivieren möchten. Dieser Modus erlaubt es, Ihren Computer zu einem bestimmten Zeitpunkt wieder aufzuwecken, damit er selbständig startet.

> #### info::Wake On Stand By
>
> Wake On Stand By erlaubt es, einen ausgeschalteten Computer mit Hilfe der eingebauten Energieverwaltung zu starten. Dabei wird der Computer nicht komplett ausgeschaltet, sondern in einen speziellen Modus versetzt, der es ihm noch erlaubt auf elektronische Signale zu reagieren. Nicht jeder Computer unterstützt dies, die Funktion hängt also von dessen Hardware-Fähigkeiten ab. Wake On Stand By ist nicht zu verwechseln mit Wake On LAN, einer ähnlichen Technik, bei der das Startsignal durch einen externen Netzwerkbefehl ausgelöst wird.

## Projekte publizieren

Haben Sie alle Showcases und Zeitpläne definiert, können Sie Ihr Projekt auf Ihre Public Displays verteilen. Die einfachste Art und Weise dies zu tun ist es, ein Projekt zu publizieren.

Publizieren bedeutet in CONFIRE SHOWTIME ein Projektarchiv zu erstellen und dieses auf einem ausgewiesenen Ort im Netzwerk oder im Internet zu hinterlegen, damit ein oder mehrere Player darauf zugreifen können. Sollten alle Player über das lokale Netzwerk erreichbar sein, macht es Sinn, das Projekt in einem Netzwerkordner zu publizieren. Sollten Ihre Player sich jedoch auf mehrere Standorte verteilen, können Sie das Projekt im Internet publizieren. Dabei haben Sie mehrere Möglichkeiten:

* Publikation auf einem FTP-Server
* Publikation auf einem WebDAV-Server
* Publikation auf einem Cloud-Speicher (DropBox, Microsoft OneDrive oder Google Drive).

> #### primary::Hinweis
> 
> Alle von CONFIRE SHOWTIME unterstützten Cloud-Speicher setzen voraus, dass Sie ein eigenes Konto dort eröffnen, um sie zu nutzen. Die Nutzung dieser Dienste ist bis zu einer bestimmten Speicherobergrenze kostenlos. 

## Projekte abonnieren

Ein Player kann ein oder mehrere Projekte abonnieren. Abonnieren bedeutet, dass der Player in regelmäßigen Abständen überprüft, ob ein publiziertes Projekt sich geändert hat. Ist dies der Fall, wird es auf den Computer des Public Displays heruntergeladen und steht zur Verfügung. Sollte das abonnierte Projekt gerade auf dem Public Display angezeigt werden, wird es automatisch ausgewechselt. Mit anderen Worten: Haben Sie ein Projekt einmal abonniert und dann gestartet, werden alle Änderungen am Projekt ohne manuelles Eingreifen auf dem jeweiligen Public Display reflektiert.
