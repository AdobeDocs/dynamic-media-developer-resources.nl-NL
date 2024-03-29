---
title: Zoomen
description: Zoomviewer is een afbeeldingsviewer waarin een afbeelding wordt weergegeven waarop kan worden ingezoomd. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Deze heeft zoomgereedschappen, ondersteuning voor volledig scherm, stalen en een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2393'
ht-degree: 0%

---

# Zoomen{#zoom}

Zoomviewer is een afbeeldingsviewer waarin een afbeelding wordt weergegeven waarop kan worden ingezoomd. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Deze heeft zoomgereedschappen, ondersteuning voor volledig scherm, stalen en een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 502.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Zoomviewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

Zoom Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload.

U kunt de Kijker van het Gezoem op pop-up wijze gebruiken gebruikend een productie-klaar HTML pagina die van IS-Kijkers of op ingebedde wijze wordt voorzien, waar het in doelWeb-pagina gebruikend gedocumenteerde API wordt geïntegreerd.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Zoomviewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De zoomviewer ondersteunt de volgende aanraakbewegingen die ook in andere mobiele toepassingen worden gebruikt. Wanneer de viewer de veegbeweging van de gebruiker niet kan verwerken, stuurt deze de gebeurtenis door naar de webbrowser om een native paginaschuiving uit te voeren. Met dit soort functionaliteit kan de gebruiker door de pagina navigeren, zelfs als de viewer het grootste deel van het schermgebied van het apparaat in beslag neemt.

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
   <td colname="col2"> <p> Hiermee selecteert u nieuwe miniaturen in stalen. In de hoofdweergave worden elementen van de gebruikersinterface verborgen of weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dubbeltikken </p> </td> 
   <td colname="col2"> <p> Hiermee zoomt u in op één niveau totdat de maximale vergroting is bereikt. Met de volgende dubbele tikbeweging wordt de viewer opnieuw ingesteld op de eerste weergavestatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kneep </p> </td> 
   <td colname="col2"> <p>Zoomt in of uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Hiermee bladert u door de lijst met stalen in de staalbalk. </p> <p> Als de afbeelding zich in een herstelstatus bevindt en de <span class="codeph"> frametransition </span> De parameter is ingesteld op dia, het element wordt gewijzigd met de dia-animatie. Voor andere <span class="codeph"> frametransition </span> , voert de beweging native paginaschuiven uit. </p> <p> Als in de afbeelding wordt ingezoomd, wordt de afbeelding horizontaal verplaatst. Als de afbeelding naar de weergavegrens wordt verplaatst en een veegbeweging in dezelfde richting wordt uitgevoerd, wordt native paginaschuiven uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal veeggebaar </p> </td> 
   <td colname="col2"> <p> Als de status van de afbeelding opnieuw is ingesteld, wordt door de beweging native paginaschuiven uitgevoerd. </p> <p> Als u op de afbeelding hebt ingezoomd, wordt de afbeelding verticaal verplaatst. Als de afbeelding naar de weergaverand wordt verplaatst en een veegbeweging in dezelfde richting wordt uitgevoerd, wordt de native paginaschuiving uitgevoerd. </p> <p> Als de beweging binnen het stalengebied wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt zowel aanraakinvoer als muisinvoer op Windows-apparaten met een aanraakscherm en muis. Deze ondersteuning is echter beperkt tot Chrome, Internet Explorer 11 en alleen Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Zoomviewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een koppeling die de viewer in een apart browservenster opent als deze optie is geselecteerd. In andere gevallen moet u de viewer rechtstreeks insluiten op de hostpagina. In het laatste geval kan de webpagina een statische indeling hebben of een responsief ontwerp gebruiken dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, insluiten van vaste grootte en insluiten van responsieve ontwerpen.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van het apparaat wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

U wordt aangeraden een uit-de-box HTML-pagina te gebruiken voor de pop-upbewerkingsmodus. De uit-van-de-doos HTML pagina wordt geroepen `ZoomViewer.html` en het bevindt zich onder de `html5/` subfolder van uw standaard plaatsing IS-Viewers zoals in het volgende:

`<s7viewers_root>/html5/ZoomViewer.html`

Pas aangepaste CSS toe om een aangepaste verschijning voor de pagina te bereiken.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in het nieuwe venster wordt geopend:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt normaal gesproken slechts een deel van het onroerend goed van de webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na de eerste keer laden. Deze optie is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij de insluitmodus voor responsief ontwerp wordt ervan uitgegaan dat het formaat van de viewer tijdens de runtime moet worden aangepast vanwege de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt aangepast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze logica zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke lay-outkaders zoals Bootstrap en Stichting gebruiken.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt `DIV`vult de viewer dat gebied en volgt de grootte die de webpagina biedt. U kunt de viewer bijvoorbeeld insluiten in een modale overlay, waarbij de grootte van de overlay afhankelijk is van de venstergrootte van de webbrowser.

