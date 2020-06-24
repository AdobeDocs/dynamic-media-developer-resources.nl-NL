---
description: eCatalog Viewer is een catalogusviewer die elektronische brochures in een spread per spread of pagina per pagina weergeeft. Met de eCatalog kunnen gebruikers door de catalogus navigeren met behulp van extra gebruikersinterface-elementen of een toegewijde miniatuurmodus. Gebruikers kunnen ook op elke pagina inzoomen voor meer informatie.
keywords: responsive
seo-description: eCatalog Viewer is een catalogusviewer die elektronische brochures in een spread per spread of pagina per pagina weergeeft. Met de eCatalog kunnen gebruikers door de catalogus navigeren met behulp van extra gebruikersinterface-elementen of een toegewijde miniatuurmodus. Gebruikers kunnen ook op elke pagina inzoomen voor meer informatie.
seo-title: eCatalog
solution: Experience Manager
title: eCatalog
topic: Dynamic media
uuid: 6950306d-637e-4932-ae96-c5366e5477f3
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---


# eCatalog{#ecatalog}

eCatalog Viewer is een catalogusviewer die elektronische brochures in een spread per spread of pagina per pagina weergeeft. Met de eCatalog kunnen gebruikers door de catalogus navigeren met behulp van extra gebruikersinterface-elementen of een toegewijde miniatuurmodus. Gebruikers kunnen ook op elke pagina inzoomen voor meer informatie.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van Image Rendering (IR) of door de gebruiker gegenereerde inhoud (UGC) worden niet ondersteund door deze viewer.

Viewer type 507.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Deze viewer werkt met catalogi en ondersteunt optionele afbeeldingen met hyperlinks en gereedschappen voor sociaal delen. Deze bevat zoomgereedschappen, gereedschappen voor catalogusnavigatie, ondersteuning voor volledig scherm, miniaturen en een optionele knop Sluiten. De viewer ondersteunt ook gereedschappen voor sociaal delen, Afdrukken, Downloaden en Favorieten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## De eCatalog Viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload

U kunt eCatalog Viewer in pop-upmodus gebruiken met een voor productie geschikte HTML-pagina die is voorzien van IS-Viewers of in de ingesloten modus, waar deze is geïntegreerd in de doelwebpagina met behulp van gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met eCatalog Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De eCatalog Viewer ondersteunt de volgende aanraakbewegingen die ook in andere mobiele toepassingen worden gebruikt.

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
   <td colname="col2"> <p> Hiermee selecteert u nieuwe miniaturen in stalen. </p> </td> 
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
   <td colname="col1"> <p>Horizontaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Hiermee bladert u door de lijst met cataloguspagina's als een overgang naar een diaframe wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal vegen of tikken </p> </td> 
   <td colname="col2"> <p>Wanneer de afbeelding in een herstelstatus staat, wordt een native paginaschuiving uitgevoerd. </p> <p>Wanneer de duimnagels actief zijn, scrolt het de lijst van duimnagels. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het is mogelijk om een realistisch animatie-effect voor paginapijten in te schakelen voor het navigeren tussen cataloguspagina&#39;s. In dergelijke gevallen kan een gebruiker een paginahoek vasthouden en slepen en de pagina omdraaien.

Deze viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met een aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord, zoals wordt beschreven in [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Hulpprogramma&#39;s voor het delen van sociale media met eCatalog Viewer {#section-eb575084a99647c3a9591f439f40b412}

De eCatalog-viewer ondersteunt gereedschappen voor sociaal delen Deze gereedschappen zijn beschikbaar als een knop op de hoofdbesturingsbalk die wordt uitgevouwen tot een werkbalk voor delen wanneer een gebruiker erop klikt of erop tikt.

De werkbalk voor delen bevat pictogrammen voor elk type ondersteund kanaal voor delen, waaronder Facebook, Twitter, Delen via e-mail, delen via insluiten van code en delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, stuurt de viewer de gebruiker door naar een standaarddialoogvenster voor delen van een sociale service. Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

## eCatalog-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling die de viewer in een apart browservenster opent wanneer erop wordt geklikt. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk ontwerp het inbedden.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met behulp van `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een HTML-pagina uit de doos te gebruiken voor de pop-upbewerkingsmodus. In dit geval, wordt het geroepen [!DNL eCatalogViewer.html] en wordt gevestigd binnen [!DNL html5/] subfolder van uw standaard plaatsing IS-Viewers:

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als gevolg van de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval komt het meest voor bij webpagina&#39;s die responsieve lay-outframeworks gebruiken, zoals Bootstrap, Foundation, enzovoort.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt, vult de viewer alleen dat gebied `DIV`en volgt deze het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Zorg ervoor dat u de viewer-API opneemt voordat u deze kunt gebruiken [!DNL eCatalogViewer.js]. Het [!DNL eCatalogViewer.js] bestand bevindt zich in de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop de IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
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

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7ecatalogviewer` `stagesize` top-level CSS klasse in absolute eenheden te verklaren, of door bepaling te gebruiken.

   U kunt grootte in CSS plaatsen direct op de HTML- pagina, of in een douaneCSS dossier van de kijker, dat dan later aan een kijker vooraf ingesteld verslag in het Publiceren Scene7 Systeem wordt toegewezen, of uitdrukkelijk overgegaan gebruikend een stijlbevel.

   Zie [De eCatalog Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in HTML-pagina:

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt de bepaling of in de kijker vooraf ingestelde verslag in het Publiceren Scene7 Systeem plaatsen, of het uitdrukkelijk met de kijker initialisatiecode met `stagesize` `params` inzameling overgaan, of als API vraag zoals die in de sectie van de Verwijzing van het Bevel wordt beschreven, als het volgende:

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. De viewer initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.eCatalogViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object heeft minimaal het `containerId` veld met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval moet voor het `params` object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl` eigenschap en het eerste element als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode echter aan vlak voor de afsluitende `BODY` tag of voor de `onload()` hoofdgebeurtenis.

   Het containerelement hoeft echter nog geen deel uit te maken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met een `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan dat `eCatalogViewer` de viewer-instantie is; `s7viewer` de naam van de plaatsaanduiding `DIV`; `http://s7d1.scene7.com/is/image/` Dit is de URL voor Beeldbewerking en `Viewers/Pluralist` is het element:

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de eCatalog Viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert hoe u in de praktijk meer gevallen kunt gebruiken van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie is het mogelijk om setter-gebaseerde API en no-args constructor te gebruiken. Met die API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met behulp van `setContainerId()`, `setParam()`en `setAsset()` API-methoden met aparte JavaScript-aanroepen.

In het volgende voorbeeld wordt het insluiten van een vaste grootte met een setter-API getoond:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```

