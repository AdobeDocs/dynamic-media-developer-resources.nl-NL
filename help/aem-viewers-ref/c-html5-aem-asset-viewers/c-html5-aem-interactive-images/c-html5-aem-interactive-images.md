---
description: Interactive Image Viewer is een viewer die één niet-zoombare afbeelding met aanklikbare hotspots weergeeft. Het doel van deze viewer is het implementeren van een 'shoppable banner'-ervaring. Met andere woorden, de gebruiker kan een hotspot boven de bannerafbeelding selecteren en worden omgeleid naar een pagina in de Snelle weergave of de productdetails op uw website. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-description: Interactive Image Viewer is een viewer die één niet-zoombare afbeelding met aanklikbare hotspots weergeeft. Het doel van deze viewer is het implementeren van een 'shoppable banner'-ervaring. Met andere woorden, de gebruiker kan een hotspot boven de bannerafbeelding selecteren en worden omgeleid naar een pagina in de Snelle weergave of de productdetails op uw website. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-title: Interactieve afbeelding
solution: Experience Manager
title: Interactieve afbeelding
topic: Dynamic media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---


# Interactieve afbeelding{#interactive-image}

Interactive Image Viewer is een viewer die één niet-zoombare afbeelding met aanklikbare hotspots weergeeft. Het doel van deze viewer is het implementeren van een &#39;shoppable banner&#39;-ervaring. Met andere woorden, de gebruiker kan een hotspot boven de bannerafbeelding selecteren en worden omgeleid naar een pagina in de Snelle weergave of de productdetails op uw website. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud), worden niet ondersteund door deze viewer.

Het viewertype is 508.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Systeemvereisten {#section-b7270cc4290043399681dc504f043609}

Zie [Systeemvereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Interactieve afbeeldingsviewer {#section-e6c68406ecdc4de781df182bbd8088b4} gebruiken

Interactive Image Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand bevat alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload.

Interactive Image Viewer kan alleen worden gebruikt in de ingesloten modus, waar deze met de gedocumenteerde API is geïntegreerd in de doelwebpagina.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers die in deze Help worden beschreven. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Interactive Image Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Interactie die wordt ondersteund door de Video Image Viewer is activering van hotspots op desktopsystemen. Deze activering vindt plaats op klikapparaten en op aanraakapparaten met één tik.

De viewer is volledig toegankelijk via het toetsenbord.

Zie [Toegankelijkheid en navigatie op toetsenbord](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Interactieve afbeeldingsviewer {#section-6bb5d3c502544ad18a58eafe12a13435} insluiten

Interactive Image Viewer is ontworpen om te worden ingesloten in de hostpagina. Een dergelijke webpagina kan een statische lay-out hebben of kan &quot;responsief&quot; zijn en anders worden weergegeven op verschillende apparaten of voor verschillende venstergrootten in de browser.

Om aan deze behoeften tegemoet te komen, ondersteunt de viewer twee primaire bewerkingsmodi: insluiten met een vaste grootte en responsieve insluiting.

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina. Deze webpagina heeft mogelijk al inhoud van een klant die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De meest gebruikte gevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container `DIV` door de webpagina wordt verkleind. Als de webpagina alleen de breedte van de container `DIV` instelt en de hoogte onbeperkt laat, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval komt het meest voor voor Web-pagina&#39;s die ontvankelijke kaders van de Webontwerp lay-out zoals Bootstrap, Stichting, etc. gebruiken.

Als de webpagina anders zowel de breedte als de hoogte voor de container `DIV` van de viewer instelt, vult de viewer alleen dat gebied. De pagina volgt ook de grootte die de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container `DIV` definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Voordat u de viewer-API kunt gebruiken, moet u [!DNL InterativeImage.js] opnemen. Het [!DNL InteractiveImage.js]-bestand bevindt zich in de submap [!DNL html5/js/] van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Klassieke Adobe Dynamic Media-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop de IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Verwijs alleen naar het JavaScript-bestand `include` van de hoofdviewer op de pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK `Utils.js`-bibliotheek die door de viewer is geladen vanaf het contextpad `/s7viewers` (de zogeheten geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer `includes` niet op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript `include` op de pagina plaatst, wordt de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container `DIV` definiëren.

   Voeg een leeg `DIV` element aan de pagina toe waar u de kijker wilt verschijnen. Voor het element `DIV` moet de id zijn gedefinieerd omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding `DIV` is een gepositioneerd element, wat betekent dat de CSS-eigenschap `position` is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding `DIV`-element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7interactiveimage` top-level CSS klasse in absolute eenheden te verklaren, of door `stagesize` bepaling te gebruiken.

   U kunt de grootte in CSS rechtstreeks op de HTML-pagina plaatsen, of in een aangepast CSS-bestand van de viewer, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in AEM Assets, op aanvraag, of expliciet wordt doorgegeven met de opdracht `style`.

   Zie [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in de HTML-pagina:

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   U kunt expliciet de `stagesize` bepaling met de de initialisatiecode van de kijker met `params` inzameling of als API vraag overgaan zoals die in de sectie van de Verwijzing van het Bevel wordt beschreven, als dit:

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt voltooid, maakt u een instantie van de klasse `s7viewers.InteractiveImage`, geeft u alle configuratiegegevens door aan de constructor ervan en roept u `init()` methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens `containerId` veld hebben met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval moet voor het `params`-object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl`-eigenschap en het eerste element als `asset`-parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de methode `init()` aan vlak voor de afsluitingstag `BODY` of op de hoofdgebeurtenis `onload()`.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld worden verborgen met de stijl `display:none` die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de methode `init()`. In het voorbeeld wordt ervan uitgegaan dat `interactiveImage` de viewerinstantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` is de URL van de afbeeldingsserver en `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` is het element:

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Video Image Viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer `DIV` bepaalt. In het volgende voorbeeld gaat u ervan uit dat de webpagina de container `DIV` van de viewer 40% van de venstergrootte van de webbrowser laat innemen. En de hoogte blijft onbeperkt. De HTML-code van de webpagina ziet er als volgt uit:

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
1. De container `DIV` definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Voeg de container `DIV` aan bestaande `"holder"` `DIV` toe. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Wanneer u deze API-constructor gebruikt, worden geen parameters gebruikt en worden configuratieparameters opgegeven met de API-methoden `setContainerId()`, `setParam()` en `setAsset()` met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting met een vaste grootte met de op een setter gebaseerde API geïllustreerd:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```

