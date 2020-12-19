---
description: De gemengde Kijker van Media is een media kijker. De klasse biedt ondersteuning voor mediasets die afbeeldingen, stalensets, centrifuges, video's en adaptieve videosets bevatten.
keywords: responsive
seo-description: De gemengde Kijker van Media is een media kijker. De klasse biedt ondersteuning voor mediasets die afbeeldingen, stalensets, centrifuges, video's en adaptieve videosets bevatten.
seo-title: Gemengde media
solution: Experience Manager
title: Gemengde media
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2681'
ht-degree: 0%

---


# Gemengde media{#mixed-media}

De gemengde Kijker van Media is een media kijker. De klasse biedt ondersteuning voor mediasets die afbeeldingen, stalensets, centrifuges, video&#39;s en adaptieve videosets bevatten.

Een miniatuur onder aan de viewer geeft elk element in de mediaset weer, samen met de aanduiding voor het type element. Wanneer een element in een stalenset is geselecteerd, wordt een tweede rij stalen weergegeven waarmee u kleurvariaties kunt selecteren in de stalenset. Afbeeldingen en stalensetelementen bieden ondersteuning voor zoomen in continue of inline modus. centrifuges ondersteunen zowel zoomen als draaien. Video&#39;s en Adaptieve videosets ondersteunen alle standaardbesturingselementen voor afspelen, mits optionele, gesloten bijschriften boven op de video-inhoud worden weergegeven. Een gebruiker kan op elk gewenst moment overschakelen naar volledig scherm door op de knop Volledig scherm te klikken. De viewer heeft een optionele knop Sluiten. Het is ontworpen voor gebruik op desktops en mobiele apparaten.

De gemengde Kijker van Media gebruikt het stromen HTML5 videoplayback in formaat HLS in zijn standaardconfiguratie wanneer het onderliggende systeem dat steunt. Op systemen die geen ondersteuning bieden voor HTML5-streaming, valt de viewer terug naar progressieve HTML5-video.

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

Viewer type 505.

