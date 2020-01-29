# Markdown

Mit Hilfe von Text-Elementen können Sie Text zu einem Layout hinzufügen. Standardmäßig hat dieser Text eine Schriftart, eine Farbe, eine Größe und einen Stil. CONFIRE SHOWTIME unterstützt allerdings auch einen einfachen Auszeichnungssyntax, mit desen Hilfe man Texte formatieren kann. Dieser Syntax ist unter dem Namen *Markdown* bekannt.

## Einführung

Markdown erlaubt es, Texte durch das Einfügen von Leerzeilen, Leerzeichen, Sonderzeichen sowie das Einrücken von Absätzen so auszuzeichnen, dass ein HTML-Generator daraus einen strukturierten Text erstellen kann. Lesbarkeit des Originaltextes ist hierbei das oberste Ziel, der Autor muss kein Wissen über HTML haben. 

Ein kleines Beispiel: Der folgende Text in Markdown

````
Dies ist ein **fetter Text**.
````

wird in HTML wie folgt umgesetzt:

````
Dies ist ein <strong>fetter Text</strong>.
````

Das Beispiel zeigt, dass durch das Angabe von `\*\*` am Anfang und `\*\*` am Ende einer Textpassage eine HTML-Ausgabe erzwungen wird, in der dieser Textteil als stark betont ausgezeichnet wird.

Im Folgenden beschreiben wir die wichtigsten Aspekte von Markdown aus Sicht von CONFIRE SHOWTIME.

## Blockelemente

### Absätze und Zeilenumbrüche

Ein Absatz besteht einfach aus einer oder aus mehreren Zeilen von Text, abgetrennt durch eine oder mehrere leere Zeilen. (Eine leere Zeile ist jede Zeile die aussieht wie eine leere Zeile -- eine Zeile die nichts anderes enthält als Leerzeichen und Tabs wird als leer behandelt.) Normale Absätze sollten nicht mit Leerzeichen oder Tabs eingerückt sein.

Die "eine oder mehrere Zeilen"-Regel impliziert eine Sache: Markdown unterstützt Absätze mit "harten Umbrüchen". Dies ist ein großer Unterschied zu den meisten anderen Text-zu-HTML-Formatierern (inklusive der "Convert Line Breaks" Option von Movable Type), die jeden Zeilenumbruch in einem Absatz als &lt;br /&gt; formatieren.

Wenn man ein &lt;br /&gt; als Umbruch haben will, kann man die Zeile einfach mit zwei oder mehr Leerzeichen beenden.

Dies ist zwar ein kleiner Mehraufwand um ein &lt;br /&gt; zu erzeugen, aber eine einfache "jeder Zeilenumbruch ist ein &lt;br /&gt;" Regel würde in Markdown nicht funktionieren.

### Kopfzeilen

Markdown unterstützt zwei Arten von Kopfzeilen-Formatierung, Setext und atx.

Setext-artige Kopfzeilen werden mit Gleichheitszeichen (für Überschriften erster Ebene) und Bindestrichen (für die zweite Ebene) "unterstrichen". Zum Beispiel:

````
Dies ist ein H1
===============

Dies ist ein H2
---------------
````

Eine beliebige Zahl von = oder - funktioniert.

Atx-artige Kopfzeilen verwenden 1-6 Rauten-Zeichen am Anfang der Zeile, entsprechend den Ebenen 1-6. Zum Beispiel:

````
# Dies ist ein H1

## Dies ist ein H2

###### Dies ist ein H6
````

Wenn gewünscht können atx-artige Kopfzeilen auch "geschlossen" werden. Dies ist nur Kosmetik -- es kann genutzt werden wenn es besser aussieht. Die Zahl der schließenden Rauten-Zeichen muss nicht einmal der Zahl der öffnenden Zeichen entsprechen.

````
# Dies ist ein H1 #

## Dies ist ein H2 ##

### Dies ist ein H3 ######
````

### Listen

Markdown unterstützt sortierte (nummerierte) und unsortierte Listen (Aufzählungen).

Unsortierte Listen benutzen Sternchen, Plus und Bindestriche -- austauschbar -- als Listen-Marker:

````
*   Rot
*   Grün
*   Blau
````

ist gleich:

````
+   Rot
+   Grün
+   Blau
````

Und:

````
-   Rot
-   Grün
-   Blau
````

Sortierte Listen verwenden Zahlen mit darauf folgendem Punkt:

````
1.  Hund
2.  Katze
3.  Maus
````

Hierbei ist es wichtig zu verstehen, dass die Zahlen selber keine Auswirkung auf den Output von Markdown hat. Markdown erstellt aus der letzten Liste folgenden HTML-Code:

````
<ol>
  <li>Hund</li>
  <li>Katze</li>
  <li>Maus</li>
</ol>
````

Wenn man die Liste statt dessen so schreibt:

````
1.  Hund
1.  Katze
1.  Maus
````

Oder sogar:

````
3. Hund
1. Katze
8. Maus
````

kommt trotzdem jedes Mal die gleiche Liste heraus. Wenn gewünscht, kann man seine Listen von Hand richtig nummerieren. Aber wer faul sein will, kann getrost immer die gleiche Ziffer benutzen.

