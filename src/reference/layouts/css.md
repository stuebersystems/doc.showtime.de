# CSS nutzen

Die gesamte grafische Ausgabe eines Layouts (inklusive der Layout-Elemente) basiert auf [HTML], [CSS] und [JavaScript]. Das bedeutet im Grunde genommen, dass Sie mit Hilfe von CONFIRE SHOWTIME Webseiten mit einem speziellem Verhalten erstellen. 

Auch wenn Sie alle Layout-Elemente per Drag & Drop positionieren und über die Eigenschaftseditoren des Layout-Designers viele Aspekte bequem einstellen können, so kontrollieren sie damit nur einen Bruchteil der grafischen Möglichkeiten. 

Wenn Sie CSS und/oder JavaScript als Hilfsmittel einsetzen, können Sie auf jedes Detail eines Layout-Elemente beliebig Einfluss nehmen. Dazu ein kleines Beispiel:

1. Erstellen Sie in einem Layout ein neues Textelement.

2. Tippen Sie einen beliebigen Text ein und stellen Sie Farbe, Schriftart und Hintergrund nach Ihren Wünschen ein.

3. Kopieren Sie nun die Angabe unter `Referenz-ID` in die Windows-Zwischenablage.

4. Öffnen Sie ím Eigenschaftseditor unter `Design > Eigenes CSS` den CSS-Editor.

5. Tippen Sie dort die folgende CSS-Sequenz ein:
   
   ```` css
   #text-73D1AECD-1D83-45A9-B421-B5558A2C9DC6 {
      text-shadow: 10px 10px 5px grey
   }
   ````

   Ersetzen Sie dabei die beispielhafte Angabe `#text-73D1AECD-1D83-45A9-B421-B5558A2C9DC6` mit der soeben kopierten Referenz-ID.

6. Klicken Sie auf `OK`.

Der Text in Ihrem Textelement hat jetzt einen Schatten bekommen. Wie ist das möglich? Nun, Sie haben soeben eine CSS-Deklaration für das HTML-Element mit der ID `text-73D1AECD-1D83-45A9-B421-B5558A2C9DC6` hinterlegt. Und diese CSS-Deklaration legt fest, dass ein Textschatten mit einem horizontalen und vertikalen Versatz von jeweils 10px, einer Breite von 5px für den Weichzeichner sowie der Farbe grau ausgegeben werden soll.

Gehen wir noch einen Schritt weiter: Unser Text mit Schatten soll auch noch blinken. Ersetzen Sie die bisherige CSS-Deklaration mit dieser hier:

```` css
#text-73D1AECD-1D83-45A9-B421-B5558A2C9DC6 {
   text-shadow: 10px 10px 5px grey;
   -webkit-animation-name: blinker;
   -webkit-animation-duration: 0.5s;
   -webkit-animation-iteration-count: infinite;
   -webkit-animation-timing-function: ease-in-out;
   -webkit-animation-direction: alternate;
}

@-webkit-keyframes blinker {
  from {opacity: 1.0;}
  to {opacity: 0.0;}
}
````

Sie werden sehen, Ihr Text blinkt jetzt fröhlich vor sich hin.

Wenn Sie Lust auf mehr haben, empfehlen wir folgende Vorgehensweise:

1. Frischen Sie Ihre Kenntnisse in CSS auf bzw. erlernen Sie CSS. Es existieren unzählige Einführungen im Web. Einfach mal nach den Begriffen `CSS Einführung` suchen. Eine umfassende Referenz zu CSS (allerdings in Englisch) finden sie unter http://www.w3schools.com/css. 

2. Inspizieren Sie mit Hilfe der Entwicklerkonsole unter `Ansicht > Entwicklerkonsole` (oder durch Drücken auf `F12`) die HTML-Struktur des aktuellen Layouts. So bekommen Sie ein besseres Gefühl für den inneren Aufbau eines Layouts. Zudem können Sie in der Entwicklerkonsole direkt mit den CSS-Einstellungen rumspielen

3. Überlegen Sie sich, welchen Effekt Sie gerne umsetzen möchten und versuchen Sie dies mit CSS zu realisieren.

Auch CSS hat natürlich seine Grenzen, und sobald diese erreicht sind, kommt JavaScript ins Spiel. Mit JavaScript können Sie so ziemlich alle Wünsche umsetzen, da Sie hier im Gegensatz zu CSS eine richtige Programmiersprache nutzen können.

[HTML]: ../../simple-glossary.md#html
[CSS]: ../../simple-glossary.md#css
[JavaScript]: ../../simple-glossary.md#js