# Multimedia-Elemente

Mit Multimedia-Elementen können Sie einzelne Bilder, Bildsammlungen, Videos, Videossammlungen oder PDF-Seiten in einer Slideshow in einem Layout abspielen. Als Voraussetzung benötigen Sie eine Wiedergabeliste. 

## Eine Multimedia-Element hinzufügen

1. Klicken Sie auf `LAYOUTS > Multimedia`. Ein Dialogfenster öffnet sich.

   ![Eine Multimedia-Element hinzufügen](../../../images/create-multimedia-element.png)

3. Vergeben Sie einen aussagekräftigen Namen für das neue Layout-Element.

4. Wählen Sie eine passende Wiedergabeliste aus und bestätigen Sie mit `OK`.

Das neue Multimedia-Element wird nun im aktuellen Layout dargestellt. Per Drag & Drop können Sie Größe, Positionierung und Drehung beeinflussen.

## Eigenschaften eines Multimedia-Elements

Haben Sie ein Multimedia-Element in einem Layout mit der Maus markiert, werden Ihnen auf der rechten Seite alle Eigenschaften des Elements angezeigt.

Neben den für alle grafischen Elemente gleichen Eigenschaften können Sie für Multimedia-Elemente folgende Eigenschafgten konfigurieren:

Eigenschaft        | Bedeutung
------------------ | ---------
Ressource          | Verweis auf eine Wiedergabeliste
Lautsärke          | Lautstärke des Tons bei Videos
Stumm              | Sollen Videos ohne Ton abgespielt werden?
Endlossschleife    | Soll die Wiedergabeliste immer wieder von vorne anfangen? 
Visueller Übergang | Visueller Übergang beim Wechsel von Einträgen in der Wiedergabeliste 
Audioübergang      | Tonaler Übergang beim Wechsel von Einträgen in der Wiedergabeliste 

## Nachladefunktion externer Inhalte

Mit dem Einbetten externer Inhalte haben Sie die Möglichkeit Dokumente z.B. PDF-Dateien außerhalb von SHOWTIME zu ändern und die Inhalte aktualisieren sich auf dem Display, ohne im Designer nochmal veröffentlichen müssen.

Mit dem folgenden Javascript-Code auf dem Multimedia-Element können Sie sicher stellen, dass die Inhalte der Playlist regelmäßig aktualisiert werden:

````
var element = $(this);

$(".presentation").on("sht_layout_deactivate",function(){
    var layout = $(this);
    var multimediaContent = element.find(".multimediaContent");
    updateMultimediaContent(multimediaContent);
});
````

* Zunächst wählen Sie Ihr Multimedia-Element im linken Panel aus:

![Multimedia-Element auswählen](../../../images/multimedia.element.png)

* Im rechten Eigenschaftseditor klicken Sie auf die Schaltfläche mit den drei Punkten bei `Eigenes CSS`. Ein Dialogfenster öffnet sich.

![Eigenes CSS öffnen](../../../images/custom.javascript.png)

* Fügen Sie das o.g. Javascript ins Feld ein, anschließend klicken Sie auf `OK`.

![Öffnen Sie eigenes Javascript auf dem Multimedia-Element](../../../images/custom.javascript.insert.png)

Nach dem nächsten Publizieren bleiben Ihre extern verknüpfte Multimedia-Inhalte immer auf dem neusten Stand.

