---
description: De Video Viewer is een videospeler die streaming en progressieve video afspeelt die in de H.264-indeling zijn gecodeerd. Het wordt geleverd van het Publiceren Scene7 Systeem of Dynamic Media AEM.
keywords: responsive
seo-description: De Video Viewer is een videospeler die streaming en progressieve video afspeelt die in de H.264-indeling zijn gecodeerd. Het wordt geleverd van het Publiceren Scene7 Systeem of Dynamic Media AEM.
seo-title: Video
solution: Experience Manager
title: Video
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2402'
ht-degree: 0%

---


# Video{#video}

De Video Viewer is een videospeler die streaming en progressieve video afspeelt die in de H.264-indeling zijn gecodeerd. Het wordt geleverd van het Publiceren Scene7 Systeem of Dynamic Media AEM.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Zowel enkelvoudige video als Adaptieve videosets worden ondersteund. Bovendien biedt de viewer ondersteuning voor het werken met progressieve video- en HLS-streams op externe locaties. Het is ontworpen voor zowel desktopbrowsers als mobiele webbrowsers die HTML5-video ondersteunen. Deze viewer ondersteunt ook optionele, gesloten bijschriften die boven op video-inhoud, navigatie in videohoofdstukken en gereedschappen voor het delen van sociale media worden weergegeven.

De video-viewer gebruikt in de standaardconfiguratie HTML5 streaming video playback in HLS-indeling wanneer het onderliggende systeem dit ondersteunt. Op systemen die geen ondersteuning bieden voor HTML5-streaming, valt de viewer terug naar progressieve HTML5-video.

Viewer type 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Video-viewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

De video-viewer vertegenwoordigt een hoofd-JavaScript-bestand en een set hulplijnbestanden, één JavaScript-bestand met alle Viewer SDK-componenten die door deze viewer worden gebruikt, elementen en CSS-gedownload door de viewer in runtime.

U kunt de Video-viewer in de pop-upmodus gebruiken met de voor productie geschikte HTML-pagina die bij IS-Viewers wordt geleverd. U kunt de viewer ook gebruiken in de ingesloten modus, waar deze is geïntegreerd in een doelwebpagina met behulp van de gedocumenteerde API.

Het configureren en toewijzen van een skin aan de viewer is vergelijkbaar met die van andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Video Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

De video Viewer biedt een set standaardbesturingselementen voor de gebruikersinterface voor het afspelen van video, zoals een afspeel-/pauzeknop, een videobubbel met scrubber, een indicator voor de afspeeltijd/totale tijd, volumeregeling, een knop voor volledig scherm en een schakelknop voor een gesloten bijschrift. Al deze controles worden gegroepeerd in een controlebar bij de bodem van het gebruikersinterface van de kijker.

Op aanraakapparaten is volumeregeling verborgen in de gebruikersinterface, omdat het alleen mogelijk is het volume te regelen met de hardwareknoppen.

Wanneer de viewer werkt in de pop-upmodus, is de knop Volledig scherm niet beschikbaar in de gebruikersinterface.

U kunt snel door de inhoud van een video navigeren wanneer videochaptering wordt geactiveerd. De videohoofdstukken worden getoond als tellers in het video scrubberspoor en tonen de hoofdstuktitel en bijbehorende beschrijving op een muisrol over of met één enkele aanraking op aanrakingssystemen. Gebruikers kunnen naar een bepaald hoofdstuk zoeken door op een hoofdstukmarkering te klikken of op de hoofdstukbeschrijvingsballon te tikken.

De viewer ondersteunt zowel aanraakinvoer als muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Gereedschappen voor sociale media delen met Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

De video-viewer ondersteunt gereedschappen voor het delen van sociale media Deze knoppen zijn beschikbaar als één knop in de gebruikersinterface die wordt uitgebreid naar een werkbalk voor delen wanneer de gebruiker erop klikt of tikt.

De werkbalk voor delen bevat een pictogram voor elk type kanaal dat wordt ondersteund, zoals Facebook, Twitter, Delen via e-mail, Delen via code insluiten en delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, stuurt de viewer de gebruiker terug naar een standaarddialoogvenster voor delen via een sociale-mediaservice. Ook wanneer een gereedschap voor delen is geactiveerd, wordt het afspelen van video automatisch gepauzeerd.

Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

## Video-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling die de viewer in een apart browservenster opent wanneer erop wordt geklikt. In andere gevallen moet u de viewer rechtstreeks insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: popup, insluiting van vaste grootte en responsieve ontwerpinsluiting.

Het insluiten van meerdere video&#39;s op dezelfde pagina wordt ondersteund op tablets en mobiele apparaten. In de meeste gevallen kan slechts één video tegelijk worden afgespeeld. Wanneer een gebruiker een video begint af te spelen en vervolgens een andere video probeert af te spelen, wordt de eerste video automatisch gepauzeerd. De video die automatisch is gepauzeerd onthoudt de huidige afspeeltijd, zodat de gebruiker er altijd weer naar kan terugkeren en het afspelen kan hervatten. De enige uitzondering op deze regel is de Chrome-browser op Android 4.x-apparaten, die video&#39;s parallel kunnen afspelen.

