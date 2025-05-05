---
title: Flyout
description: Flyout Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die wordt weergegeven in de vervolgweergave die een gebruiker activeert. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# Flyout{#flyout}

Flyout Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die wordt weergegeven in de vervolgweergave die een gebruiker activeert. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Het viewertype is 504.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Flyout-viewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

Flyout Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload

De Flyout Viewer is alleen bedoeld voor ingesloten gebruik, wat betekent dat deze met gedocumenteerde API is geïntegreerd in de webpagina. Voor de Flyout-viewer is geen voor productie geschikte webpagina beschikbaar.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. U kunt aangepaste CSS gebruiken om skins toe te passen.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Flyout Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

De Flyout Viewer ondersteunt Single-touch en multi-touch bewegingen die ook in andere mobiele toepassingen voorkomen.

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
   <td colname="col2"> <p> Hiermee activeert u de vervolgweergave of de wijzigingen tussen het primaire en het secundaire zoomniveau. </p> </td> 
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

Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Flyout-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. De webpagina kan een statische pagina-indeling hebben, of een responsief ontwerp gebruiken dat op verschillende apparaten anders wordt weergegeven of voor verschillende venstergrootten in de browser. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer twee primaire bewerkingsmodi: insluiting op vaste grootte en responsieve ontwerpinsluiting.

De insluitingsmodus met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt nadat de viewer voor het eerst is geladen. Deze optie is het meest geschikt voor webpagina&#39;s met een statische pagina-indeling.

Bij de insluitingsmodus voor responsief ontwerp wordt ervan uitgegaan dat de viewer tijdens runtime de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

Wanneer u responsieve ontwerpinsluitingsmodus gebruikt met de Flyout-viewer, moet u expliciete onderbrekingspunten opgeven voor de hoofdweergaveafbeelding met de opdracht `imagereload` parameter. In het ideale geval past u uw onderbrekingspunten aan met de breedteonderbrekingspunten van de viewer die door de CSS van de webpagina worden voorgeschreven.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop een webpaginacontainer werkt `DIV` is groot. Als de webpagina alleen de breedte van de container instelt `DIV`Als de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Dit betekent dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit specifieke gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de ontwerplay-out zoals Bootstrap en Stichting gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`en vult de viewer alleen dat gebied en volgt het formaat dat wordt aangegeven door de indeling van de webpagina. Een voorbeeld van een nuttig geval is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze `FlyoutViewer.js`. `FlyoutViewer.js` bevindt zich in het volgende [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media-servers waarop de IS-Viewers zijn geïnstalleerd.

Een relatief pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Alleen verwijzen naar de JavaScript-hoofdviewer `include` op uw pagina. Verwijs niet naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar HTML5 SDK `Utils.js` bibliotheek die door de viewer is geladen vanuit `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK) `include`). De reden is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken worden volledig beheerd door de logica van de viewer en de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet bij `includes` op de server.
>
>
>Hierdoor wordt een directe verwijzing naar secundaire JavaScript geplaatst `include` die door de viewer op de pagina worden gebruikt, verbreekt de viewerfunctionaliteit in de toekomst wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. De id van het DIV-element moet worden gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Het is de verantwoordelijkheid van de webpagina om de juiste `z-index` voor de plaatsaanduiding DIV-element. Zo zorgt u ervoor dat het vervolggedeelte van de viewer boven op de andere webpagina-elementen wordt weergegeven.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. De viewergrootte instellen.

   In deze viewer worden miniaturen weergegeven wanneer u werkt met sets met meerdere items. Op desktopsystemen worden miniaturen onder de hoofdweergave geplaatst. Tegelijkertijd kan de viewer het hoofdelement tijdens runtime wisselen met `setAsset()` API. Als ontwikkelaar hebt u controle over de manier waarop de viewer het miniatuurgebied in het onderste gebied beheert wanneer het nieuwe element slechts één item bevat. Het is mogelijk de grootte van de buitenste viewer ongewijzigd te laten en de hoogte van de hoofdweergave te verhogen en het gebied met miniaturen in beslag te nemen. U kunt ook de grootte van de hoofdweergave statisch houden en het buitenste viewergebied samenvouwen, de inhoud van de webpagina omhoog laten verplaatsen en vervolgens het openstaande paginagebied van de miniaturen gebruiken.

   Als u de buitenste grenzen van de viewer ongewijzigd wilt laten, definieert u de grootte voor `.s7flyoutviewer` CSS-klasse op hoofdniveau in absolute eenheden. De grootte in CSS kan op de pagina van de HTML worden gezet, of in een douaneCSS dossier van de kijker, later toegewezen aan een kijker vooraf ingestelde verslag in Dynamic Media Classic, of uitdrukkelijk overgegaan gebruikend stijlbevel.

   Zie [Flyout-viewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van de statische buitenste viewergrootte in een HTML-pagina:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt het gedrag met een vast buitenste viewergebied op de volgende voorbeeldpagina zien. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html?lang=nl-NL](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html?lang=nl-NL)

   Als u de afmetingen van de hoofdweergave statisch wilt maken, definieert u de viewergrootte in absolute eenheden voor het binnenste `Container` SDK-component gebruiken `.s7flyoutviewer .s7container` CSS-kiezer. Bovendien moet u de vaste grootte overschrijven die is gedefinieerd voor de `.s7flyoutviewer` CSS-klasse op hoofdniveau in de standaard viewer-CSS door deze in te stellen op `auto`.

   Hieronder ziet u een voorbeeld van het definiëren van de viewergrootte voor de binnenzijde `Container` SDK-component, zodat het hoofdweergavegebied niet van grootte verandert wanneer u van element verandert:

   ```html {.line-numbers}
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

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html?lang=nl-NL](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html?lang=nl-NL)

   Bovendien biedt de CSS van de standaardviewer een vaste grootte voor het buitenste gebied.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.FlyoutViewer` klasse, geef alle configuratieinformatie tot zijn aannemer door en roep `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet ten minste het volgende bevatten: `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan de DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` -tag of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan `flyoutViewer` de viewer-instantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; `http://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver; en `Scene7SharedAssets/ImageSet-Views-Sample` is het actief:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Flyout-viewer insluit met een vaste grootte:

   ```html {.line-numbers}
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
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## Responsief ontwerpinsluiting met onbeperkte hoogte {#section-056cb574713c4d07be6d07cf3c598839}

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

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met de stappen voor het insluiten van een vaste grootte. Het enige verschil is dat u de vaste grootte van de standaardviewer-CSS moet overschrijven met de grootte die is ingesteld in relatieve eenheden.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan de stappen voor de insluiting van een vaste grootte, met de volgende drie uitzonderingen:

* de container toevoegen `DIV` aan de bestaande &quot;houder&quot; `DIV`;
* added `imagereload` parameter met expliciete onderbrekingspunten;
* in plaats van een vaste viewergrootte in te stellen met absolute eenheden gebruikt u CSS die de breedte en hoogte van de viewer instelt op 100% zoals in het volgende voorbeeld:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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

[Locatie van alternatieve demo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=nl-NL)

## Flexibele insluiting van grootte met gedefinieerde breedte en hoogte {#section-0a329016f9414d199039776645c693de}

Als er insluiting in flexibele grootte is waarbij de breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreert het in het browser venster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element aan 100 percenten.

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Insluiten met behulp van op Setter gebaseerde API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Met deze API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met `setContainerId()`, `setParam()`, en `setAsset()` API-methoden, met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting op vaste grootte met een setter-API geïllustreerd:

```html {.line-numbers}
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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
