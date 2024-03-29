---
title: Gemengde media
description: De gemengde Kijker van Media is een media kijker. De klasse biedt ondersteuning voor mediasets die afbeeldingen, stalensets, centrifuges, video's en adaptieve videosets bevatten.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2642'
ht-degree: 0%

---

# Gemengde media{#mixed-media}

De gemengde Kijker van Media is een media kijker. De klasse biedt ondersteuning voor mediasets die afbeeldingen, stalensets, centrifuges, video&#39;s en adaptieve videosets bevatten.

Een miniatuur onder aan de viewer geeft elk element in de mediaset weer, samen met de desbetreffende indicator voor het type element. Wanneer een element in een stalenset is geselecteerd, wordt een tweede rij stalen weergegeven waarmee u kleurvariaties kunt selecteren in de stalenset. Afbeeldingen en elementen in stalensets ondersteunen zoomen in de modus Continu of Inline. Spin-sets ondersteunen zowel zoomen als draaien. Video&#39;s en Adaptieve videosets ondersteunen alle standaardbesturingselementen voor afspelen, mits optionele, gesloten bijschriften boven op de video-inhoud worden weergegeven. Een gebruiker kan op elk moment overschakelen naar het volledige scherm door op de knop Volledig scherm te klikken. De viewer heeft een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

