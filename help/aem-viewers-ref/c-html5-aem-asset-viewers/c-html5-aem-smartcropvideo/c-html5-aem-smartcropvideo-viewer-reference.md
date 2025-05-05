---
title: Smart Crop Video Viewer
description: In de Smart Crop Video Viewer worden streaming en progressieve video die in de H.264-indeling is gecodeerd, afgespeeld met ondersteuning voor slimme uitsnijdingen. Het wordt geleverd door Dynamic Media Classic of Adobe Experience Manager met Dynamic Media.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2399'
ht-degree: 0%

---

# Video over slim uitsnijden{#smart-crop-video}

In de Smart Crop Video Viewer worden streaming en progressieve video die in de H.264-indeling is gecodeerd, afgespeeld met ondersteuning voor slimme uitsnijdingen. Het wordt geleverd van Dynamic Media Classic of Experience Manager met Dynamic Media.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Zowel enkelvoudige video als Adaptieve videosets worden ondersteund. De viewer ondersteunt ook het werken met progressieve video- en HLS-streams die op externe locaties worden gehost. Het is ontworpen voor zowel desktopbrowsers als mobiele webbrowsers die HTML5-video ondersteunen. Deze viewer ondersteunt ook optionele, gesloten bijschriften die boven op video-inhoud, navigatie in videohoofdstukken en gereedschappen voor het delen van sociale media worden weergegeven.

De SmartCrop Video-viewer gebruikt in de standaardconfiguratie HTML5-streaming video afspelen in HLS-indeling wanneer het onderliggende systeem dit ondersteunt. Op systemen die geen ondersteuning bieden voor HTML5-streaming, valt de viewer terug naar de progressieve HTML van de video.

Viewer type 518.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## De Smart Crop Video Viewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

De Smart Crop Video Viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulpbestanden, één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen en CSS-gedownload door de viewer in runtime.

U kunt de SmartCrop Video-viewer in de pop-upmodus gebruiken met een HTML-pagina die klaar is voor productie en die wordt geleverd bij IS-Viewers. U kunt de viewer ook gebruiken in de ingesloten modus, waar deze met de gedocumenteerde API is geïntegreerd in een doelwebpagina.

Het configureren en toewijzen van een skin aan de viewer is vergelijkbaar met die van andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met de SmartCrop Video-viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

De Smart Crop Video Viewer biedt een set standaardbesturingselementen voor de gebruikersinterface voor het afspelen van video, zoals:

* Een knop Afspelen/Pauzeren.
* Videoscrubber-videotijdballon.
* Tijdindicator voor afspeeltijd/totale tijd.
* Volumeregeling.
* schermvullende knop.
* Schakelen tussen Closed Caption-codes.

Al deze controles worden gegroepeerd in een controlebar bij de bodem van het gebruikersinterface van de kijker.

Op aanraakapparaten is volumeregeling verborgen in de gebruikersinterface, omdat het alleen mogelijk is het volume te regelen met de hardwareknoppen.

Wanneer de viewer werkt in de pop-upmodus, is de knop Volledig scherm niet beschikbaar in de gebruikersinterface.

U kunt snel door de inhoud van een video navigeren wanneer het videohoofdstuk wordt geactiveerd. De videohoofdstukken worden getoond als tellers in het videoscrubberspoor en tonen de hoofdstuktitel en bijbehorende beschrijving op een muisomvergooien of met één enkele aanraking op aanrakingssystemen. Gebruikers kunnen naar een bepaald hoofdstuk zoeken door een hoofdstukmarkering te selecteren of de ballon met de hoofdstukbeschrijving te selecteren.

De viewer ondersteunt zowel aanraakinvoer als muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter beperkt tot Chrome, Internet Explorer 11 en alleen Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Gereedschappen voor het delen van sociale media met SmartCrop Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

De SmartCrop Video-viewer ondersteunt gereedschappen voor het delen van sociale media. Ze zijn beschikbaar als één knop in de gebruikersinterface die wordt uitgevouwen tot een werkbalk voor delen wanneer de gebruiker erop klikt of tikt.

De werkbalk voor delen bevat een pictogram voor elk type kanaal dat wordt ondersteund, zoals Facebook, Twitter, e-maildelen, het insluiten van code voor delen en het delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, leidt de viewer de gebruiker om naar een standaarddialoogvenster voor delen via een sociale-mediaservice. Ook wanneer het afspelen van video automatisch wordt gepauzeerd met een gereedschap voor delen.

Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