Allerdings sollte man auch dann die Liste mit der Nummer 1 beginnen. In Zukunft wird Markdown vielleicht eine Startziffer für den ersten Listeneintrag festlegen wollen.

Listeneinträge beginnen normalerweise am linken Rand des Dokuments, sie können jedoch bis zu drei Leerzeichen nach Rechts eingerückt sein. Listen-Marker müssen mit ein oder mehr Leerzeichen oder einem Tab vom folgenden Text getrennt werden.

Um Listen schön zu formatieren, können die einzelnen Einträge weiter eingerückt werden, so wie hier:

````
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.
````

Das folgende Beispiel generiert den gleichen Code, ist aber weniger aufgeräumt:

````
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.
````

Wenn Listeinträge durch Leerzeilen getrennt sind, wird Markdown die Listeneinträge mit &lt;p&gt; und &lt;/p&gt; umhüllen.

Zum Beispiel wird dies:

````
*   Warsteiner
*   König
````

zu

````
<ul>
  <li>Warsteiner</li>
  <li>König</li>
</ul>
````

Aber dies:

````
*   Warsteiner

*   König
````

wird zu

````
<ul>
  <li><p>Warsteiner</p></li>
  <li><p>König</p></li>
</ul>
````

Listenpunkte können aus mehreren Absätzen bestehen. Jeder folgende Absatz in einem Listenpunkt muss mit mindestens 4 Leerzeichen oder einem Tab eingerückt werden:

````
1.  Dies ist eine Listenpunkt mit zwei Absätzen. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.
````

Es sieht gut aus wenn jede Zeile des folgenden Absatzes eingerückt ist, aber wieder erlaubt Markdown dem Faulen, nur die erste Zeile einzurücken:

````
*   Dies ist ein Listenpunkt mit zwei Absätzen

    Dies ist der zweite Absatz in diesem Listenpunkt. Nur die
erste Zeile muss eingerückt sein. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit.

*   Ein weiterer Punkt in der selben Liste.
````

Es ist möglich Listen unabsichtlich zu erstellen, indem man z.B. folgendes schreibt:

````
1986. Was für ein wundervolles Jahr.
````

Mit anderen Worten: Die Sequenz Zahl-Punkt-Leerzeichen am Anfang einer Zeile. Um dieses Problem zu vermeiden kann der Punkt per Backslash maskiert werden:

````
1986\. Was für ein wundervolles Jahr.
````

### Horizontale Linien

Der Tag für horizontale Linien (&lt;hr /&gt;) kann generiert werden indem 3 oder mehr Bindestriche oder Sternchen allein auf einer Zeile geschrieben werden. Leerzeichen zwischen den Zeichen sind auch erlaubt. Alle folgenden Beispiele würden eine horizontale Linie generieren:

## Betonung

Markdown behandelt Sternchen (\*) und Unterstriche (\_) als Indikatoren für Betonung. In einzelne \* oder \_ gepackter Text wird mit dem HTML-Tag &lt;em&gt; umschlossen, doppelte \* oder \_ werden mit dem Tag &lt;strong&gt; markiert. Folgender Text zum Beispiel:

````
*Einzelne Sternchen*
_Einzelne Unterstriche_
**Doppelte Sternchen**
__Doppelte Unterstriche__
````

Wird folgendes ausgeben:

````
<em>Einzelne Sternchen</em>
<em>Einzelne Unterstriche</em>
<strong>Doppelte Sternchen</strong>
<strong>Doppelte Unterstriche</strong>
````

Der Stil kann beliebig gewählt werden. Die einzige Begrenzung ist, dass das gleiche Zeichen zum Öffnen und Schließen eines Betonungs-Bereiches verwendet werden muss.

Betonung kann inmitten eines Wortes verwendet werden:

````
Herr*gott*sakrament
````

Aber wenn ein \* oder \_ von Leerzeichen umgeben ist, wird es wie ein einfaches Sternchen oder ein einfacher Unterstrich behandelt.

Um ein Sternchen oder einen Unterstrich zu schreiben an einer Stelle wo er als Betonung verstanden würde, kann er mit einem Backslash maskiert werden:

````
\*Dieser Text ist von Sternchen umschlossen.\*
````

## Backslash-Maskierung

Markdown ermöglicht es, Backslash-Maskierung zu nutzen um Zeichen zu schreiben, die sonst eine bestimmte Bedeutung in Markdowns Syntax haben. Wenn man zum Beispiel ein Wort mit Sternchen umgeben will (statt dem HTML-Tag &lt;em&gt;), kann man Backslashes vor die Sternchen stellen:

````
\*Von Sternchen umgeben\*
````

Markdown bietet diese Möglichkeit für folgende Zeichen:

````
\   Backslash
`   Backtick
*   Sternchen
_   Unterstrich
{}  Geschweifte Klammern
[]  Eckige Klammern
()  Runde Klammern
#   Raute
+   Plus-Zeichen
-   Minus-Zeichen (Bindestrich)
.   Punkt
!   Ausrufezeichen
````


## Schlussbemerkung

Diese Einführng in Markdown basiert auf Texten von Lasar Liepins auf seiner Seite http://markdown.de. Dort finden Sie auch eine vollständige Beschreibung des Markdown-Syntaxes.