De gemengde Kijker van Media gebruikt HTML5 die videoplayback in formaat HLS in zijn standaardconfiguratie stromen wanneer het onderliggende systeem dat steunt. Op systemen die geen ondersteuning bieden voor HTML5-streaming, valt de viewer terug naar de progressieve HTML van de video.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 505.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Gemengde Media Viewer gebruiken {#section-f21ac23d3f6449ad9765588d69584772}

De gemengde Kijker van Media vertegenwoordigt een belangrijkste dossier JavaScript en een reeks helperdossiers (één enkele omvat JavaScript met alle componenten van SDK van de Kijker die door deze bepaalde kijker worden gebruikt, activa, CSS) door de kijker in runtime wordt gedownload.

U kunt de Gemengde Kijker van Media op pop-up wijze gebruiken gebruikend productie-klaar HTML pagina die van IS-Kijkers wordt voorzien. U kunt de viewer ook gebruiken in de ingesloten modus, waar deze met de gedocumenteerde API is geïntegreerd in een doelwebpagina.

Het configureren en toewijzen van een skin aan de viewer is vergelijkbaar met die van andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met de gemengde Media Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

De gemengde Kijker van Media steunt enig-aanraak en multi-aanrakingsgebaren die in andere mobiele toepassingen gemeenschappelijk zijn. Wanneer de viewer de veegbeweging van een gebruiker niet kan verwerken, stuurt deze de gebeurtenis door naar de webbrowser om een native paginaschuiving uit te voeren. Met deze functionaliteit kan de gebruiker door de pagina navigeren, zelfs als de viewer het grootste gedeelte van het apparaatschermgebied in beslag neemt.

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
   <td colname="col1"> <p>Dubbeltikken </p> </td> 
   <td colname="col2"> <p>Wanneer in <span class="codeph"> continu </span> zoommodus, zoomt in op één niveau totdat de maximale vergroting is bereikt, de volgende dubbele tikbeweging wordt weer ingesteld op de begintoestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanraken en vasthouden </p> </td> 
   <td colname="col2"> <p> Wanneer in <span class="codeph"> inline </span> Hiermee activeert u de zoommodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kneep </p> </td> 
   <td colname="col2"> <p>In de modus Continue zoom zoomt u in of uit op de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Wanneer het huidige element een centrifugeset is en de afbeelding zich in een herstelstatus bevindt, draait het door de centrifugeset. </p> <p> Als het huidige element een centrifugeerset of een afbeelding is en de afbeelding wordt ingezoomd, wordt de afbeelding horizontaal verplaatst. Als de afbeelding naar de weergavegrens wordt verplaatst en de veegbeweging nog steeds in die richting wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> <p> Hiermee bladert u door de lijst met stalen in de staalbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verticaal vegen of tikken </p> </td> 
   <td colname="col2"> <p> Als de afbeelding zich in een herstelstatus bevindt, verandert de verticale weergavehoek voor het geval dat een multidimensionale centrifugeset wordt gebruikt. In een eendimensionale centrifuge of wanneer een multidimensionale centrifuge zich op de laatste of de eerste as bevindt, zodat verticale veeggebaren niet tot een verandering van de verticale weergavehoek leidt, wordt de beweging uitgevoerd door een native paginaschuiving. </p> <p> Als het huidige element een centrifugeerset of een afbeelding is en u op de afbeelding hebt ingezoomd, wordt de afbeelding verticaal verplaatst. Als de afbeelding naar de weergavegrens wordt verplaatst en de veegbeweging nog steeds in die richting wordt uitgevoerd, wordt de beweging op de pagina zelf uitgevoerd. </p> <p> Als de beweging binnen het stalengebied wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter beperkt tot Chrome, Internet Explorer 11 en alleen Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toetsenbordtoegankelijkheid en -navigatie](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Gemengde Media Viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms bevat een webpagina een koppeling die de viewer in een apart browservenster opent als deze optie is geselecteerd. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, insluiten van vaste grootte en insluiten van responsieve ontwerpen.

## Pop-upmodus {#section-77d5aa03b8b94566958a179b1a2cd474}

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een uit-de-box HTML-pagina te gebruiken voor de pop-upbewerkingsmodus. In dit geval wordt [!DNL MixedMediaViewer.html] en bevindt zich binnen het [!DNL html5/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Vaste grootte en responsieve ontwerpinsluiting {#section-ec86b100ba5943d0b16694268520bbde}

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tabletapparaten, en ook responsieve ontwerppagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na de eerste keer laden. Deze handeling is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitmodus werkt de viewer anders, afhankelijk van de manier waarop de container van de webpagina wordt aangepast `DIV`. Als de webpagina alleen de breedte van de container instelt `DIV`Wanneer de hoogte onbeperkt blijft, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het gebruikte element. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het gemeenschappelijkst voor Web-pagina&#39;s die ontvankelijke ontwerplay-outkaders zoals Bootstrap of Stichting gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container van de kijker plaatst `DIV`, vult de viewer alleen dat gebied en volgt het formaat dat de webpaginalay-out biedt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

## Vaste grootte insluiten {#section-17d162f76ffa4804b27928f51e7bea1d}

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container definiëren `DIV`.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag toevoegen aan de kop van de HTML. Voordat u de viewer-API kunt gebruiken, moet u controleren of deze [!DNL MixedMediaViewer.js]. De [!DNL MixedMediaViewer.js] bestand bevindt zich onder de [!DNL html5/js/] submap van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Dynamic Media Classic-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Dynamic Media Classic-servers waarop IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. De viewergrootte instellen

   In deze viewer worden miniaturen weergegeven wanneer u werkt met sets met meerdere items. Op desktopsystemen worden miniaturen onder de hoofdweergave geplaatst. Tegelijkertijd kan de viewer het hoofdelement tijdens runtime wisselen met `setAsset()` API. Als ontwikkelaar hebt u controle over de manier waarop de viewer het miniatuurgebied onderaan beheert wanneer het nieuwe element slechts één item bevat. Het is mogelijk de grootte van de buitenste viewer ongewijzigd te laten en de hoogte van de hoofdweergave te verhogen en het gebied met miniaturen in beslag te nemen. U kunt ook de grootte van de hoofdweergave statisch houden en het buitenste viewergebied samenvouwen, zodat de inhoud van de webpagina omhoog kan gaan. Gebruik vervolgens de ruimte voor vrije pagina&#39;s die bij de miniaturen achterblijft.

   Als u de buitenste grenzen van de viewer ongewijzigd wilt laten, definieert u de grootte voor `.s7mixedmediaviewer` CSS-klasse op hoofdniveau in absolute eenheden. De grootte in CSS kan op de pagina van de HTML, of in een douanekijker CSS dossier worden gezet, en later aan een kijker vooraf ingestelde verslag in Dynamic Media Classic worden toegewezen, of uitdrukkelijk worden overgegaan gebruikend stijlbevel.

   Zie [Gemengde Media Viewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van de statische buitenste viewergrootte in een HTML-pagina:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt het gedrag met een vast buitenste viewergebied op de volgende voorbeeldpagina zien. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Als u de afmetingen van de hoofdweergave statisch wilt maken, definieert u de viewergrootte in absolute eenheden voor het binnenste `Container` SDK-component gebruiken `.s7mixedmediaviewer .s7container` CSS-kiezer of door gebruik te maken van `stagesize` modifier.

   Hieronder ziet u een voorbeeld van het definiëren van de viewergrootte voor de binnenzijde `Container` SDK-component, zodat het hoofdweergavegebied niet van grootte verandert wanneer u van element verandert:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Op de volgende voorbeeldpagina ziet u het gedrag van de viewer met een vaste hoofdweergavegrootte. Wanneer u tussen sets schakelt, blijft de hoofdweergave statisch en wordt de inhoud van de webpagina verticaal verplaatst:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   U kunt de `stagesize` in de viewervoorinstellingsrecord in Dynamic Media Classic, of geef deze expliciet door met de viewerinitialisatiecode met `params` verzameling. Of, als API vraag zoals die in de sectie van de Verwijzing van het Bevel van deze Hulp wordt beschreven, zoals in het volgende:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van `s7viewers.MixedMediaViewer` klasse, geef alle configuratieinformatie tot zijn aannemer door en roep `init()` op een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet ten minste het volgende bevatten `containerId` veld met de naam van de container-id van de viewer en het geneste veld `params` JSON-object met configuratieparameters die de viewer ondersteunt. In dit geval worden de `params` Het object moet ten minste de URL van de afbeeldingsserver hebben doorgegeven zoals `serverUrl` eigenschap, de URL van de videoserver doorgegeven als `videoserverurl` vastgoed en eerste actief als `asset` parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de `init()` methode vlak voor het sluiten `BODY` of op de hoofdtekst `onload()` gebeurtenis.

   Tegelijkertijd mag het containerelement nog niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld verborgen zijn met `display:none` stijl die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer deze actie wordt uitgevoerd, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de `init()` methode. In het voorbeeld wordt ervan uitgegaan `mixedMediaViewer` de viewer-instantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; [!DNL http://s7d1.scene7.com/is/image/] is de URL van de afbeeldingsserver; [!DNL http://s7d1.scene7.com/is/content/] de URL van de videoserver is, en [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] is het actief:

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

De volgende code is een volledig voorbeeld van een triviale webpagina die de Gemengde Media Viewer insluit met een vaste grootte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Responsief insluiten met onbeperkte hoogte {#section-056cb574713c4d07be6d07cf3c598839}

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
1. De viewer maken en initialiseren

Alle bovenstaande stappen zijn gelijk aan die bij het insluiten van de vaste grootte. De container DIV toevoegen aan het bestaande `"holder"` DIV. De volgende code is een volledig voorbeeld. U ziet hoe de grootte van de viewer verandert wanneer de grootte van de browser wordt gewijzigd en hoe de hoogte-breedteverhouding van de viewer overeenkomt met het element.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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

[Locatie van alternatieve demo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Flexibele insluiting van grootte met gedefinieerde breedte en hoogte {#section-0a329016f9414d199039776645c693de}

Als er insluiting in flexibele grootte is waarbij de breedte en hoogte zijn gedefinieerd, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreert het in het browser venster. Bovendien stelt de webpagina de grootte van de `HTML` en `BODY` tot 100 procent.

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