## Smart Crop Video Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een koppeling die de viewer in een apart browservenster opent wanneer u deze optie selecteert. In andere gevallen moet u de viewer rechtstreeks insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: popup, insluiten van vaste grootte en insluiten van responsieve ontwerpen.

Het insluiten van meerdere video&#39;s op dezelfde pagina wordt ondersteund op tablets en mobiele apparaten. Gewoonlijk kan slechts één video tegelijk worden afgespeeld. Wanneer een gebruiker een video begint af te spelen en vervolgens een andere video probeert af te spelen, wordt de eerste video automatisch gepauzeerd. De video die automatisch is gepauzeerd onthoudt de huidige afspeeltijd, zodat de gebruiker er altijd weer naar kan terugkeren en het afspelen kan hervatten. De enige uitzondering op deze regel is de Chrome-browser op Android™ 4.x-apparaten, die video&#39;s parallel kunnen afspelen.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van het apparaat wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een uit-van-doos HTML-pagina voor pop-up verrichtingswijze te gebruiken. Het wordt [!DNL SmartCropVideoViewer.html] en het bevindt zich onder de [!DNL html5/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**Insluitmodus met vaste grootte en responsieve insluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt normaal gesproken slechts een deel van het onroerend goed van de webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tabletapparaten, en ook responsieve ontwerppagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na de eerste keer laden. Dit is de beste keuze voor webpagina&#39;s met een statische pagina-indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime de grootte moet wijzigen als gevolg van de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van de viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de webpagina de grootte van de container aanpast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze methode zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die een ontvankelijk kader van de ontwerplay-out zoals Bootstrap of Stichting gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`, vult de viewer alleen dat gebied en volgt het formaat dat wordt aangegeven door de indeling van de webpagina. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de grootte van het venster van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL SmartCropVideoViewer.js]. De [!DNL SmartCropVideoViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Relatief pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   Controleer of de functie Volledig scherm goed werkt in Internet Explorer. Controleer of het DOM geen andere elementen bevat die een hogere stapelvolgorde hebben dan de plaatsaanduiding DIV.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding voor een DIV-element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de viewer instellen door deze te declareren voor `.s7videoviewer` CSS-klasse op hoofdniveau in absolute eenheden of met de modifier `stagesize`.

   U kunt de grootte in CSS rechts op de pagina HTML of in een aangepast CSS-bestand van de viewer plaatsen. Deze wordt later toegewezen aan een viewer-voorinstellingsrecord in Dynamic Media Classic of expliciet doorgegeven met behulp van een stijlopdracht.

   Zie [De Smart Crop Video-viewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in een HTML-pagina:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt instellen `stagesize` in de viewervoorinstellingsrecord in Dynamic Media Classic, of geef deze expliciet door met de viewerinitialisatiecode met `params` verzameling. Of, als API vraag zoals die in de de verwijzingssectie van het Bevel wordt beschreven, zoals in het volgende:

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.SmartCropVideoViewer` klasse, alle configuratieinformatie tot zijn aannemer overgaan, en vraag `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval: `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` eigenschap, videoserver-URL doorgegeven als `videoserverurl` en het oorspronkelijke actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de `init()` methode. In dit voorbeeld wordt ervan uitgegaan `smartCropVideoViewer` de viewer-instantie is, `s7viewer` is de naam van de tijdelijke aanduiding `DIV`, [!DNL http://s7d1.scene7.com/is/image/] is de URL van de Beeldserver; [!DNL http://s7d1.scene7.com/is/content/] de URL van de videoserver is, en [!DNL html5automation/frisbee-AVS] is het actief.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Smart Crop Video Viewer insluit met een vaste grootte:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Met responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een of andere flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In dit voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer toestaat `DIV` om 40% van de grootte van het venster van de Webbrowser te nemen, verlatend zijn hoogte onbeperkt. De HTML-code van de webpagina ziet er als volgt uit:

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

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met het insluiten van een vaste grootte. Het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Container toevoegen `DIV` aan de bestaande &quot;houder&quot; `DIV`. De volgende code is een volledig voorbeeld. U kunt zien hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[Live demo&#39;s](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Locatie van alternatieve demo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=nl-NL)

**Responsief ontwerpinsluiting met gedefinieerde breedte en hoogte**

Als er responsieve ontwerpinsluiting is waarbij breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. De aanduiding voor beide formaten krijgt de aanduiding `DIV` en centreer deze in het browservenster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` element tot 100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