Zie [Systeemvereisten en -vereisten](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## De gemengde Kijker van Media {#section-f21ac23d3f6449ad9765588d69584772} gebruiken

De gemengde Kijker van Media vertegenwoordigt een belangrijkste dossier JavaScript en een reeks helperdossiers (één enkele omvat JavaScript met alle componenten van SDK van de Kijker die door deze bepaalde kijker worden gebruikt, activa, CSS) door de kijker in runtime wordt gedownload.

U kunt de gemengde Kijker van Media in pop-up wijze gebruiken gebruikend productie-klaar HTML- pagina die van IS-Kijkers wordt voorzien. U kunt de viewer ook gebruiken in de ingesloten modus, waar deze is geïntegreerd in een doelwebpagina met behulp van de gedocumenteerde API.

Het configureren en toewijzen van een skin aan de viewer is vergelijkbaar met die van andere viewers. Alle skins worden gemaakt door middel van aangepaste CSS.

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactie met gemengde Media Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

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
   <td colname="col2"> <p>In <span class="codeph"> ononderbroken </span> zoommodus zoomt u op één niveau totdat de maximale vergroting is bereikt. De volgende dubbele tikbeweging wordt dan weer ingesteld op de begintoestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanraken en vasthouden </p> </td> 
   <td colname="col2"> <p> Als u de zoommodus <span class="codeph"> inline </span> inschakelt, wordt de ingezoomde afbeelding geactiveerd. </p> </td> 
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
   <td colname="col2"> <p> Als de afbeelding zich in een herstelstatus bevindt, verandert de verticale weergavehoek voor het geval dat een multidimensionale centrifugeset wordt gebruikt. In een eendimensionale centrifuge of wanneer een multidimensionale centrifuge zich op de laatste of de eerste as bevindt, zodat verticale veeggebaren niet tot een verandering van de verticale weergavehoek leidt, wordt de beweging uitgevoerd door een native paginaschuiving. </p> <p> Als het huidige element een gecentreerde of afbeeldingsset is en u op de afbeelding hebt ingezoomd, wordt de afbeelding verticaal verplaatst. Als de afbeelding naar de weergavegrens wordt verplaatst en de veegbeweging nog steeds in die richting wordt uitgevoerd, wordt de beweging op de pagina zelf uitgevoerd. </p> <p> Als de beweging binnen het stalengebied wordt uitgevoerd, wordt een native paginaschuiving uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

De viewer ondersteunt ook aanraakinvoer en muisinvoer op Windows-apparaten met aanraakscherm en muis. Deze ondersteuning is echter alleen beschikbaar voor Chrome-, Internet Explorer 11- en Edge-webbrowsers.

Deze viewer is volledig toegankelijk via het toetsenbord.

Zie [Toegankelijkheid en navigatie op toetsenbord](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Gemengde Media-viewer insluiten {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschillende webpagina&#39;s hebben verschillende vereisten voor viewergedrag. Soms biedt een webpagina een koppeling die de viewer in een apart browservenster opent wanneer erop wordt geklikt. In andere gevallen moet u de viewer rechts insluiten op de hostpagina. In het laatste geval heeft de webpagina mogelijk een statische paginalay-out of wordt een responsief ontwerp gebruikt dat op verschillende apparaten of voor verschillende venstergrootten van de browser anders wordt weergegeven. Om aan deze behoeften tegemoet te komen, ondersteunt de viewer drie primaire bewerkingsmodi: pop-up, vaste grootte het inbedden, en ontvankelijk ontwerp het inbedden.

## Info over pop-upmodus {#section-77d5aa03b8b94566958a179b1a2cd474}

In de pop-upmodus wordt de viewer geopend in een apart venster of tabblad van een webbrowser. Het neemt het volledige browservenstergebied en past zich aan voor het geval de browser wordt aangepast of de oriëntatie van een mobiel apparaat wordt gewijzigd.

Pop-upmodus is de meest gebruikte voor mobiele apparaten. De webpagina laadt de viewer met behulp van `window.open()` JavaScript-aanroep, correct geconfigureerd `A` HTML-element of een andere geschikte methode.

Het wordt aanbevolen een HTML-pagina uit de doos te gebruiken voor de pop-upbewerkingsmodus. In dit geval wordt deze [!DNL MixedMediaViewer.html] genoemd en bevindt deze zich in de submap [!DNL html5/] van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

U kunt visuele aanpassing bereiken door aangepaste CSS toe te passen.

Hieronder ziet u een voorbeeld van HTML-code waarmee de viewer in een nieuw venster wordt geopend:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Over een vaste grootte en responsieve ontwerpinsluiting {#section-ec86b100ba5943d0b16694268520bbde}

In de ingesloten modus wordt de viewer toegevoegd aan de bestaande webpagina, waar al inhoud van de klant beschikbaar is die geen betrekking heeft op de viewer. De viewer neemt doorgaans slechts een deel van het onroerend goed van een webpagina in beslag.

De belangrijkste gebruiksgevallen zijn webpagina&#39;s die zijn georiënteerd op desktops of tabletapparaten, en ook responsieve ontwerppagina&#39;s die de lay-out automatisch aanpassen, afhankelijk van het apparaattype.

De insluiting met een vaste grootte wordt gebruikt wanneer de viewer de grootte niet wijzigt na het laden. Dit is de beste keuze voor webpagina&#39;s met een statische indeling.

Bij het insluiten van responsieve ontwerpen wordt ervan uitgegaan dat de viewer tijdens runtime mogelijk de grootte moet wijzigen als reactie op de wijziging van de grootte van de container `DIV`. De meest gebruikte optie is het toevoegen van een viewer aan een webpagina die een flexibele pagina-indeling gebruikt.

In de responsieve ontwerpinsluitingsmodus werkt de viewer anders, afhankelijk van de manier waarop de container `DIV` door de webpagina wordt verkleind. Als de webpagina alleen de breedte van de container `DIV` instelt en de hoogte onbeperkt laat, kiest de viewer automatisch de hoogte op basis van de hoogte-breedteverhouding van het element dat wordt gebruikt. Deze functionaliteit zorgt ervoor dat het element perfect in de weergave past zonder opvulling aan de zijkanten. Dit gebruiksgeval is het meest voor Web-pagina&#39;s die ontvankelijke kaders van de ontwerplay-out zoals Bootstrap, Stichting, etc. gebruiken.

Anders, als de Web-pagina zowel de breedte als de hoogte voor de container `DIV` van de kijker plaatst, vult de kijker enkel dat gebied en volgt de grootte die de Web-pagina lay-out verstrekt. Een goed voorbeeld is het insluiten van de viewer in een modale overlay, waarbij de grootte van de overlay wordt aangepast aan de venstergrootte van de webbrowser.

## Vaste grootte insluiten {#section-17d162f76ffa4804b27928f51e7bea1d}

U voegt de viewer als volgt toe aan een webpagina:

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.
1. De container `DIV` definiëren.
1. De viewergrootte instellen.
1. De viewer maken en initialiseren.

1. Het JavaScript-bestand van de viewer toevoegen aan uw webpagina.

   Voor het maken van een viewer moet u een scripttag aan de HTML-kop toevoegen. Voordat u de viewer-API kunt gebruiken, moet u [!DNL MixedMediaViewer.js] opnemen. Het [!DNL MixedMediaViewer.js]-bestand bevindt zich in de submap [!DNL html5/js/] van uw standaard IS-Viewers-implementatie:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

U kunt een relatief pad gebruiken als de viewer wordt geïmplementeerd op een van de Adobe Scene7-servers en vanuit hetzelfde domein wordt aangeboden. Anders geeft u een volledig pad op naar een van de Adobe Scene7-servers waarop IS-Viewers zijn geïnstalleerd.

Het relatieve pad ziet er als volgt uit:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Verwijs alleen naar het JavaScript-bestand `include` van de hoofdviewer op de pagina. U moet niet verwijzen naar extra JavaScript-bestanden in de webpaginacode die door de logica van de viewer in runtime kunnen worden gedownload. Verwijs met name niet rechtstreeks naar de HTML5 SDK `Utils.js`-bibliotheek die door de viewer is geladen vanaf het contextpad `/s7viewers` (de zogeheten geconsolideerde SDK `include`). De reden hiervoor is dat de locatie van `Utils.js` of vergelijkbare runtimeviewerbibliotheken volledig wordt beheerd door de logica van de viewer en dat de locatie verandert tussen de viewerreleases. Adobe houdt oudere versies van de secundaire viewer `includes` niet op de server.
>
>
>Als u dus een directe verwijzing naar een secundair JavaScript `include` op de pagina plaatst, wordt de viewerfunctionaliteit in de toekomst verbroken wanneer een nieuwe productversie wordt geïmplementeerd.

1. De container DIV definiëren.

   Voeg een leeg DIV-element toe aan de pagina waarop u de viewer wilt weergeven. Voor het DIV-element moet de id zijn gedefinieerd, omdat deze id later wordt doorgegeven aan de viewer-API. De grootte van het DIV-bestand wordt bepaald door CSS.

   De plaatsaanduiding DIV is een gepositioneerd element, wat betekent dat de CSS-eigenschap `position` is ingesteld op `relative` of `absolute`.

   Controleer of de functie Volledig scherm goed werkt in Internet Explorer. Controleer of het DOM geen andere elementen bevat die een hogere stapelvolgorde hebben dan het DIV-bestand voor de plaatsaanduiding.

   Hieronder ziet u een voorbeeld van een gedefinieerd plaatsaanduiding DIV-element:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. De viewergrootte instellen

   In deze viewer worden miniaturen weergegeven wanneer u werkt met sets met meerdere items. Op desktopsystemen worden miniaturen onder de hoofdweergave geplaatst. Tegelijkertijd kan de viewer het hoofdelement tijdens runtime wisselen met de API `setAsset()`. Als ontwikkelaar hebt u controle over de manier waarop de viewer het miniatuurgebied onderaan beheert wanneer het nieuwe element slechts één item bevat. Het is mogelijk de grootte van de buitenste viewer ongewijzigd te laten en de hoogte van de hoofdweergave te verhogen en het gebied met miniaturen in beslag te nemen. U kunt ook de grootte van de hoofdweergave statisch houden en het buitenste viewergebied samenvouwen, zodat de inhoud van de webpagina omhoog kan worden verplaatst en vervolgens de ruimte voor de vrije pagina gebruiken die bij de miniaturen blijft.

   Als u de buitenste grenzen van de viewer ongewijzigd wilt laten, definieert u de grootte voor de CSS-klasse op hoofdniveau in absolute eenheden. `.s7mixedmediaviewer` Grootte in CSS kan rechts op de HTML-pagina worden geplaatst, of in een aangepast CSS-bestand van de viewer, dat later wordt toegewezen aan een viewer-voorinstellingsrecord in Scene7 Publishing System, of expliciet wordt doorgegeven met de opdracht style.

   Zie [Gemengde Media Viewer aanpassen](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) voor meer informatie over het opmaken van de viewer met CSS.

   Hieronder ziet u een voorbeeld van het definiëren van de statische buitenste viewergrootte in een HTML-pagina:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   U kunt het gedrag met een vast buitenste viewergebied op de volgende voorbeeldpagina zien. Wanneer u schakelt tussen sets, verandert de grootte van de buitenste viewer niet:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Als u de afmetingen van de hoofdweergave statisch wilt maken, definieert u de viewergrootte in absolute eenheden voor de binnenste SDK-component met behulp van `Container` CSS-kiezer of met de optie `.s7mixedmediaviewer .s7container`.`stagesize`

   Hieronder ziet u een voorbeeld van het definiëren van de viewergrootte voor de binnenste SDK-component `Container`, zodat de grootte van het hoofdweergavegebied niet wordt gewijzigd wanneer u van element verandert:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Op de volgende voorbeeldpagina ziet u het gedrag van de viewer met een vaste hoofdweergavegrootte. Wanneer u tussen sets schakelt, blijft de hoofdweergave statisch en wordt de inhoud van de webpagina verticaal verplaatst:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   U kunt de bepaling `stagesize` of in het vooraf ingestelde verslag van de kijker in het Publiceren van Scene7 Systeem plaatsen, of het uitdrukkelijk met de de initialisatiecode van de kijker met `params` inzameling overgaan, of als API vraag zoals die in de sectie van de Verwijzing van het Bevel van deze Hulp wordt beschreven, zoals in het volgende:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Een op CSS gebaseerde benadering wordt geadviseerd en in dit voorbeeld gebruikt.

1. De viewer maken en initialiseren.

   Wanneer u de bovenstaande stappen hebt uitgevoerd, maakt u een instantie van de klasse `s7viewers.MixedMediaViewer`, geeft u alle configuratiegegevens door aan de constructor en roept u `init()` methode aan voor een viewerinstantie. De informatie van de configuratie wordt overgegaan tot de aannemer als voorwerp JSON. Dit object moet minstens het veld `containerId` hebben dat de naam van de viewercontainer-id bevat en het geneste JSON-object `params` met configuratieparameters die de viewer ondersteunt. In dit geval moet voor het `params`-object ten minste de URL van de afbeeldingsserver worden doorgegeven als `serverUrl`-eigenschap, de URL van de videoserver als `videoserverurl`-eigenschap en het eerste element als `asset`-parameter. Met de op JSON gebaseerde initialisatie-API kunt u de viewer maken en starten met één coderegel.

   Het is belangrijk dat de viewercontainer aan het DOM wordt toegevoegd, zodat de viewercode het containerelement op basis van de id kan vinden. Sommige browsers stellen het samenstellen van DOM tot het einde van de webpagina uit. Voor maximale compatibiliteit roept u de methode `init()` aan vlak voor de afsluitingstag `BODY` of op de hoofdgebeurtenis `onload()`.

   Tegelijkertijd mag het containerelement niet noodzakelijkerwijs deel uitmaken van de webpaginalay-out. Het kan bijvoorbeeld worden verborgen met de stijl `display:none` die eraan is toegewezen. In dit geval vertraagt de viewer het initialisatieproces totdat de webpagina het containerelement weer in de layout plaatst. Wanneer dit gebeurt, wordt het laden van de viewer automatisch hervat.

   Hieronder ziet u een voorbeeld van het maken van een viewer-instantie, het doorgeven van de minimaal benodigde configuratieopties aan de constructor en het aanroepen van de methode `init()`. In het voorbeeld wordt ervan uitgegaan dat `mixedMediaViewer` de viewerinstantie is; `s7viewer` is de naam van de tijdelijke aanduiding `DIV`; [!DNL http://s7d1.scene7.com/is/image/] is de URL van de afbeeldingsserver; [!DNL http://s7d1.scene7.com/is/content/] is de URL van de videoserver; en [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] is het element:

```
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

```
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

Bij responsieve ontwerpinsluiting heeft de webpagina normaal gesproken een flexibele indeling die de runtimegrootte van de container van de viewer `DIV` bepaalt. In het volgende voorbeeld gaat u ervan uit dat de webpagina de container `DIV` van de viewer 40% van de venstergrootte van de webbrowser laat nemen, zodat de hoogte onbeperkt blijft. De HTML-code van de webpagina ziet er als volgt uit:

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

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Flexibele insluiting van grootte met gedefinieerde breedte en hoogte {#section-0a329016f9414d199039776645c693de}

In het geval van insluiting van flexibele grootte met gedefinieerde breedte en hoogte, is de opmaak van de webpagina anders. Het verstrekt beide grootte aan `"holder"` DIV en centreert het in het browser venster. Bovendien stelt de webpagina de grootte van het element `HTML` en `BODY` in op 100 procent.

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

## Insluiten met een op Setter gebaseerde API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

In plaats van JSON-gebaseerde initialisatie, is het mogelijk om op setter-gebaseerde API en no-args aannemer te gebruiken. Wanneer u deze API-constructor gebruikt, worden geen parameters gebruikt en worden configuratieparameters opgegeven met de API-methoden `setContainerId()`, `setParam()` en `setAsset()`, met aparte JavaScript-aanroepen.

In het volgende voorbeeld wordt het gebruik van insluiting op vaste grootte met een setter-API geïllustreerd:

```
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