## Insluiten met vaste grootte {#section-44f365e6c0dd40709467a459afa82a7f}

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL ZoomViewer.js]. De [!DNL ZoomViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Alleen verwijzen naar de JavaScript-hoofdviewer `include` op uw pagina. Verwijs niet naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar HTML5 SDK `Utils.js` bibliotheek die door de viewer is geladen vanuit `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK) `include`). De reden is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken worden volledig beheerd door de logica van de viewer en de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet bij `includes` op de server.
>
>
>Hierdoor wordt een directe verwijzing naar secundaire JavaScript geplaatst `include` die door de viewer op de pagina worden gebruikt, verbreekt de viewerfunctionaliteit in de toekomst wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding voor een DIV-element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen.

   In deze viewer worden miniaturen weergegeven wanneer u werkt met sets met meerdere items. Op desktopsystemen worden miniaturen onder de hoofdweergave geplaatst. Tegelijkertijd kan de viewer het hoofdelement tijdens runtime wisselen met `setAsset()` API. Als ontwikkelaar hebt u controle over de manier waarop de viewer het miniatuurgebied onderaan beheert wanneer het nieuwe element slechts één item bevat. Het is mogelijk om de grootte van de buitenste viewer ongewijzigd te laten en de hoofdweergave de hoogte te laten verhogen en het gebied met miniaturen te laten beslaan. U kunt ook de grootte van de hoofdweergave statisch houden en het buitenste viewergebied samenvouwen, de inhoud van de webpagina omhoog laten verplaatsen en de ruimte in de ruimte met vrije schermruimte uit de miniaturen gebruiken.

   Als u de buitenste grenzen van de viewer ongewijzigd wilt laten, definieert u de grootte voor de `.s7zoomviewer` CSS-klasse op hoofdniveau in absolute eenheden. De grootte in CSS kan op de pagina van de HTML worden gezet. U kunt de voorinstelling ook in een CSS-bestand voor een aangepaste viewer plaatsen. Dit bestand wordt later toegewezen aan een record met viewervoorinstellingen in Dynamic Media Classic of expliciet doorgegeven via een stijlopdracht.

   Zie [Zoomviewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische buitenste viewergrootte in een HTML-pagina:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   In het volgende voorbeeld ziet u het gedrag met een vaste buitenviewer. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   Als u de afmetingen van de hoofdweergave statisch wilt maken, definieert u de viewergrootte in absolute eenheden voor het binnenste `Container` SDK-component met `.s7zoomviewer` `.s7container` CSS-kiezer of door gebruik te maken van `stagesize` modifier.

   Hieronder ziet u een voorbeeld van het definiëren van de viewergrootte voor de binnenzijde `Container` SDK-component, zodat het hoofdweergavegebied niet van grootte verandert wanneer u van element verandert:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   De volgende demopagina toont het gedrag van de viewer met een vaste hoofdweergavegrootte. Wanneer u tussen sets schakelt, blijft de hoofdweergave statisch en wordt de inhoud van de webpagina verticaal verplaatst.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   U kunt de `stagesize` in de viewervoorinstellingsrecord in Dynamic Media Classic. Of u kunt deze expliciet doorgeven met de initialisatiecode van de viewer met de `params` verzameling of als API-aanroep zoals beschreven in de sectie Opdrachtverwijzing van deze Help, zoals hieronder:

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.ZoomViewer` klasse, geef alle configuratieinformatie tot zijn aannemer door en roep `init()` op een viewerinstantie.

   De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die de viewer ondersteunt. In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` vastgoed en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In dit voorbeeld wordt ervan uitgegaan `zoomViewer` de viewer-instantie is, `s7viewer` de naam van de plaatsaanduiding DIV; `http://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver, en `Scene7SharedAssets/ImageSet-Views-Sample` is het actief.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Video-viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsief ontwerpinsluiting met onbeperkte hoogte {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In het volgende voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer toestaat `DIV` om 40% van de grootte van het venster van de Webbrowser te nemen, verlatend zijn hoogte onbeperkt. De HTML-code van de webpagina ziet er als volgt uit:

```html {.line-numbers}
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
1. De viewer maken en initialiseren

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. De container DIV toevoegen aan het bestaande `"holder"` DIV. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Flexibele insluiting op grootte met gedefinieerde breedte en hoogte {#section-3674e6c032594441a6576b7fb1de6e64}

Als er insluiting in flexibele grootte is waarbij de breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreer het in het browser venster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` tot 100 procent.

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

De overige insluitingsstappen zijn identiek aan de stappen die worden gebruikt voor responsieve ontwerpinsluiting met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Insluiten met behulp van setter-API {#section-44e014925f24418b900696003855c0a9}

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Met deze API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met `setContainerId()`, `setParam()`, en `setAsset()` API-methoden met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting op vaste grootte met een setter-API geïllustreerd:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
