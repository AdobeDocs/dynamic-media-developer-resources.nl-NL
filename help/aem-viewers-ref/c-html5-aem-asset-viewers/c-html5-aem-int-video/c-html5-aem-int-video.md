---
description: Interactive Video Viewer is een videospeler die streaming en progressieve video afspeelt die zijn gecodeerd in de H.264-indeling.
seo-description: Interactive Video Viewer is een videospeler die streaming en progressieve video afspeelt die zijn gecodeerd in de H.264-indeling.
seo-title: Interactieve video
solution: Experience Manager
title: Interactieve video
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Interactieve video{#interactive-video}

Interactive Video Viewer is een videospeler die streaming en progressieve video afspeelt die zijn gecodeerd in de H.264-indeling.

In de viewer van de viewer worden ook interactieve productstalen weergegeven naast de video-inhoud. Zowel enkelvoudige video als Adaptieve videosets worden ondersteund. Het is ontworpen voor zowel desktopbrowsers als mobiele webbrowsers die HTML5-video ondersteunen. De viewer ondersteunt optionele Closed Captions die boven op video-inhoud worden weergegeven, navigatie in videohoofdstukken en gereedschappen voor sociaal delen. Het doel van deze viewer is om u te helpen bij het implementeren van een &#39;shoppable video&#39;-ervaring. Met andere woorden, gebruikers kunnen een staal selecteren dat is gekoppeld aan een bepaald videotijdgebied en worden omgeleid naar een Snelle weergave of een pagina met productdetails op de website van de klant.

Het viewertype is 510.

## Demo-URL&#39;s {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

en

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Systeemvereisten {#section-b7270cc4290043399681dc504f043609}

Zie [Systeemvereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Interactieve video-viewer gebruiken {#section-e6c68406ecdc4de781df182bbd8088b4}

De interactieve VideoKijker vertegenwoordigt een belangrijkste dossier JavaScript en een reeks helperdossiers (één enkele omvat JavaScript met alle componenten van de Kijker SDK die door deze bepaalde kijker, activa, en CSS worden gebruikt) die door de kijker in runtime worden gedownload.

De interactieve VideoKijker kan in pop-up wijze worden gebruikt gebruikend productie-klaar HTML- pagina die met de Kijkers van de Dienstende Beeld wordt verstrekt. Het kan ook worden gebruikt in de ingesloten modus, waar het wordt geïntegreerd in de doelwebpagina met behulp van de gedocumenteerde API.

Configuratie en skins zijn vergelijkbaar met die van de andere viewers die in deze handleiding worden beschreven. Alle skins toewijzen wordt bereikt door middel van aangepaste CSS (Cascading Style Sheets).

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) van de Configuratie en de verwijzing van het [Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met Interactive Video Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

De interactieve VideoKijker verstrekt een reeks standaardgebruikersinterfacecontroles voor videoplayback, zoals een Spel/pauze knoop, videoscrubber, videotijd bel, speeltijd/totale tijdindicator, volumeregelaar, het volledig-schermknoop, en gesloten titelknevel. Al deze besturingselementen worden rechtstreeks onder de hoofdweergave gegroepeerd in een besturingsbalk.

Op aanraakapparaten is de volumeregeling verborgen in de gebruikersinterface, omdat het alleen mogelijk is het volume te regelen met de hardwareknoppen van het apparaat.

Wanneer de viewer werkt in de pop-upmodus, is er geen knop voor een volledig scherm beschikbaar in de gebruikersinterface.

De viewer geeft een deelvenster weer met interactieve stalen rechts van het videoweergavegebied. De lijst met stalen wordt automatisch bijgewerkt tijdens het afspelen van de video, zodat de stalen die overeenkomen met het huidige videogebied worden weergegeven. Wanneer u op een staal klikt of erop tikt, wordt een handeling geactiveerd die tijdens het ontwerpen aan dat staal is gekoppeld. Afhankelijk van de manier waarop u deze instelt, kan de trigger worden omgeleid naar een andere pagina op de website of kan productinformatie worden teruggestuurd naar de webpaginalogica, die op zijn beurt weer kan leiden tot het openen van een Snelle weergave waarin verwante productinhoud wordt weergegeven.

Het is mogelijk om snel door de video-inhoud te navigeren wanneer videochaptering wordt geactiveerd. De videohoofdstukken worden getoond als tellers in het videoscrubberspoor en tonen de hoofdstuktitel en beschrijving op rollover (of op één enkele aanraking op aanraaksystemen). De klant kan &quot;zoeken&quot;aan een bepaald hoofdstuk door een hoofdstukteller te klikken of een borrel van de hoofdstukbeschrijving te tikken.

De viewer ondersteunt ook diverse gereedschappen voor het delen van sociale media. Ze zijn beschikbaar als één knop in de gebruikersinterface die wordt uitgevouwen tot een werkbalk voor delen wanneer de gebruiker erop klikt of tikt. De werkbalk voor delen bevat een pictogram voor elk type kanaal dat wordt ondersteund, zoals Facebook, Twitter, Delen via e-mail, Delen via code insluiten en delen van koppelingen. Wanneer gereedschappen voor delen via e-mail, insluiten of delen van koppelingen zijn geactiveerd, wordt in de viewer een modaal dialoogvenster weergegeven met een bijbehorend formulier voor gegevensinvoer. Wanneer Facebook of Twitter wordt aangeroepen, stuurt de viewer de gebruiker terug naar een standaarddialoogvenster voor delen via een sociale-mediaservice. Wanneer een gereedschap voor delen wordt geactiveerd, wordt het afspelen van video ook automatisch gepauzeerd. Delen van gereedschappen is niet beschikbaar in de modus Volledig scherm vanwege beveiligingsbeperkingen van de webbrowser.

De viewer is volledig toegankelijk via het toetsenbord. Zie [Toetsenbordtoegankelijkheid en navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Interactieve video-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactieve video-viewer is ontworpen om te worden ingesloten in de hostpagina. Een dergelijke webpagina kan een statische lay-out hebben of kan &quot;responsief&quot; zijn en anders worden weergegeven op verschillende apparaten of voor verschillende venstergrootten in de browser.

Om aan deze behoeften tegemoet te komen, ondersteunt de viewer twee primaire bewerkingsmodi: insluiten met een vaste grootte en responsieve insluiting.

**Insluitmodus van vaste grootte en responsieve ontwerpinsluitmodus**

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tablets, en responsieve, ontworpen pagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als gevolg van de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt verkleind `DIV`. Als op de webpagina alleen de breedte van de container wordt ingesteld `DIV`en de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke kaders van de lay-out van het Webontwerp zoals Boek, Stichting, etc. gebruiken.

Als de webpagina zowel de breedte als de hoogte voor de container van de viewer instelt, vult de viewer alleen dat gebied `DIV`en volgt deze het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

**Insluiten met vaste grootte**

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Zorg ervoor dat u de viewer-API opneemt voordat u deze kunt gebruiken [!DNL InterativeVideoViewer.js]. Het [!DNL InteractiveVideoViewer.js] bestand bevindt zich in de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en deze wordt aangeboden vanuit hetzelfde domein. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop de IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>U moet alleen verwijzen naar het JavaScript- `include` hoofdviewerbestand op uw pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK- `Utils.js` bibliotheek die door de viewer is geladen vanuit het `/s7viewers` contextpad (de zogenaamde geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer niet `includes` op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript dat door de viewer op de pagina wordt `include` gebruikt, maakt u de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container definiëren `DIV`.

   Voeg een leeg `DIV` element toe aan de pagina waarop u de viewer wilt weergeven. De id van het `DIV` element moet zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding `DIV` is een gepositioneerd element, wat betekent dat de `position` CSS-eigenschap is ingesteld op `relative` of `absolute`.

   De functie Volledig scherm werkt alleen correct in Internet Explorer als er zich geen andere elementen in de DOM bevinden die een hogere stapelvolgorde hebben dan de plaatsaanduiding `DIV`.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduidingselement `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. De viewergrootte instellen

   U kunt de statische grootte voor de kijker plaatsen door of het voor `.s7interactivevideoviewer` `stagesize` top-level CSS klasse in absolute eenheden te verklaren, of door bepaling te gebruiken.

   U kunt de grootte in CSS rechtstreeks op de HTML-pagina plaatsen, of in een aangepast CSS-bestand van de viewer, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in AEM Assets - op aanvraag of expliciet wordt doorgegeven met behulp van de `style` opdracht.

   Zie Interactieve video-viewer [](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) aanpassen voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van een statische viewergrootte in de HTML-pagina:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   U kunt de `stagesize` modifier in de vooraf ingestelde viewer instellen in AEM Assets, op aanvraag. Of u kunt het expliciet doorgeven met de initialisatiecode van de viewer met `params` verzameling of als een API-aanroep zoals beschreven in de sectie Opdrachtverwijzing, als volgt:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van een `s7viewers.InteractiveVideoViewer` klasse, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` de methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minimaal een `containerId` veld hebben met de naam van de viewercontainer-id en het geneste `params` JSON-object met configuratieparameters die door de viewer worden ondersteund.

   In dit geval moet voor het `params` object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl` eigenschap en het eerste element als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel, een URL van de videoserver die als `videoserverurl` eigenschap is doorgegeven, een eerste element als `asset` parameter en interactieve gegevens als `interactivedata` eigenschap. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Roep voor maximale compatibiliteit de `init()` methode aan vlak voor de afsluitende `BODY` tag of voor de body- `onload()` gebeurtenis.

   Het containerelement hoeft echter nog geen deel uit te maken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met een `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. In dat geval wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt uitgegaan van het volgende:

   * De viewer-instantie is `interactiveVideoViewer`.
   * De naam van de tijdelijke aanduiding `DIV` is `s7viewer`.
   * De URL van de afbeeldingsserver is `https://aodmarketingna.assetsadobe.com/is/image/`.
   * De URL van de videoserver is `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * De inhoud-URL is `https://aodmarketingna.assetsadobe.com/`.
   * Het element is `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * De interactieve gegevens zijn `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   De volgende code is een volledig voorbeeld van een triviale webpagina die de Interactive Video Viewer insluit met een vaste grootte:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsief ontwerpinsluiting met onbeperkte hoogte**

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

Het toevoegen van de viewer aan een dergelijke pagina is vergelijkbaar met de stappen voor het insluiten van een vaste grootte. Het enige verschil is dat u de viewergrootte niet expliciet hoeft te definiëren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container DIV definiëren.
1. De viewer maken en initialiseren.

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. Voeg de container DIV aan bestaande `"holder"` DIV toe. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

De volgende voorbeeldpagina illustreert het levensechte gebruik van responsieve ontwerpinsluiting met onbeperkte hoogte:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Responsief insluiten met gedefinieerde breedte en hoogte**

Bij responsieve insluiting waarbij breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt zowel grootte aan `"holder"` DIV als centrum het in het browser venster. Bovendien stelt de webpagina de grootte van het element `HTML` en het `BODY` element in op 100 procent.

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

De overige insluitingsstappen zijn identiek aan de stappen die worden gebruikt voor het insluiten van responsieve lagen met onbeperkte hoogte. Het resulterende voorbeeld is het volgende:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Insluiten met op setter gebaseerde API**

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Wanneer u deze API-constructor gebruikt, worden er geen parameters gebruikt en worden configuratieparameters opgegeven met behulp van `setContainerId()`, `setParam()`en `setAsset()` API-methoden met aparte JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting met een vaste grootte met de op een setter gebaseerde API geïllustreerd:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```

