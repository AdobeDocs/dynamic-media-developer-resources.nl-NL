---
description: Flyout Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die wordt weergegeven in de vervolgweergave die een gebruiker activeert. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsive
seo-description: Flyout Viewer is een beeldviewer. Er wordt een statische afbeelding weergegeven met de ingezoomde versie die wordt weergegeven in de vervolgweergave die een gebruiker activeert. Deze viewer werkt met afbeeldingssets en de navigatie wordt uitgevoerd met stalen. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-title: Flyout
solution: Experience Manager
title: Flyout
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

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

Zie [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Flyout-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. De webpagina kan een statische pagina-indeling hebben, of een responsief ontwerp gebruiken dat op verschillende apparaten anders wordt weergegeven of voor verschillende venstergrootten in de browser. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer twee primaire bewerkingsmodi: insluiting op vaste grootte en responsieve ontwerpinsluiting.

De insluitingsmodus met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt nadat de viewer voor het eerst is geladen. Deze optie is het meest geschikt voor webpagina&#39;s met een statische pagina-indeling.

Bij de insluitingsmodus voor responsief ontwerp wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

Wanneer u responsieve ontwerpinsluitingsmodus gebruikt met de Flyout-viewer, moet u expliciete onderbrekingspunten voor de hoofdweergaveafbeelding opgeven met de `imagereload` parameter. In het ideale geval past u uw onderbrekingspunten aan met de breedteonderbrekingspunten van de viewer die door de CSS van de webpagina worden voorgeschreven.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van een webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Dit betekent dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit specifieke gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de ontwerplay-out zoals Boek, Stichting, etc. gebruiken.

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

   Zie [Flyout Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van de statische buitenste viewergrootte in een HTML-pagina:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt het gedrag met een vast buitenste viewergebied op de volgende voorbeeldpagina zien. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

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

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Houd er ook rekening mee dat de CSS van de standaardviewer een vaste grootte biedt voor het buitenste gebied.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.FlyoutViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens het `containerId` veld hebben met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die de viewer ondersteunt. In dit geval moet voor het `params` object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl` eigenschap en het eerste element als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan de DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Roep voor maximale compatibiliteit de `init()` methode aan vlak voor de afsluitende `BODY` tag of voor de body- `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met een `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan dat `flyoutViewer` de viewer-instantie is; de naam van de plaatsaanduiding `s7viewer` is `DIV`; `http://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver; en `Scene7SharedAssets/ImageSet-Views-Sample` is het actief:

   ```
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
* in plaats van een vaste viewergrootte in te stellen met absolute eenheden gebruikt u CSS die de breedte en hoogte van de viewer instelt op 100% zoals in het volgende voorbeeld:

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

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

