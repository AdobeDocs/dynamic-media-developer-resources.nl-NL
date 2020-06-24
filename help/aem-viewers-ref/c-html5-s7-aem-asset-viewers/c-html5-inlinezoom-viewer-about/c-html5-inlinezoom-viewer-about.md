---
description: Inline Zoom Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die boven die statische afbeelding wordt weergegeven wanneer een gebruiker de hoofdweergave beweegt of aanraakt. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsive
seo-description: Inline Zoom Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die boven die statische afbeelding wordt weergegeven wanneer een gebruiker de hoofdweergave beweegt of aanraakt. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-title: Inline zoomen
solution: Experience Manager
title: Inline zoomen
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---


# Inline zoomen{#inline-zoom}

Inline Zoom Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die boven die statische afbeelding wordt weergegeven wanneer een gebruiker de hoofdweergave beweegt of aanraakt. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Het viewertype is 504.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Inline zoomviewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

Inline zoomviewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer bij uitvoering zijn gedownload.

De inline zoomviewer kan zowel in de pop-upmodus worden gebruikt met behulp van voor productie geschikte HTML-pagina&#39;s die worden geleverd met Image Serving Viewers, als in de ingesloten modus waarin deze is geïntegreerd in een doelwebpagina met behulp van gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. U kunt aangepaste CSS gebruiken om skins toe te passen.

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met de Inline Zoom Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Inline Zoom Viewer ondersteunt Single-touch en multi-touch bewegingen die ook in andere mobiele toepassingen voorkomen.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Enkele tik </p> </td> 
   <td colname="col2"> <p> Hiermee activeert u de flyoutweergave of wijzigingen tussen het primaire en het secundaire zoomniveau in stalen en selecteert u nieuwe miniaturen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Hiermee bladert u door de lijst met stalen in de staalbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal veeggebaar </p> </td> 
   <td colname="col2"> <p>Als de beweging binnen het stalengebied wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Inline zoomviewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een klikbare koppeling waarmee de viewer in een apart browservenster wordt geopend. In andere gevallen kan het nodig zijn de viewer rechtstreeks in te sluiten in de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of een responsief ontwerp dat op verschillende apparaten anders wordt weergegeven, of voor verschillende venstergrootten in de browser. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk inbedden.

