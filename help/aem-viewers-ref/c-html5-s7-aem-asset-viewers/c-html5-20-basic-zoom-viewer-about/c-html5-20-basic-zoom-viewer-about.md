---
description: De standaardzoomviewer is een afbeeldingsviewer die één zoombare afbeelding weergeeft. Deze heeft zoomgereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Deze viewer is de lichtste. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsief
seo-description: De standaardzoomviewer is een afbeeldingsviewer die één zoombare afbeelding weergeeft. Deze heeft zoomgereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Deze viewer is de lichtste. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-title: Standaardzoom
solution: Experience Manager
title: Standaardzoom
uuid: 5466d647-af70-4503-9898-bb712ba6a007
feature: Dynamic Media Classic,Viewers,SDK/API,Zoomen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 0%

---


# Standaardzoom{#basic-zoom}

De standaardzoomviewer is een afbeeldingsviewer die één zoombare afbeelding weergeeft. Deze heeft zoomgereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Deze viewer is de lichtste. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 501.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## De standaardzoomviewer {#section-e6c68406ecdc4de781df182bbd8088b4} gebruiken

De Basic Zoom Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand bevat alle SDK-componenten van de viewer die door deze viewer worden gebruikt, elementen, CSS) die de viewers tijdens runtime downloaden.

U kunt de standaard zoomviewer in de pop-upmodus gebruiken met behulp van een voor productie geschikte HTML-pagina die wordt geleverd met IS-Viewers of in de ingesloten modus, waar deze wordt geïntegreerd in de doelwebpagina met behulp van gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met de standaardzoomviewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De standaardzoomviewer ondersteunt de volgende aanraakbewegingen die ook in andere mobiele toepassingen worden gebruikt.

Wanneer de viewer de veegbeweging van een gebruiker niet kan verwerken, stuurt deze de gebeurtenis door naar de webbrowser om een native paginaschuiving uit te voeren. Met dit soort functionaliteit kan de gebruiker door de pagina navigeren, zelfs als de viewer het grootste deel van het schermgebied van het apparaat in beslag neemt.

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
   <td colname="col2"> <p>Hiermee verbergt of onthult u elementen van de gebruikersinterface. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dubbeltikken </p> </td> 
   <td colname="col2"> <p> Hiermee zoomt u in op één niveau totdat de maximale vergroting is bereikt. Met de volgende dubbele tikbeweging wordt de viewer opnieuw ingesteld op de eerste weergavestatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kneep </p> </td> 
   <td colname="col2"> <p>Hiermee zoomt u in of uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Veeggebaar </p> </td> 
   <td colname="col2"> <p> Als de afbeelding is hersteld, wordt door de beweging een eigen paginaschuiving uitgevoerd. </p> <p> Wanneer u op de afbeelding hebt ingezoomd, wordt de afbeelding verplaatst. Als de afbeelding naar de weergaverand wordt verplaatst en een veegbeweging in die richting wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toegankelijkheid en navigatie op toetsenbord](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Standaardzoomviewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling die de viewer in een apart browservenster opent wanneer erop wordt geklikt. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk ontwerp het inbedden.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van het apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met de JavaScript-aanroep `window.open()`, het HTML-element op de juiste wijze geconfigureerd `A` of een andere geschikte methode.

Het wordt aanbevolen een HTML-pagina uit de doos te gebruiken voor de pop-upbewerkingsmodus. In dit geval wordt deze [!DNL BasicZoomViewer.html] genoemd en bevindt deze zich in de submap [!DNL html5/] van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container `DIV` door de webpagina wordt verkleind. Als de webpagina alleen de breedte van de container `DIV` instelt en de hoogte onbeperkt laat, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het element dat wordt gebruikt. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval komt het meest voor voor Web-pagina&#39;s die ontvankelijke kaders van de Webontwerp lay-out zoals Bootstrap, Stichting, etc. gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container `DIV` van de kijker plaatst, vult de kijker enkel dat gebied en volgt de grootte die de Web-pagina lay-out verstrekt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Voordat u de viewer-API kunt gebruiken, moet u [!DNL BasicZoomViewer.js] opnemen. Het [!DNL BasicZoomViewer.js] dossier wordt gevestigd onder [!DNL html5/js/] subfolder van uw standaard plaatsing IS-Viewers:

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Klassieke Adobe Dynamic Media-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop de IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>U moet alleen verwijzen naar het JavaScript-bestand `include` van de hoofdviewer op uw pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK `Utils.js`-bibliotheek die door de viewer is geladen vanaf het contextpad `/s7viewers` (de zogeheten geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer `includes` niet op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript `include` op de pagina plaatst, wordt de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de CSS-eigenschap `position` is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7basiczoomviewer` top-level CSS klasse in absolute eenheden te verklaren, of door `stagesize` bepaling te gebruiken.

   U kunt de grootte in CSS rechtstreeks op de HTML-pagina plaatsen, of in een aangepast CSS-bestand van de viewer, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in Dynamic Media Classic, of expliciet wordt doorgegeven met behulp van een stijlopdracht.

   Zie [De standaardzoomviewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in HTML-pagina:

   ```
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt de `stagesize` bepaling of in de kijker vooraf ingestelde verslag in Classic van Dynamic Media plaatsen, of het uitdrukkelijk met de kijker- initialisatiecode met `params` inzameling, of als API vraag zoals die in de sectie van de Verwijzing van het Bevel wordt beschreven, als het volgende overgaan:

   ```
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt voltooid, maakt u een instantie van de klasse `s7viewers.BasicZoomViewer`, geeft u alle configuratiegegevens door aan de constructor ervan en roept u `init()` methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens een ContainerId-veld hebben met de naam van de viewer `container ID` en een genest `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval moet voor het `params`-object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl`-eigenschap en het eerste element als `asset`-parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de methode `init()` aan vlak voor de afsluitingstag `BODY` of op de hoofdgebeurtenis `onload()`.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld worden verborgen met de stijl `display:none` die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de methode `init()`. In het voorbeeld wordt ervan uitgegaan dat `basicZoomViewer` de viewerinstantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; `http://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver en `Scene7SharedAssets/Backpack_B` is het element:

   ```
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Basic Zoom Viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer `DIV` bepaalt. In het volgende voorbeeld gaat u ervan uit dat de webpagina de container `DIV` van de viewer 40% van de venstergrootte van de webbrowser laat nemen, zodat de hoogte onbeperkt blijft. De HTML-code van de webpagina ziet er als volgt uit:

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

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met de stappen voor het insluiten van een vaste grootte. Het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Voeg de container DIV aan bestaande `"holder"` DIV toe. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexibel formaat Insluiten met gedefinieerde breedte en hoogte**

In het geval van insluiting van flexibele grootte met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreert het in het browser venster. Bovendien stelt de webpagina de grootte van het element `HTML` en `BODY` in op 100 procent.

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

De overige insluitingsstappen zijn identiek aan de stappen die worden gebruikt voor het insluiten van responsieve lagen met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Wanneer u deze API-constructor gebruikt, worden geen parameters gebruikt en worden configuratieparameters opgegeven met de API-methoden `setContainerId()`, `setParam()` en `setAsset()` met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting op vaste grootte met een setter-API geïllustreerd:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```

