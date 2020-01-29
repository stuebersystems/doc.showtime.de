# Layouts

Layouts sind der komplexeste Aspekt eines CONFIRE SHOWTIME Projekts. Mit einem Layout legen Sie fest, was die einzelnen Szenen eines Showcases anzeigen sollen. 

Layouts werden hierarchisch definiert. Die oberste Hierarchieebene bilden sogenannte Masterlayouts, die sich in zwei Punkten von anderen Layouts unterscheiden:

* Sie besitzen kein Elternlayout

* Sie definieren die Zielauflösung des Bildschirms für sich selbst und für alle ihre Unterlayouts.

Die Menge aller Layouts bildet also eine baumartige Hierarchie:

````
Masterlayout
-- Layout 1
   -- Layout 1.1   
   -- Layout 1.2
-- Layout 2
   -- Layout 2.1   
   -- Layout 2.2
-- Layout 3
   -- Layout 3.1   
   -- Layout 3.2
````

Auf jedem Layout (auch auf einem Masterlayout) können Layout-Elemente frei positioniert werden. Die folgenden Layout-Elemente stehen zurzeit zur Verfügung:

* Bild-Element
* Text-Element
* Multimedia-Element
* SVG-Element
* Website-Element
* Panel-Element
* App-Elemente

Auf folgende Aspekte von Layouts soll näher eingegangen werden:

* [Bildschirmauflösungen](multi-resolutions.md)
* [Markdown](markdown.md)
* [CSS nutzen](css.md)
* [RSS nutzen](rss.md)