**Pop-upmodus**

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van het apparaat wordt gewijzigd.

Deze modus wordt het meest gebruikt voor mobiele apparaten. De webpagina laadt de viewer met behulp van `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een HTML-pagina uit de doos te gebruiken voor de pop-upbewerkingsmodus. Het wordt geroepen [!DNL VideoViewer.html] en het wordt gevestigd onder [!DNL html5/] subfolder van uw standaard plaatsing IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Insluitmodus met vaste grootte en responsieve insluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt normaal gesproken slechts een deel van het onroerend goed van de webpagina in beslag.

Het primaire gebruiksgeval zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en ook responsieve ontwerppagina&#39;s die de lay-out automatisch aanpassen afhankelijk van het apparaattype.

Insluiten met vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na de eerste keer laden. Dit is de beste keuze voor webpagina&#39;s met een statische pagina-indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als gevolg van de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van de viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze methode zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval komt het meest voor bij webpagina&#39;s die een responsief ontwerplay-outframework gebruiken, zoals Bootstrap, Foundation, enzovoort.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt, vult de viewer alleen dat gebied `DIV`en volgt deze het formaat dat wordt aangegeven door de indeling van de webpagina. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de grootte van het venster van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Zorg ervoor dat u de viewer-API opneemt voordat u deze kunt gebruiken [!DNL FlyoutViewer.js]. Het [!DNL FlyoutViewer.js] bestand bevindt zich in de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop de IS-Viewers zijn geïnstalleerd.

Relatief pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>U moet alleen verwijzen naar het JavaScript- `include` hoofdviewerbestand op uw pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK- `Utils.js` bibliotheek die door de viewer is geladen vanuit het `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet `includes` op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript dat door de viewer op de pagina wordt `include` gebruikt, maakt u de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   Controleer of de functie Volledig scherm goed werkt in Internet Explorer. Controleer of het DOM geen andere elementen bevat die een hogere stapelvolgorde hebben dan het DIV-bestand voor de plaatsaanduiding.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7videoviewer` top-level CSS klasse in absolute eenheden te verklaren, of door de bepaling te gebruiken `stagesize`.

   De grootte in CSS kan op de HTML- pagina, of in een douaneCSS dossier van de kijker worden gezet, dat later aan een kijker vooraf ingesteld verslag in het Publiceren Scene7 Systeem wordt toegewezen of uitdrukkelijk gebruikend een stijlbevel wordt overgegaan.

   Zie Video-viewer [](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in een HTML-pagina:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt bepaling of in de kijker vooraf ingestelde verslag in Scene7 het Publiceren Systeem plaatsen, of het uitdrukkelijk overgaan met de kijker initialisatiecode met `stagesize` `params` inzameling, of als API vraag zoals die in de de verwijzingssectie van het Bevel wordt beschreven, zoals in het volgende:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.VideoViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minimaal een `containerId` veld hebben met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die door de viewer worden ondersteund. In dit geval moet ten minste de URL van de afbeeldingsserver worden doorgegeven als `params` eigenschap, de URL van de videoserver als `serverUrl` eigenschap en het eerste element als `videoserverurl` `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Roep voor maximale compatibiliteit de `init()` methode aan vlak voor de afsluitende `BODY` tag of voor de body- `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met een `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van minimaal noodzakelijke configuratieopties aan de constructor en het aanroepen van de `init()` methode. In dit voorbeeld `videoViewer` wordt ervan uitgegaan dat dit de viewerinstantie is, `s7viewer` de naam van de plaatsaanduiding is `DIV`, [!DNL http://s7d1.scene7.com/is/image/] de URL van de afbeeldingsserver is, de URL van de videoserver [!DNL http://s7d1.scene7.com/is/content/] en [!DNL Scene7SharedAssets/Glacier_Climber_MP4] het element is.

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Video-viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

Met responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een of andere flexibele indeling die de runtimegrootte van de container van de viewer bepaalt `DIV`. In dit voorbeeld wordt ervan uitgegaan dat de webpagina de container van de viewer 40% van de venstergrootte van de webbrowser laat `DIV` innemen, zodat de hoogte onbeperkt blijft. De HTML-code van de webpagina ziet er als volgt uit:

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

Het toevoegen van de viewer aan een dergelijke pagina lijkt sterk op het insluiten van een vaste grootte. het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Voeg container toe `DIV` aan de bestaande &quot;houder&quot; `DIV`. De volgende code is een volledig voorbeeld. U kunt zien hoe de grootte van de viewer verandert wanneer de browser wordt aangepast en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Responsief ontwerpinsluiting met gedefinieerde breedte en hoogte**

Bij responsieve ontwerpinsluiting met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. het verstrekt zowel grootte aan de &quot;houder&quot; `DIV` en centreert het in het browser venster. Bovendien stelt de webpagina de grootte van het element `HTML` en het `BODY` element in op 100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Insluiten met behulp van op Setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Met die API neemt constructor geen parameters en worden configuratieparameters opgegeven met behulp van `setContainerId()`, `setParam()`en `setAsset()` API-methoden met afzonderlijke JavaScript-aanroepen.

In het volgende voorbeeld wordt het insluiten van een vaste grootte met een setter-API geïllustreerd:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```

