---
description: eCatalog Search Viewer is een catalogusviewer die elektronische brochures in een spread per spread of pagina per pagina weergeeft. Met de eCatalog kunnen gebruikers door de catalogus navigeren met behulp van aanvullende gebruikersinterface-elementen of toegewijde miniatuurmodus. Gebruikers kunnen ook op elke pagina inzoomen voor meer informatie.
keywords: responsief
solution: Experience Manager
title: Zoeken in eCatalog
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# Zoeken in eCatalog{#ecatalog-search}

eCatalog Search Viewer is een catalogusviewer die elektronische brochures in een spread per spread of pagina per pagina weergeeft. Met de eCatalog kunnen gebruikers door de catalogus navigeren met behulp van aanvullende gebruikersinterface-elementen of toegewijde miniatuurmodus. Gebruikers kunnen ook op elke pagina inzoomen voor meer informatie.

Deze viewer werkt met catalogi en ondersteunt optionele afbeeldingen met hyperlinks en gereedschappen voor sociaal delen. Deze bevat zoomgereedschappen, gereedschappen voor catalogusnavigatie, ondersteuning voor volledig scherm, miniaturen en een optionele knop Sluiten. De viewer ondersteunt ook gereedschappen voor sociaal delen, Afdrukken, Downloaden en Favorieten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

De gebruiker kan ook op trefwoorden of woordgroepen gebaseerde zoekopdrachten uitvoeren in de inhoud van de catalogus.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 513.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## De eCatalog Viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Search Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand bevat alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload

U kunt de eCatalog Search Viewer in de pop-upmodus gebruiken met een HTML-pagina die klaar is voor productie en die wordt geleverd met IS-Viewers of in de ingesloten modus, waar deze wordt geïntegreerd in de doelwebpagina met behulp van gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met eCatalog Search Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De eCatalog Search Viewer ondersteunt de volgende aanraakbewegingen die ook in andere mobiele toepassingen voorkomen.

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
   <td colname="col2"> <p>Hiermee bladert u door de lijst met cataloguspagina's als een overgang naar een diaframe wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal vegen of tikken </p> </td> 
   <td colname="col2"> <p>Wanneer de afbeelding in een herstelstatus staat, wordt een native paginaschuiving uitgevoerd. </p> <p>Wanneer de duimnagels actief zijn, scrolt het de lijst van duimnagels. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het is mogelijk om een realistisch animatie-effect voor paginapijten in te schakelen voor het navigeren tussen cataloguspagina&#39;s. In dergelijke gevallen kan een gebruiker een paginahoek vasthouden en slepen en de pagina omdraaien.

Deze viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met een aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

## Gereedschappen voor het delen van sociale media met eCatalog Search Viewer {#section-eb575084a99647c3a9591f439f40b412}

De eCatalogKijker van het Onderzoek steunt sociale het delen hulpmiddelen zij beschikbaar als knoop in de belangrijkste controlebar die zich in een het delen hulpmiddelbar uitbreidt wanneer een gebruiker klikt of op het klikt.

De werkbalk voor delen bevat pictogrammen voor elk type ondersteund kanaal voor delen, waaronder Facebook, Twitter, Delen via e-mail, delen van code insluiten en delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, stuurt de viewer de gebruiker door naar een standaarddialoogvenster voor delen van een sociale service. Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

De zoekfunctie van de viewer is beschikbaar als een glaspictogram in de hoofdwerkbalk. Als u op het pictogram klikt of erop tikt, wordt in het deelvenster Zoeken een invoerveld weergegeven. Nadat u een trefwoord of woordgroep hebt ingevoerd en op Enter hebt gedrukt, rendert de viewer de zoekresultaten in het deelvenster en markeert hij de gevonden woorden in de hoofdweergave.

## ECatalog Search Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een koppeling die de viewer in een apart browservenster opent als deze optie is geselecteerd. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk ontwerp het inbedden.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een uit-de-box HTML-pagina te gebruiken voor de pop-upbewerkingsmodus. In dit geval wordt [!DNL eCatalogSearchViewer.html] en bevindt zich binnen het [!DNL html5/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij insluiten van responsief ontwerp wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt aangepast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke lay-outkaders zoals Bootstrap, Stichting, etc. gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`, vult de viewer alleen dat gebied en volgt het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL eCatalogSearchViewer.js]. De [!DNL eCatalogSearchViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media-servers waarop de IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de viewer instellen door deze te declareren voor `.s7ecatalogsearchviewer` CSS-klasse op hoofdniveau in absolute eenheden of met gebruik van `stagesize` modifier.

   U kunt de grootte in CSS rechtstreeks op de pagina van de HTML plaatsen, of in een dossier van douanekijker CSS, dat dan later aan een kijker vooraf ingesteld verslag in Dynamic Media Classic wordt toegewezen, of uitdrukkelijk wordt overgegaan gebruikend een stijlbevel.

   Zie [eCatalog-viewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in een HTML-pagina:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt de `stagesize` in de viewervoorinstellingsrecord in Dynamic Media Classic of deze expliciet doorgeven met de viewerinitialisatiecode met `params` verzameling, of als een API-aanroep zoals beschreven in de sectie Opdrachtverwijzing, zoals hieronder:

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. De viewer initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.eCatalogSearchViewer` klasse, geef alle configuratieinformatie tot zijn aannemer door en roep `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object heeft minstens de `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u echter de `init()` methode vlak voor het sluiten `BODY` -tag of op de hoofdtekst `onload()` gebeurtenis.

   Het containerelement hoeft echter nog geen deel uit te maken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan `eCatalogSearchViewer` de viewer-instantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; `https://s7d1.scene7.com/is/image/` is de URL van de afbeeldingsserver, en `Viewers/Pluralist` is het actief:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de eCatalog Search Viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In dit voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer toestaat `DIV` om 40% van de grootte van het venster van de Webbrowser te nemen, verlatend zijn hoogte onbeperkt. De resulterende HTML code van de webpagina ziet er als volgt uit:

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

Het toevoegen van de viewer aan een dergelijke pagina lijkt op het insluiten van een vaste grootte. Het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan het insluiten van een vaste grootte. De container toevoegen `DIV` aan de bestaande &quot;houder&quot; `DIV`. De volgende code is een volledig voorbeeld. U kunt zien hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert hoe u in de praktijk meer gevallen kunt gebruiken van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexibele insluiting van grootte met gedefinieerde breedte en hoogte**

In het geval van insluiting van flexibele grootte met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. Met andere woorden: de houder krijgt beide grootten `DIV` en centreert het in het browservenster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element tot 100%:

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

De overige insluitstappen zijn identiek aan het reageren op ontwerpinsluiting met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie is het mogelijk om setter-gebaseerde API en no-args constructor te gebruiken. Met die API-constructor worden geen parameters gebruikt en worden configuratieparameters opgegeven met `setContainerId()`, `setParam()`, en `setAsset()` API-methoden met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het insluiten van een vaste grootte met een setter-API getoond:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
