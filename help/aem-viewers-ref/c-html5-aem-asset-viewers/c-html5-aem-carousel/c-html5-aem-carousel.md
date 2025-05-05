---
title: Carousel
description: Carousel Viewer is een viewer die een carrousel van niet-zoombare bannerafbeeldingen weergeeft met klikbare hotspots of gebieden. Met deze viewer kunt u een "schokkende carrousel"-ervaring implementeren waarmee gebruikers een hotspot of een gebied boven de bannerafbeelding kunnen selecteren. Ze kunnen worden omgeleid naar een pagina met Quickview- of productdetails op de website van de klant. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1888'
ht-degree: 0%

---

# Carousel{#carousel}

Carousel Viewer is een viewer die een carrousel van niet-zoombare bannerafbeeldingen weergeeft met klikbare hotspots of gebieden. Met deze viewer kunt u een &quot;schokkende carrousel&quot;-ervaring implementeren waarmee gebruikers een hotspot of een gebied boven de bannerafbeelding kunnen selecteren. Ze kunnen worden omgeleid naar een pagina met Quickview- of productdetails op de website van de klant. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van Afbeeldingen renderen of Door de gebruiker gegenereerde inhoud (UGC) worden niet ondersteund door deze viewer.

Het viewertype is 511.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=nl-NL](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=nl-NL)

## Systeemvereisten {#section-b7270cc4290043399681dc504f043609}

Zie [Systeemvereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Carousel Viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

De Carousel Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload.

De Carousel Viewer kan zowel in pop-upmodus worden gebruikt met behulp van een voor productie geschikte HTML-pagina die bij IS Viewers wordt geleverd, als in ingesloten modus waarin deze met behulp van gedocumenteerde API in de doelwebpagina is geïntegreerd.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers die in deze Help worden beschreven. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Carousel Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

U kunt door de carrouselset navigeren met een horizontale veegbeweging over de hoofdweergave of met twee pijlknoppen op het desktopapparaat. De vastgestelde indicatorpunten tonen de huidige positie binnen de reeks.

De viewer kan hotspots of gebieden boven op de bannerafbeelding renderen om het interactieve gebied van het product aan te geven.

Wanneer u op een hotspot of gebied klikt of erop tikt, wordt tijdens de auteurstijd een bijbehorende handeling geactiveerd. De handeling kan worden omgeleid naar een andere pagina op de website of de productinformatie kan worden teruggestuurd naar de webpaginalogica, die op zijn beurt weer een QuickView met verwante productinhoud kan activeren.

De viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Carousel Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een uit-de-box HTML-pagina te gebruiken voor de pop-upbewerkingsmodus. In dit geval wordt `CarouselViewer.html` en bevindt zich binnen het `html5/` submap van uw standaard IS-Viewers-implementatie:

`<s7viewers_root>/html5/CarouselViewer.html`

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina. Deze webpagina heeft mogelijk al inhoud van een klant die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De meest gebruikte gevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Deze methode is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt aangepast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de lay-out van het Webontwerp zoals Bootstrap en Stichting gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`, vult de viewer alleen dat gebied. De pagina volgt ook de grootte die de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL CarouselViewer.js]. De [!DNL CarouselViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Alleen verwijzen naar de JavaScript-hoofdviewer `include` op uw pagina. Verwijs niet naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar HTML5 SDK `Utils.js` bibliotheek die door de viewer is geladen vanuit `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK) `include`). De reden is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken worden volledig beheerd door de logica van de viewer en de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet bij `includes` op de server.
>
>
>Hierdoor wordt een directe verwijzing naar secundaire JavaScript geplaatst `include` die door de viewer op de pagina worden gebruikt, verbreekt de viewerfunctionaliteit in de toekomst wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container definiëren `DIV`.

   Een leeg item toevoegen `DIV` aan de pagina waar u de kijker wilt verschijnen. De `DIV` De id van het element moet gedefinieerd zijn omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De tijdelijke aanduiding `DIV` is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerde plaatsaanduiding `DIV` element:

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de viewer instellen door deze te declareren voor `.s7carouselviewer` CSS-klasse op hoofdniveau in absolute eenheden of met gebruik van `stagesize` modifier.

   U kunt de grootte in CSS rechtstreeks op de pagina HTML plaatsen. Of u kunt de grootte in een aangepast CSS-bestand van de viewer plaatsen, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in AEM Assets - Op aanvraag, of expliciet wordt doorgegeven via het dialoogvenster `style` gebruiken.

   Zie [Carousel Viewer aanpassen](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte op de pagina HTML:

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   U kunt de `stagesize` modifier met de viewer-initialisatiecode met `params` verzameling of als API-aanroep zoals beschreven in de sectie Opdrachtverwijzing, als volgt:

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.CarouselViewer` klasse, alle configuratieinformatie tot zijn aannemer overgaan, en vraag `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` -tag of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze functionaliteit optreedt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan `carouselViewer` de viewer-instantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` is de URL van de afbeeldingsserver, en `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` is het actief:

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Carousel Viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In het volgende voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer toestaat `DIV` om 40% van het vensterformaat van de webbrowser te nemen. En de hoogte blijft onbeperkt. De HTML-code van de webpagina ziet er als volgt uit:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
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
1. De container definiëren `DIV`.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. De container toevoegen `DIV` de bestaande `"holder"` `DIV`. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=nl-NL](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=nl-NL)

**Flexibel formaat Insluiten met gedefinieerde breedte en hoogte**

In insluiten van flexibele grootte waarbij breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreer het in het browser venster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element aan 100 percenten.

```html {.line-numbers}
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

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Met deze API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met `setContainerId()`, `setParam()`, en `setAsset()` API-methoden met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting met een vaste grootte met de op een setter gebaseerde API geïllustreerd:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