**Pop-up**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan wanneer de grootte van het browservenster wordt gewijzigd of de apparaatoriëntatie wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met behulp van `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte manier.

Het wordt aanbevolen de HTML-pagina uit de doos te gebruiken voor de pop-upmodus `FlyoutViewer.html`. Het bevindt zich in de [!DNL html5/] submap van uw standaardimplementatie van Image Serving-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

Het is ook noodzakelijk om de component FlyoutZoomView te hebben die wordt gevormd om op de gealigneerde gezoemwijze te werken. U wordt aangeraden de `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` voorinstelling voor de weergave Inline zoomen te gebruiken, of een aangepaste voorinstelling die hiervan is afgeleid. Visuele aanpassing kan worden bereikt door aangepaste CSS toe te passen.

Hieronder ziet u een HTML-codevoorbeeld waarmee de viewer in een nieuw venster wordt geopend:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Vaste grootte insluiten en responsieve insluiting**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het vastgoed van een webpagina in beslag.

Het primaire gebruiksgeval zijn webpagina&#39;s die zijn georiënteerd op desktops of tabletapparaten, en ook responsieve webpagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluitingsmodus met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt nadat de viewer voor het eerst is geladen. Deze optie is het meest geschikt voor webpagina&#39;s met een statische pagina-indeling.

Bij de insluitingsmodus voor responsief ontwerp wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

Wanneer u responsieve ontwerpinsluitmodus gebruikt met de Inline Zoom Viewer, moet u expliciete onderbrekingspunten opgeven voor de hoofdweergaveafbeelding met de `imagereload` parameter. In het ideale geval past u uw onderbrekingspunten aan met de breedteonderbrekingspunten van de viewer die door de CSS van de webpagina worden voorgeschreven.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van een webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Dit betekent dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit specifieke gebruiksgeval komt het meest voor bij webpagina&#39;s die responsieve ontwerplay-outframeworks gebruiken, zoals Bootstrap, Foundation, enzovoort.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt, vult de viewer alleen dat gebied `DIV`en volgt deze het formaat dat wordt aangegeven door de indeling van de webpagina. Een voorbeeld van een nuttig geval is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Zorg ervoor dat u de viewer-API opneemt voordat u deze kunt gebruiken `FlyoutViewer.js`. `FlyoutViewer.js` bevindt zich in de volgende [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

U kunt een relatieve weg gebruiken als de kijker op één van de servers van Adobe Scene7 wordt opgesteld en het van het zelfde domein wordt gediend. Anders, specificeert u een volledige weg aan één van de servers van Adobe Scene7 die de IS-Kijkers hebben geïnstalleerd.

Een relatief pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>U moet alleen verwijzen naar het JavaScript- `include` hoofdviewerbestand op uw pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK- `Utils.js` bibliotheek die door de viewer is geladen vanuit het `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet `includes` op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript dat door de viewer op de pagina wordt `include` gebruikt, maakt u de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. De id van het DIV-element moet worden gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Het is de verantwoordelijkheid van de webpagina om de juiste waarde `z-index` voor het plaatsaanduidings-DIV-element op te geven. Zo zorgt u ervoor dat het vervolggedeelte van de viewer boven op de andere webpagina-elementen wordt weergegeven.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. De viewergrootte instellen.

   In deze viewer worden miniaturen weergegeven wanneer u werkt met sets met meerdere items. Op desktopsystemen worden miniaturen onder de hoofdweergave geplaatst. Tegelijkertijd kan de viewer het hoofdelement tijdens runtime wisselen met behulp van de `setAsset()` API. Als ontwikkelaar hebt u controle over de manier waarop de viewer het miniatuurgebied in het onderste gebied beheert wanneer het nieuwe element slechts één item bevat. Het is mogelijk de grootte van de buitenste viewer ongewijzigd te laten en de hoogte van de hoofdweergave te verhogen en het gebied met miniaturen in beslag te nemen. U kunt ook de grootte van de hoofdweergave statisch houden en het buitenste viewergebied samenvouwen, waarbij de inhoud van de webpagina omhoog wordt verplaatst en vervolgens het bestand met de openstaande pagina-inhoud van de miniaturen wordt gebruikt.

   Als u de buitenste grenzen van de viewer ongewijzigd wilt laten, definieert u de grootte van de CSS-klasse op het `.s7flyoutviewer` hoogste niveau in absolute eenheden. De grootte in CSS kan worden gezet recht op de HTML- pagina, of in een douaneCSS dossier van de kijker, dat later aan een kijker vooraf ingesteld verslag in het Publiceren Scene7 Systeem wordt toegewezen, of uitdrukkelijk wordt overgegaan gebruikend stijlbevel.

   Zie [Inline zoomviewer](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van de statische buitenste viewergrootte in een HTML-pagina:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt het gedrag met een vast buitenste viewergebied op de volgende voorbeeldpagina zien. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   Als u de afmetingen van de hoofdweergave statisch wilt maken, definieert u de viewergrootte in absolute eenheden voor de binnenste `Container` SDK-component met behulp van `.s7flyoutviewer .s7container` CSS-kiezer. Daarnaast moet u de vaste grootte die is gedefinieerd voor de CSS-klasse op het `.s7flyoutviewer` hoogste niveau in de standaard viewer-CSS negeren door deze in te stellen op `auto`.

   Hieronder ziet u een voorbeeld van het definiëren van de viewergrootte voor de binnenste `Container` SDK-component, zodat de grootte van het hoofdweergavegebied niet verandert wanneer u van element verandert:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Op de volgende voorbeeldpagina ziet u het gedrag van de viewer met een vaste hoofdweergavegrootte. Wanneer u tussen sets schakelt, blijft de hoofdweergave statisch en wordt de inhoud van de webpagina verticaal verplaatst:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   Houd er ook rekening mee dat de CSS van de standaardviewer een vaste grootte biedt voor het buitenste gebied.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.FlyoutViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens het `containerId` veld hebben met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die de viewer ondersteunt. In dit geval moet voor het `params` object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl` eigenschap, het eerste element als `asset` parameter, het basispad voor het laden van CSS als `contentUrl` parameter en de naam van de voorinstelling als `config` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Roep voor maximale compatibiliteit de `init()` methode aan vlak voor de afsluitende `BODY` tag of voor de body- `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met een `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan dat `inlineZoomViewer` de viewer-instantie is; `s7viewer` de naam van de plaatsaanduiding `DIV`; `http://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver; en `Scene7SharedAssets/ImageSet-Views-Sample` is het actief:

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Inline Zoom-viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsief ontwerpinsluiting met onbeperkte hoogte {#section-056cb574713c4d07be6d07cf3c598839}

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In het volgende voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer 40% van de venstergrootte van de webbrowser laat `DIV` afnemen, waarbij de hoogte onbeperkt blijft. De HTML-code van de webpagina ziet er als volgt uit:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met de stappen voor het insluiten van een vaste grootte. Het enige verschil is dat u de vaste grootte van de standaardviewer-CSS moet overschrijven met de grootte die is ingesteld in relatieve eenheden.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan de stappen voor de insluiting van een vaste grootte, met de volgende drie uitzonderingen:

* de container toevoegen `DIV` aan de bestaande &quot;houder&quot; `DIV`;
* toegevoegde `imagereload` parameter met expliciete onderbrekingspunten;
* in plaats van een vaste viewergrootte in te stellen met absolute eenheden gebruikt u CSS die de viewer instelt `width` en `height` op 100% instelt als in het volgende:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Flexibele insluiting van grootte met gedefinieerde breedte en hoogte {#section-0a329016f9414d199039776645c693de}

In het geval van insluiting van flexibele grootte met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. Het verstrekt zowel grootte aan `"holder"` DIV als centreert het in het browser venster. Bovendien stelt de webpagina de grootte van het element `HTML` en het `BODY` element in op 100 procent.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

De overige insluitingsstappen zijn identiek aan de stappen die worden gebruikt voor responsieve ontwerpinsluiting met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Insluiten met behulp van op Setter gebaseerde API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Het gebruik van deze API-constructor heeft geen invloed op parameters en configuratieparameters die zijn opgegeven met `setContainerId()`, `setParam()`en `setAsset()` API-methoden, met aparte JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting op vaste grootte met een setter-API geïllustreerd:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```

