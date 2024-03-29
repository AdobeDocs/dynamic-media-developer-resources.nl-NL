---
description: De Server van het beeld verstrekt verscheidene alternatieven om tekst terug te geven, toegankelijk met text= en textPs= bevelen.
solution: Experience Manager
title: Tekstopmaak
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Tekstopmaak{#text-formatting}

De Server van het beeld verstrekt verscheidene alternatieven om tekst terug te geven, toegankelijk met text= en textPs= bevelen.

`textPs=` biedt een hoge mate van gelijkenis met tekst die wordt weergegeven met Adobe Photoshop en Illustrator. `text=` is redelijk compatibel met tekst die met WordPad van Vensters wordt teruggegeven.

>[!NOTE]
>
>Naast de elders genoemde verschillen, `text=` veroorzaakt subtiele verschillen in de gerenderde tekst in vergelijking met `textPs=`. onderstreept hebben bijvoorbeeld niet dezelfde dikte en positie en gesynthetiseerde cursief worden onder een iets andere hoek gerenderd. Als de tekst niet in de beschikbare ruimte past, `text=` kan de laatste regel gedeeltelijk uitsnijden, terwijl `textPs=` alleen volledige regels worden weergegeven.

Alle tekstopdrachten accepteren opgemaakte tekst die is gebaseerd op een subset van de RTF-specificatie (Rich Text Format). Elke tekstlaag kan een andere tekstopdracht opgeven.

In de volgende tabel worden de belangrijkste functies weergegeven die beschikbaar zijn voor elke tekstopdracht:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Functie</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Zie ook</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop-compatibel </p> </td> 
   <td> <p> nee </p> </td> 
   <td> <p> beperkt </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekst in willekeurige vormen laten doorlopen </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekst laten doorlopen langs willekeurige paden </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Kopiëren </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Aanpassen aan kopiëren <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Marges tekstvak </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Volledige uitvulling van alinea's </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>uitvulling laatste regel </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alinea-inspringing </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekst in kapitalen en kleinkapitalen </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Kleuren van afbeeldingsserver </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Meerdere anti-aliasingmodi </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>text flow top-bottom/right-left </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ondersteuning voor Photoshop® </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Fontverwerking </td> 
  </tr> 
  <tr> 
   <td> <p>Laag automatisch passend maken voor tekst </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK-ondersteuning </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekenstroom van rechts naar links </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekstomloop uitschakelen </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tekst automatisch schalen om laag te passen (door resolutie te variëren) </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nee </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-compatibele tekenreeksen kunnen handmatig worden samengesteld of door de gewenste tekst op te maken in een teksteditor of tekstverwerker die RTF-bestanden kan opslaan. Het RTF-bestand kan vervolgens worden geopend in een teksteditor zonder opmaak en de relevante Raw RTF-inhoud van het bestand wordt gekopieerd naar de aanvraag-URL.

Sommige tekstverwerkers genereren vrij grote bestanden, die aanzienlijke preambles bevatten die niet door Dynamic Media Image Serving worden gebruikt. Het wordt aanbevolen de ongebruikte RTF-elementen uit de tekenreeks te verwijderen voordat u de tekenreeks doorgeeft aan de tekstopdrachten.

Taalcodering op basis van UTF-8- en ISO-standaarden wordt ondersteund in RTF-tekenreeksen als alternatief voor de standaardcoderingsmechanismen voor RTF-tekens. Hierdoor kunnen toepassingen niet-Engelse tekst zonder RTF-codering naar de server verzenden.

Alle niet-HTTP-compatibele tekens moeten correct worden beschermd als de tekenreeks via http moet worden verzonden. Alleen &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; hoeven te worden beschermd als de tekenreeks in het `catalog::Modifiers` van een catalogusrecord in een afbeelding. Besturingstekens, inclusief `<CR>`, `<LF>`, en `<TAB>` moet altijd worden verwijderd.

De Image Serving text engines interpreteren een subset van opdrachten die zijn gedefinieerd in de RTF-specificatie (Rich Text Format), versie 1.6. Deze subset is gericht op lettertype-/tekenopmaak, eenvoudige alineaopmaak en ondersteuning voor internationale lettertypen en tekensets. Geavanceerde opmaakconstructies, zoals stijlpagina&#39;s en tabellen, worden momenteel niet ondersteund.

U moet de RTF-specificatie (Rich Text Format), die door Microsoft wordt gepubliceerd, kennen wanneer u met RTF-codering gecodeerde tekstreeksen handmatig wilt maken.

* [Fontverwerking](r-font-handling.md)
* [Kleurverwerking](r-color-handling.md)
* [Kopiëren](r-copy-fitting.md)
* [Tekstlagen](r-text-layers.md)
* [Tekstpositionering](r-text-positioning.md)
* [Gereserveerde tekens](r-reserved-characters.md)
* [Ondersteunde RTF-opdrachten en -trefwoorden](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Voorbeelden van RTF-codering](r-rtf-encoding-examples.md)
