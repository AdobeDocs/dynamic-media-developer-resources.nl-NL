---
title: Video360
description: De HTML5 Video360 Viewer is een videospeler van 360 graden die streaming en progressieve 360 video die in het formaat H.264 wordt gecodeerd speelt, van Dynamic Media Classic of van Adobe Experience Manager, Dynamic Media wordt geleverd.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Video360{#video}

De HTML5 Video360 Viewer is een videospeler van 360 graden die streaming en progressieve 360 video die in het formaat H.264 wordt gecodeerd speelt, van Dynamic Media Classic of van Adobe Experience Manager, Dynamic Media wordt geleverd.

Video&#39;s van 360 graden, ook wel overweldigende video&#39;s of sferische video&#39;s genoemd, zijn video-opnamen waarbij een weergave in elke richting tegelijkertijd wordt opgenomen en opgenomen met een omnidirectionele camera of een verzameling camera&#39;s. Zowel enkelvoudige video als Adaptieve videosets worden ondersteund. De viewer ondersteunt ook het werken met progressieve video- en HLS-streams die op externe locatie worden gehost.

De aanbevolen hoogte-breedteverhouding voor 360 video is 2:1. Ruimtelijk geluid wordt niet ondersteund. De viewer is alleen ontworpen voor gebruik met 360 video; Wanneer u probeert een andere video dan 360 af te spelen, wordt de video vervormd afgespeeld.

De viewer is ontworpen voor gebruik in zowel desktopbrowsers als mobiele webbrowsers die HTML5-video ondersteunen. De viewer ondersteunt optionele gereedschappen voor sociale media.

De Video360 Viewer gebruikt in de standaardconfiguratie HTML5-streaming video afspelen in HLS-indeling wanneer het onderliggende systeem dat ondersteunt. Op systemen die geen ondersteuning bieden voor HTML5-streaming, valt de viewer terug naar de progressieve HTML van de video.

Het viewertype is 517.

## Demo-URL&#39;s {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systeemvereisten {#section-b7270cc4290043399681dc504f043609}

Zie [Systeemvereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Video360 Viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden (één JavaScript-bestand met alle HTML5 Viewer SDK-componenten die door deze viewer worden gebruikt, elementen, CSS) die door de viewer in runtime zijn gedownload.

HTML5 Video360 Viewer kan zowel in popup-modus worden gebruikt met een pagina voor HTML die klaar is voor productie en die wordt geleverd bij IS-Viewers, als in de ingesloten modus, waarbij de viewer is geïntegreerd in de doelwebpagina met behulp van gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers die in deze handleiding worden beschreven. Alle skins toewijzen wordt bereikt door middel van aangepaste CSS (Cascading Style Sheets).

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Voor 360 video-inhoud zijn hogere coderingsinstellingen vereist dan voor de standaard niet-360 video. Met andere woorden, 360-inhoud moet een hogere resolutie krijgen dan niet-360-video om dezelfde waarneembare kwaliteit te bereiken. U wordt aangeraden de volgende instellingen voor adaptieve videovoorinstellingen voor 360 video in overweging te nemen:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Merk echter op dat het dienen van video die met dergelijke hoge kwaliteitsinstellingen wordt gecodeerd een hoge bandbreedteverbinding op het apparaat van een eindgebruiker vereist.

## Interactie met Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer biedt een set standaardbesturingselementen voor de gebruikersinterface voor het afspelen van video, zoals de knop Afspelen/pauzeren, de videoband van de scrubber, de tijd-tijdindicator voor het afspelen van de video, volumeregeling en de knop Volledig scherm. Al deze besturingselementen worden gegroepeerd in de besturingsbalk onder aan de gebruikersinterface van de viewer.

Op aanraakapparaten is de volumeregeling verborgen in de gebruikersinterface, omdat het alleen mogelijk is het volume te regelen met de hardwareknoppen van het apparaat.

Wanneer de viewer werkt in de pop-upmodus, is er geen knop voor een volledig scherm beschikbaar in de gebruikersinterface.

De viewer ondersteunt ook diverse gereedschappen voor het delen van sociale media. Ze zijn beschikbaar als één knop in de gebruikersinterface die wordt uitgevouwen tot een werkbalk voor delen wanneer de gebruiker erop klikt of tikt. De werkbalk voor delen bevat een pictogram voor elk type kanaal dat wordt ondersteund, zoals Facebook, Twitter, Delen via e-mail, Delen via code insluiten en delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, stuurt de viewer de gebruiker terug naar een standaarddialoogvenster voor delen via een sociale-mediaservice. Wanneer een gereedschap voor delen wordt geactiveerd, wordt het afspelen van video ook automatisch gepauzeerd. Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

De viewer ondersteunt het afspelen van 360 video op de volgende manieren:

* VR-headsets (zoals Oculus Go en Oculus Rift)
* VR HMD (hoofdmontage)-montagesysteem (zoals Google Cardboard)
* Niet-VR-apparaten (zoals desktopbrowsers, tablets en mobiele telefoons die niet zijn aangesloten op VR HMD-montageapparatuur)

Geen extra configuratie is noodzakelijk om 360 video inhoud op hoofdtelefoon te bekijken VR. De viewer detecteert automatisch de aanwezigheid van een VR-hoofdtelefoon en toont de knop VR boven op video-inhoud. Als u deze knop VR activeert, wordt het renderen van video overgeschakeld naar de VR-modus. De viewer ondersteunt alleen VR-rendering in browsers met WebVR-ondersteuning.

Voor het gebruik van VR HMD-montagesystemen `Video360Player.vrrender` modifier moet worden ingesteld op `1` in de configuratie van de kijker, die stereoscopische rendering afdwingt.

Op VR-koptelefoons en VR HMD-montagesystemen vindt verandering in het gezichtspunt plaats als reactie op de beweging van de hoofdtelefoon, niet op een ander afspeelapparaat in de VR-modus.

Wanneer de eindgebruiker 360 video op niet-VR toegelaten apparaten bekijkt, kan muis, aanraking, of toetsenbord gebruiken om videoplayback en gezichtspunt te controleren.

De viewer ondersteunt zowel aanraakinvoer als muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter beperkt tot Chrome-, Internet Explorer 11- en Edge-webbrowsers.

De viewer is volledig toegankelijk via het toetsenbord. Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Video360-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een koppeling die de viewer in een apart browservenster opent wanneer u deze optie selecteert. In andere gevallen moet u de viewer rechtstreeks insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: popup, insluiting van vaste grootte en responsieve ontwerpinsluiting.

Het insluiten van meerdere video&#39;s op dezelfde pagina wordt ondersteund op tablets en mobiele apparaten. Gewoonlijk kan slechts één video tegelijk worden afgespeeld. Wanneer een gebruiker een video begint af te spelen en vervolgens een andere video probeert af te spelen, wordt de eerste video automatisch gepauzeerd. De video die automatisch is gepauzeerd onthoudt de huidige afspeeltijd, zodat de gebruiker er altijd weer naar kan terugkeren en het afspelen kan hervatten. De enige uitzondering op deze regel is de Chrome-browser op Android™ 4.x-apparaten, die video&#39;s parallel kunnen afspelen.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van het apparaat wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een uit-van-doos HTML-pagina voor pop-up verrichtingswijze te gebruiken. Het wordt [!DNL Video360Viewer.html] en het bevindt zich onder de [!DNL html5/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Deze methode is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt aangepast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de lay-out van het Webontwerp zoals Bootstrap en Stichting gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`, vult de viewer alleen dat gebied en volgt het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL Video360Viewer.js]. De [!DNL Video360Viewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   Voor de volledige het schermeigenschap om behoorlijk in Internet Explorer te functioneren zorg ervoor dat er geen andere elementen in DOM zijn die een hogere stapelvolgorde dan uw placeholder hebben `DIV`.

   Hieronder ziet u een voorbeeld van een gedefinieerde plaatsaanduiding `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de viewer instellen door deze te declareren voor `.s7video360viewer` CSS-klasse op hoofdniveau in absolute eenheden of met gebruik van `stagesize` modifier.

   U kunt de grootte in CSS rechtstreeks op de pagina HTML of in een aangepast CSS-bestand van de viewer plaatsen, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in Adobe Experience Manager Assets - Op aanvraag of expliciet wordt doorgegeven met behulp van `style` gebruiken.

   Zie [Video360 Viewer aanpassen](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte op de pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   U kunt de `stagesize` in de viewervoorinstellingsrecord in AEM Assets. Op aanvraag. Of u kunt deze expliciet doorgeven met de initialisatiecode van de viewer met `params` verzameling, of als API-aanroep zoals beschreven in de sectie Opdrachtverwijzing, als volgt:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.Video360Viewer` klasse, alle configuratieinformatie tot zijn aannemer overgaan, en vraag `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die door de viewer worden ondersteund.

   In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel, een URL van een videoserver die als `videoserverurl` eigenschap, eerste actief als `asset` en interactieve gegevens als `interactivedata` eigenschap. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` -tag of op de hoofdtekst `onload()` gebeurtenis.

   Het containerelement hoeft echter nog geen deel uit te maken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dat gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt uitgegaan van het volgende:

   * De viewerinstantie is `video360Viewer`.
   * De naam van de tijdelijke aanduiding `DIV` is `s7viewer`.
   * De URL van de afbeeldingsserver is `https://s7d9.scene7.com/is/image`.
   * De URL van de videoserver is `https://s7d9.scene7.com/is/content`.
   * Het element is `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Video360 Viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

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
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. De container DIV toevoegen aan het bestaande `"holder"` DIV. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Responsief insluiten met gedefinieerde breedte en hoogte**

Als er responsieve insluiting is waarbij breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreer het in het browser venster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element aan 100 percenten.

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
