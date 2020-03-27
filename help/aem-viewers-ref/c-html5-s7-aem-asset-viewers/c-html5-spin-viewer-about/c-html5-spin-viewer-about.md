---
description: Spin Viewer is een beeldviewer die een weergave van 360 graden van de afbeelding biedt, of zelfs een multidimensionale weergave als de juiste centrifugeset wordt gebruikt. Deze heeft zoomen- en centrifugegereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
keywords: responsive
seo-description: Spin Viewer is een beeldviewer die een weergave van 360 graden van de afbeelding biedt, of zelfs een multidimensionale weergave als de juiste centrifugeset wordt gebruikt. Deze heeft zoomen- en centrifugegereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.
seo-title: Draaien
solution: Experience Manager
title: Draaien
topic: Dynamic media
uuid: 5d5cdf83-cfe8-48cd-af74-b270f7400b14
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Draaien{#spin}

Spin Viewer is een beeldviewer die een weergave van 360 graden van de afbeelding biedt, of zelfs een multidimensionale weergave als de juiste centrifugeset wordt gebruikt. Deze heeft zoomen- en centrifugegereedschappen, ondersteuning voor volledig scherm en een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 503.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400)

## Spin Viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

Spin Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload.

De draaiende viewer kan zowel in de pop-upmodus worden gebruikt met behulp van voor productie geschikte HTML-pagina die wordt geleverd met IS-Viewers, als in de ingesloten modus, waarbij de viewer met behulp van gedocumenteerde API is geïntegreerd in de doelwebpagina.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. Alle skins kunnen worden gemaakt met aangepaste CSS.

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met de centrifugerviewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De Draai Viewer ondersteunt de volgende aanraakbewegingen die veel voorkomen in andere mobiele toepassingen. Wanneer de viewer de veegbeweging van een gebruiker niet kan verwerken, stuurt deze de gebeurtenis door naar de webbrowser om een native paginaschuiving uit te voeren. Hierdoor kan de gebruiker door de pagina navigeren, zelfs als de viewer het grootste gedeelte van het apparaatschermgebied in beslag neemt.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dubbeltikken </p> </td> 
   <td colname="col2"> <p> Hiermee zoomt u in op één niveau totdat de maximale vergroting is bereikt. Met de volgende dubbele tikbeweging wordt de viewer opnieuw ingesteld op de eerste weergavestatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kneep </p> </td> 
   <td colname="col2"> <p>Hiermee zoomt u in of uit op de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Als de afbeelding zich in een herstelstatus bevindt, draait deze horizontaal door de set. </p> <p> Als in de afbeelding wordt ingezoomd, wordt de afbeelding horizontaal verplaatst. Als de afbeelding naar de weergaverand wordt verplaatst en er nog steeds een veegbeweging in die richting wordt uitgevoerd, wordt er een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Als de afbeelding in een herstelstatus staat, verandert de verticale weergavehoek voor het geval dat een multidimensionale centrifugeset wordt gebruikt. In een eendimensionale centrifuge of wanneer een multidimensionale centrifuge zich op de laatste of de eerste as bevindt, zodat de verticale veegbeweging niet resulteert in een wijziging van de verticale weergavehoek, wordt een native paginaschuiving uitgevoerd. </p> <p> Als u op de afbeelding hebt ingezoomd, wordt de afbeelding verticaal verplaatst. Als de afbeelding naar de weergaverand wordt verplaatst en er nog steeds een veegbeweging in die richting wordt uitgevoerd, wordt er een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Spin Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling die de viewer in een apart browservenster opent wanneer erop wordt geklikt. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk ontwerp het inbedden.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met behulp van `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een HTML-pagina uit de doos te gebruiken voor de pop-upbewerkingsmodus. In dit geval, wordt het geroepen [!DNL SpinViewer.html] en wordt gevestigd binnen [!DNL html5/] subfolder van uw standaard plaatsing IS-Viewers:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tabletapparaten, en ook responsieve ontwerppagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als gevolg van de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de ontwerplay-out zoals Boek, Stichting, etc. gebruiken.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt, vult de viewer alleen dat gebied `DIV`en volgt deze het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay afhankelijk is van de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de Spin Viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Zorg ervoor dat u de viewer-API opneemt voordat u deze kunt gebruiken `SpinViewer.js`. `SpinViewer.js` wordt gevestigd onder [!DNL html5/js/] subfolder van uw standaard plaatsing IS-Viewers:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   U kunt een relatieve weg gebruiken als de kijker op één van de servers van Adobe Scene7 wordt opgesteld en het van het zelfde domein wordt gediend. Anders, specificeert u een volledige weg aan één van de servers van Adobe Scene7 die de IS-Kijkers hebben geïnstalleerd.

   Het relatieve pad ziet er als volgt uit:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >U moet alleen verwijzen naar het JavaScript- `include` hoofdviewerbestand op uw pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK- `Utils.js` bibliotheek die door de viewer is geladen vanuit het `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet `includes` op de server.
   >
   >
   >Als u dus een directe verwijzing naar een secundair JavaScript dat door de viewer op de pagina wordt `include` gebruikt, maakt u de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7spinviewer` `stagesize` top-level CSS klasse in absolute eenheden te verklaren, of door bepaling te gebruiken.

   U kunt grootte in CSS plaatsen direct op de HTML- pagina, of in een douaneCSS dossier van de kijker, dat dan later aan een kijker vooraf ingesteld verslag in het Publiceren Scene7 Systeem wordt toegewezen, of uitdrukkelijk overgegaan gebruikend een stijlbevel.

   Zie De [Spin Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in HTML-pagina:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt de bepaling of in de kijker vooraf ingestelde verslag in het Publiceren Scene7 Systeem plaatsen, of het uitdrukkelijk met de kijker initialisatiecode met `stagesize` `params` inzameling overgaan, of als API vraag zoals die in de sectie van de Verwijzing van het Bevel wordt beschreven, als het volgende:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.SpinViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object bevat minimaal een `containerId` veld met de naam van de viewercontainer-id en een genest `params` JSON-object met configuratieparameters die de viewer ondersteunt. In dit geval van een `params` object moet ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl` eigenschap en eerste element als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Roep voor maximale compatibiliteit de `init()` methode aan vlak voor de afsluitende `BODY` tag of voor de body- `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs een deel zijn van de lay-out van de webpagina. Het kan bijvoorbeeld verborgen zijn met de `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan dat `spinViewer` de viewerinstantie `s7viewer` de naam van de plaatsaanduiding is `DIV`, [!DNL http://s7d1.scene7.com/is/image/] de URL van de afbeeldingsserver is en [!DNL Scene7SharedAssets/SpinSet_Sample] het element.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Spin Viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In dit voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer 40% van de venstergrootte van de webbrowser laat `DIV` innemen, zodat de hoogte onbeperkt blijft. De resulterende HTML-code voor webpagina&#39;s ziet er als volgt uit:

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

Het toevoegen van de viewer aan een dergelijke pagina lijkt op het insluiten van een vaste grootte. Het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan het insluiten van een vaste grootte. Voeg de container toe `DIV` aan de bestaande &quot;houder&quot; `DIV`. De volgende code is een volledig voorbeeld. U kunt zien hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert hoe u in de praktijk meer gevallen kunt gebruiken van responsieve ontwerpinsluiting met onbeperkte hoogte:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Flexibele insluiting van grootte met gedefinieerde breedte en hoogte**

In het geval van insluiting van flexibele grootte met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. Dit betekent dat de aanduiding zowel de grootte als het middelpunt van de aanduiding heeft in het browservenster. `DIV` Bovendien stelt de webpagina de grootte van het element `HTML` en het `BODY` element in op 100%:

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

De overige insluitstappen zijn identiek aan het reageren op ontwerpinsluiting met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met behulp van op Setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie is het mogelijk om setter-gebaseerde API en no-args constructor te gebruiken. Met die API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met behulp van `setContainerId()`, `setParam()`en `setAsset()` API-methoden met aparte JavaScript-aanroepen.

In het volgende voorbeeld wordt het insluiten van een vaste grootte met een setter-API getoond:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```

