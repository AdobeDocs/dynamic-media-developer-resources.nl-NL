---
title: Panoramische viewer
description: HTML5 Panorama Viewer is een beeldviewer die een panoramische afbeelding weergeeft. Het doel van deze viewer is om een bolvormig panorama weer te geven, ook wel equirechthoekige afbeelding genoemd. Deze functie ondersteunt automatisch pannen en pannen door middel van gyroscopische bewegingen. Het is ontworpen voor gebruik op desktops en mobiele apparaten. De virtuele weergavemodus voor de realiteit is beschikbaar op mobiele apparaten die deze ondersteunen.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# Panoramisch{#panoramic}

HTML5 Panorama Viewer is een beeldviewer die een panoramische afbeelding weergeeft. Het doel van deze viewer is om een bolvormig panorama weer te geven, ook wel equirechthoekige afbeelding genoemd. Deze functie ondersteunt automatisch pannen en pannen door middel van gyroscopische bewegingen. Het is ontworpen voor gebruik op desktops en mobiele apparaten. De virtuele weergavemodus voor de realiteit is beschikbaar op mobiele apparaten die deze ondersteunen.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Viewer type 514.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Panoramische Viewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramische Viewer staat voor een hoofd-JavaScript-bestand en een set hulpbestanden die door de viewer in runtime worden gedownload. De set hulpbestanden bestaat uit één JavaScript-bestand dat alle HTML5 Viewer SDK-componenten bevat die door deze viewer, elementen en CSS worden gebruikt.
HTML5 Panoramische Viewer kan zowel in de pop-upmodus worden gebruikt met een pagina die klaar is voor productie en die wordt geleverd met IS-Viewers, als in de ingesloten modus, waarbij de viewer met behulp van gedocumenteerde API is geïntegreerd in de doelwebpagina.
Configuratie en skins zijn vergelijkbaar met die van de andere HTML5-viewers. Alle skins kunnen worden gemaakt met aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met HTML5 Panorama Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramische Viewer ondersteunt automatisch pannen en navigeren door slepen of gyroscopische bewegingen.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigatie </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Desktop </p> </td> 
   <td colname="col2"> <p>Automatisch pannen en slepen om te navigeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanraakapparaat </p> </td> 
   <td colname="col2"> <p>Standaard pannen en slepen om te navigeren. Navigeer door gyroscopische beweging in VR rendermodus (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt zowel aanraakinvoer als muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter beperkt tot Chrome-, Internet Explorer 11- en Edge-webbrowsers.
Panoramische Viewer kan panoramische afbeeldingen renderen in de modus Virtual Reality (VR) door de render-modifier op te geven. Wanneer rendering is ingeschakeld, wordt een panorama-afbeelding weergegeven in gesplitste schermen. Een veel voorkomend geval zou het beeld in een mobiele telefoon in een virtuele realisatiehoofdtelefoon moeten dienen, die afzonderlijke beelden voor elk oog verstrekt. De viewer reageert op de gyroscopische beweging van de kop en navigeert door de afbeelding.

## HTML5 Panoramische Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling. Als u die koppeling selecteert, wordt de viewer geopend in een apart browservenster. In andere gevallen kan het nodig zijn de viewer in te sluiten in de hostpagina. In het laatste geval kan de webpagina een statische lay-out hebben of ‘responsief’ zijn en anders worden weergegeven op verschillende apparaten of voor verschillende venstergrootten in de browser. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: popup, insluiten van vaste grootte en responsieve insluiting.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan als de browser wordt aangepast of de apparaatoriëntatie wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd A HTML-element of op een andere geschikte manier.

Het wordt aanbevolen een uit-van-doos HTML-pagina voor pop-up verrichtingswijze te gebruiken. Het wordt [!DNL PanoramicViewer.html] en het bevindt zich onder de [!DNL html5/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

Visuele aanpassing kan worden bereikt door aangepaste CSS toe te passen.

Hier volgt een voorbeeld van HTML-code waarmee de viewer in het nieuwe venster wordt geopend:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Insluitmodus met vaste grootte en responsieve insluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het vastgoed van een webpagina in beslag.

De meest gebruikte gevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve webpagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

Insluiten met vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na de eerste keer laden. Deze methode is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve bestanden wordt ervan uitgegaan dat de gebruiker de grootte tijdens runtime moet wijzigen als gevolg van de wijziging van de grootte van de container-DIV. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele indeling gebruikt.

In de responsieve modus gedraagt de viewer zich anders, afhankelijk van de manier waarop de container DIV van de webpagina wordt vergroot of verkleind. Als op de webpagina alleen de breedte van het DIV-containerelement wordt ingesteld en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze methode zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval komt het meest voor op webpagina&#39;s die responsieve lay-outframeworks gebruiken, zoals Bootstrap, Foundation en dergelijke.

Als de webpagina de breedte en de hoogte voor de container-DIV van de viewer instelt, vult de viewer dat gebied en volgt deze het formaat dat wordt aangegeven door de indeling van de webpagina. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL PanoramicViewer.js]. De [!DNL PanoramicViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Relatief pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Alleen verwijzen naar de JavaScript-hoofdviewer `include` op uw pagina. Verwijs niet naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar HTML5 SDK `Utils.js` bibliotheek die door de viewer is geladen vanuit `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK) `include`). De reden is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken worden volledig beheerd door de logica van de viewer en de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet bij `includes` op de server.
>
>
>Hierdoor wordt een directe verwijzing naar secundaire JavaScript geplaatst `include` die door de viewer op de pagina worden gebruikt, verbreekt de viewerfunctionaliteit in de toekomst wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.


   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de viewer instellen door deze te declareren voor `.s7panoramicviewer` CSS-klasse op hoofdniveau in absolute eenheden of met de modifier `stagesize`.

   Grootte in CSS kan rechts worden geplaatst op de pagina HTML of in een aangepast CSS-bestand van de viewer, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in AOD of expliciet wordt doorgegeven met de opdracht style. Raadpleeg De sectie Viewer aanpassen voor meer informatie over het opmaken van de viewer met CSS. Hieronder ziet u een voorbeeld van het definiëren van de statische viewergrootte in de pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` De bepaling kan uitdrukkelijk met de kijker initialisatiecode met paramenteninzameling of als API vraag worden overgegaan zoals die in de sectie van de Verwijzing van het Bevel wordt beschreven, als dit:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   Een op CSS gebaseerde benadering wordt aanbevolen en wordt in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.PanoramicViewer` klasse, geef alle configuratieinformatie tot zijn aannemer door en roep `init(`) op een viewer-instantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minimaal het veld containerId hebben met de naam van de viewercontainer-id en het geneste JSON-object params met configuratieparameters die door de viewer worden ondersteund. In dit geval moet voor params-objecten ten minste de URL voor afbeeldingsserver worden doorgegeven `serverUrl` eigenschap en eerste element als parameter element. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` -tag of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de `init()` methode. In dit voorbeeld wordt ervan uitgegaan `panoramicViewer` de viewer-instantie is, `s7viewer` is de naam van de tijdelijke aanduiding `DIV`, [!DNL http://s7d1.scene7.com/is/image/] is de URL van de afbeeldingsserver, en [!DNL Scene7SharedAssets/PanoramicImage-Sample] is het actief.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Panoramische Viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Met het responsieve insluiten heeft de webpagina normaal gesproken een of andere flexibele indeling die de uitvoeringsgrootte van de container van de viewer DIV instelt. In dit voorbeeld gaan we ervan uit dat de webpagina de container DIV van de viewer toestaat 80% van de venstergrootte van de webbrowser in beslag te nemen, zodat de hoogte onbeperkt blijft. De HTML-code van de webpagina kan er als volgt uitzien:

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

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met het insluiten van een vaste grootte, met het enige verschil dat u niet expliciet de viewergrootte hoeft te definiëren:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Container DIV moet worden toegevoegd aan het bestaande &quot;holder&quot; DIV. De volgende code is een volledig voorbeeld. Mogelijk ziet u hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Locatie van alternatieve demo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsief ontwerpinsluiting met gedefinieerde breedte en hoogte**

Als er responsieve ontwerpinsluiting is met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. het verstrekt beide grootte aan de &quot; houder&quot; `DIV` en centreer deze in het browservenster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element tot 100%:

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

De overige insluitstappen zijn identiek aan het insluiten van responsieve lagen met onbeperkte hoogte. Het resulterende voorbeeld is

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Insluiten met behulp van op Setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Met die API neemt de constructor geen parameters en worden configuratieparameters opgegeven met `setContainerId()`, `setParam()`, en `setAsset()` API-methoden met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het insluiten van een vaste grootte met een setter-API geïllustreerd:

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
