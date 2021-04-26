# RSS nutzen

[RSS] ist ein XML-Format zum Speichern von Nachrichten. Wird RSS zum Lesen bereitgestellt, spricht man auch von einem RSS-Feed. Die RSS-Ticker-App von CONFIRE SHOWTIME kann diese RSS-Feeds lesen und anzeigen. Dabei ergeben sich zwei Möglichkeiten:

1. Sie konsumieren einen öffentlichen RSS-Feed (beispielsweise von einer Nachrichten-Webseite)

2. Sie erstellen sich einen eigenen RSS-Feed und publizieren Ihre eigenen Nachrichten und Meldungen.

## Erstellen eines RSS-Feeds

Gehen Sie wie folgt vor:

1. Öffnen Sie den Windows-Editor (oder einen anderen Texteditor) und erzeugen Sie eine neue leere Datei.

2. Kopieren Sie diesen XML-Textblock in den Texteditor:
   
```` xml
   <?xml version="1.0" encoding="UTF-8" ?>
   <rss version="2.0">
     <channel>
       <title>Meine Nachrichten</title>
       <item>
         <title>Abschlußfeier in der Aula</title>
         <description>Heute um 16:15 findet in der Aula die Abschlußfeier statt.</description>
       </item>
       <item>
         <title>Morgen ist schulfrei</title>
         <description>Morgen findet kein Unterricht an unserer Schule statt.</description>
       </item>
     </channel>
   </rss>
````

3. Ändern Sie den Inhalt nach Ihren Wünschen ab. Für zusätzliche Einträge kopieren Sie den `item`-Knoten so oft wie nötig.

4. Speichern Sie die Datei in einem Netzwerkordner.

5. Im RSS-Ticker-Element geben Sie unter `URL` eine Datei-URL ein. Zum Beispiel:
   
   ````
   file:///\\myserver\feeds\nachrichten.xml
   ````

Mehr brauchen Sie über RSS nicht zu wissen. Wenn Sie dennoch einen ausführlicheren Überblick über das RSS-Format bekommen möchten, empfiehlt sich das entsprechende Kapitel auf [w3schools.com](http://www.w3schools.com/xml/xml_rss.asp).

## RSS-Feed-URLs

Um einen RSS-Feed in der RSS-Ticker-App einzubinden müssen Sie eine URL eintippen. Mit einer URL können Sie Web-Adressen aber auch lokale Dateien und Dateien im lokalen Netzwerk adressieren.

Beispiel für eine Web-URL:

````
http://www.tagesschau.de/xml/rss2
````

Beispiel für eine lokale Datei:

````
file:///c:\feeds\nachrichten.xml
````

Beispiel für eine Datei im lokalen Netzwerk:

````
file:///\\myserver\feeds\nachrichten.xml
````

[RSS]: ../../simple-glossary.md#rss