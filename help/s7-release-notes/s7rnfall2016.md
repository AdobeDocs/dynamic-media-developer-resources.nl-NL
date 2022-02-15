---
title: Scene7 Fall 2016 Release
description: '"De nieuwste release bevat informatie over de Adobe Scene7 Fall 2016, een onderdeel van de Adobe Experience Manager-oplossing in de Adobe Experience Cloud."'
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Scene7 Fall 2016 Release{#scene-fall-release}

De meest recente release bevat de Adobe Scene7 Fall 2016-oplossing, die deel uitmaakt van de Adobe Experience Manager-oplossing in de Adobe Experience Cloud.

## Scene7 Fall 2016 Release {#topic-791cdf80f91e457fbb63bfedf79f5a94}

De meest recente releaseopmerkingen voor [!DNL Adobe Scene7] Vrijgavedeel van de Fall 2016 [!DNL Adobe Experience Manager] in de [!DNL Adobe Experience Cloud].

* [Algemeen](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Viewers (afbeeldingen met 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Viewers (afbeelding met 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Viewers (afbeelding met 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 and Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Algemeen {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe is opgetogen om de beschikbaarheid van HTTP/2 levering van inhoud aan te kondigen met het algemene voordeel van betere prestaties.

Zie [HTTP2 Veelgestelde vragen over inhoud](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Voor volledige documentatie raadpleegt u [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nieuwe functies, verbeteringen en foutoplossingen**

* Functie voor videorecut is verwijderd uit [!DNL Adobe Scene7 Publishing System] gebruikersinterface.
* Waar nodig en mogelijk verificatie toegevoegd aan alle Scene7-servlets
* Opgeloste problemen in verband met de lijstweergave in de prullenbak.
* Verwijderd **Dynamic Media Classic (Scene7)-beheerder maken** door beveiligingsproblemen.
* FTP WebAdmin ondersteunt nu OKTA-verificatie.
* Verwijderd de eigenschap van het standaardwachtwoord dat voor nieuwe gebruikers van het Portaal van Media werd gecreeerd.
* Bugfixatie die het tijdelijke wachtwoord impliceert dat werd geproduceerd toen een nieuwe gebruiker werd toegevoegd. Het wachtwoord voldoet niet aan de vereiste wachtwoordvereisten.
* Opgeloste problemen met WebAdmin-hoofdschijf vol.
* Bugfixatie waarbij een gebruiker wordt uitgeschakeld die niet onmiddellijk in de gebruikersinterface wordt weergegeven.
* Opgeloste problemen waarbij een gebruiker is verwijderd en die u later niet opnieuw hebt gemaakt.
* Bugfixatie met betrekking tot het welkomstbericht dat naar nieuwe Scene7-gebruikers is verzonden en waarbij geen verificatie is opgenomen voor het beheren van bepaalde instellingen.
* Opgeloste problemen waarbij een FTP-mappenlijst niet kan worden opgehaald als een map speciale tekens in de naam bevat.
* Configureer OKTA-serviceproviders voor Scene7-omgevingen.
* Toegevoegde ondersteuning voor Experience Cloud Org ID for Viewer Analytics.
* Implementeerde Scene7 SAML-consument.

## Viewers (afbeeldingen met 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Voor volledige documentatie raadpleegt u [Referentiehandleiding voor viewers](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Bugfixes voor afbeeldingen in 5.5.3**

* Compatibiliteit met RequireJS- en DOJO-bibliotheken.

   Geconsolideerde SDK JS-caching tijdens viewerimplementatie.

## Viewers (afbeelding met 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Voor volledige documentatie raadpleegt u [Referentiehandleiding voor viewers](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Bugfixes voor afbeeldingen in 5.5.2**

* Video kan niet worden afgespeeld in Internet Explorer 11 in Windows 7.
* `initialframe` had geen invloed op de staande modus op mobiele apparaten voor de HTML5 eCatalog.

## Viewers (afbeelding met 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Voor volledige documentatie raadpleegt u [Referentiehandleiding voor viewers](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Nieuwe functies, verbeteringen en foutoplossingen voor Image Serving 5.5.1**

* HTML5 eCatalog-viewer met zoekfunctie.
* Toegevoegde HLS-streaming video playback als standaardmethode voor het afspelen van video voor de meeste desktopsystemen. Op Flash gebaseerde HDS-videostreaming is nog steeds beschikbaar als alternatieve afspeeloptie.
* Extra ondersteuning voor apparaten met zowel muis- als aanraakinvoer via Chrome-browser.
* Ondersteuning voor Experience Cloud Org ID toegevoegd aan de integratie met Analytics.
* Werk de JavaScript-bibliotheek AppMeasurement bij naar versie 1.6.1.
* Extra ondersteuning voor oriëntatie van rechts naar links in de eCatalog-viewer.
* Probleem opgelost waarbij `tip=0,-1,0` heeft een fout veroorzaakt die buiten het bereik valt.

**Compatibiliteitsnotities**

* BlackBerry®

   * Incompatibiliteit met oudere AVS-sets. Clients moeten AVS-sets opnieuw uploaden om het afspelen mogelijk te maken.

* Algemeen

   * Schalen aan de browserzijde kan de interface en afbeeldingen vervagen wanneer de gebruiker inzoomt op de pagina. De opmaak van de gebruikersinterface kan ook onjuist worden weergegeven, afhankelijk van zoomen. Dit effect wordt op volledig scherm weergegeven.
   * Vanwege groottebeperking op mobiele apparaten gebruikt de gemengde Media Viewer een diabeweging om frames in ingesloten afbeeldingssets te wisselen in plaats van op de ingesloten stalenscomponent te tikken. De component is er als visuele indicator.
   * In Internet Explorer-browsers en sommige aanraakapparaten neemt de modus Volledig scherm niet het volledige apparaatscherm in beslag. In plaats daarvan wordt de grootte van de toepassing aangepast aan het browservenster.
   * De knop Sluiten werkt niet in iOS 8.0 en 8.1, maar komt niet meer voor in iOS 8.2

* Galaxy SIII

   * Geheugenlek gezien met Zoom- en eCatalog HTML5-viewers. Herhaalde navigatie door frames kan ertoe leiden dat de browser vastloopt.
   * Dubbeltik op de viewer kan ertoe leiden dat de hele pagina in- en uitzoomen in plaats van alleen de viewer waarvoor schaling aan de browserzijde is ingeschakeld.

* Galaxy S4

   * Apparaat gedetecteerd als tablet in de staande modus met Volledig scherm ingeschakeld in de browserinstellingen.

* Galaxy Nexus

   * Dubbeltik op de viewer kan ertoe leiden dat de hele pagina in- en uitzoomen in plaats van alleen de viewer waarvoor schaling aan de browserzijde is ingeschakeld.

* Galaxy Nexus 10 en Galaxy tablet

   * Een eCatalog met een onjuiste paginaspread met de stand Staand en Liggend.

* HTC mobiele apparaten

   * De mobiele apparaten van HTC tonen de bevindingen van Adobe aan dat het onvermogen om inheems knijpbeweging te onbruikbaar te maken een &quot;eigenschap&quot;van de omslag van HTML UI (HTC Sense) is. Door dit probleem kan de hele pagina worden ingezoomd wanneer een zoombeweging met een knijpbeweging in de viewer wordt gebruikt. Stel voor dat u dubbeltikt.
   * Pictogrammen met afbeeldingen met hyperlinks kunnen elkaar overlappen als de afbeeldingen met hyperlinks klein zijn en dicht bij elkaar liggen.

* HTML5-video

   * Internet Explorer 9: aangepaste posterafbeeldingen worden niet weergegeven.
   * `IntialBitRate` modifier wordt alleen ondersteund bij het afspelen van software-HLS en Flash HDS. Dit werkt niet wanneer het afspelen de native speler gebruikt.
   * OGG en WebM progressief afspelen worden momenteel niet ondersteund.
   * Schalen in de browser kan ertoe leiden dat de videospeler op een onjuiste grootte wordt weergegeven (inclusief de weergave-instellingen van het besturingsvenster van Windows OS).
   * Videozoekopdrachten waarbij gebruik wordt gemaakt van HLS-streaming op Safari kunnen inconsistent zijn.

* Internet Explorer

   * De modus Kwarten wordt momenteel niet ondersteund.
   * De compatibiliteitsmodus wordt momenteel niet ondersteund.
   * Internet Explorer op mobiel wordt momenteel niet ondersteund.

* iOS

   * Grote eCatalogs kunnen browser ertoe leiden vastloopt op iPad 2.
   * iPhone 6+ telefoons worden door de kijkers als tabletten gedetecteerd.

* Safari

   * Safari 6.1 of hoger: Instellingen voor Internet Plug-ins kunnen het afspelen van Flash-video voorkomen.
   * Video &#39;seek&#39; met gebruik van HLS-streaming op Safari kan inconsistent zijn.
   * Kan niet zoeken tot einde van video in Safari 6 met gebruik van HLS-streaming.

**Bekende problemen en beperkingen**

* De opties van de Beeldserver van `iscommands` worden niet toegevoegd aan de `req=set` aanvraag door ontwerp. Modifiers die alleen van invloed zijn op de beeldweergave, werken prima. Modifiers die van invloed zijn op de grootte, moeten in een complex element worden gebruikt. Bijvoorbeeld:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flyout] IE9 blijft soms op het scherm nadat u de muis hebt uitgeschakeld.
* Schalen in de browser leidt tot een onjuiste formaatwijziging.
* iPad 2: Grote eCatalog-elementen crashen Safari op iOS.
* Alle viewers

   * Watermerken, verduistering en vergrendeling worden niet ondersteund.
   * Voorinstellingen voor afbeeldingen worden niet ondersteund.
   * Viewer toevoegen aan of verwijderen uit het DOM met `display:none` CSS of door het dynamisch los te koppelen van het bovenliggende knooppunt wordt momenteel niet ondersteund.

* HTML5 Alle viewers

   * Het insluiten van een viewer in een tabel kan resulteren in een onjuiste grootte of plaatsing van de viewer in een niet-native modus voor volledig scherm. U kunt beter DIV&#39;s gebruiken.
   * Parameters met expliciete instantienamen in de code moeten instantienamen in de URL ook overschrijven (bijvoorbeeld `zoomView.iconfeffect=0`).
   * Uitsnijden van de opdracht Afbeeldingsserver wordt momenteel niet ondersteund.
   * De knop Sluiten werkt alleen als de viewer is geopend in het onderliggende venster.
   * De `iscommands` modifier biedt geen ondersteuning voor wijzigingstoetsen voor afbeeldingsservers die de afbeeldingsgrootte beïnvloeden.

* HTML5 eCatalog

   * Als u naar een andere HTML-pagina navigeert en zo nu en dan terugkeert, wordt de viewer teruggezet naar de eerste pagina.
   * Paginalay-out wordt soms onjuist weergegeven na het roteren van het iOS-apparaat. Als u naar de pagina zoomt, wordt de indeling gecorrigeerd.
   * Interne koppelingen verwijzen alleen naar de meest linkse pagina in spreads met meerdere pagina&#39;s. Heeft invloed op mobiele apparaten in de staande modus.
   * InitalFrame koppelt alleen aan de meest linkse pagina in spreads met meerdere pagina&#39;s. Heeft invloed op mobiele apparaten in de staande modus.
   * Vanwege beperkingen van de browser is de afdrukfunctie niet beschikbaar in IE9.

* HTML5 GemengdMedia

   * Afspelen van soundtrack wordt niet ondersteund.

* HTML5 Sociaal

   * Als u de miniaturen op de juiste wijze wilt weergeven in de uitgaande e-mail, `serverurl` modifier moet een absolute URL hebben.

* HTML5-video

   * Er kan een fout met betrekking tot de maximale grootte optreden voor de posterafbeelding. Bedrijf moet de limietinstelling voor Publiceren van afbeeldingsserver verhogen.
   * Videobijschriften vereisen een bedrijfsregels als het hosten van de HTML-pagina wordt verzorgd door een externe server (niet door een Scene7-server). Neem contact op met de ondersteuning van Adobe.
   * Bij het bijhouden van analyses kan een onjuist afspeelpercentage worden gerapporteerd als gevolg van buffering
   * Zwart frame in plaats van posterafbeelding wordt mogelijk weergegeven op iPad- of Android™-apparaten.
   * Het zwarte frame kan op het scherm opvlammen tijdens het laden van de viewer op iPad- of Android™-apparaten.
   * Zwarte randen worden weergegeven aan de zijde van de component VideoPlayer wanneer de achtergrond op iPad-apparaten is ingesteld op wit/transparant.
   * Het laatste videoframe kan vervormd zijn op iPad met iOS 7.
   * Soms treedt macroblokkering op tijdens het zoeken naar video&#39;s in de streamingmodus HLS in Chrome-, Firefox- en Internet Explorer-browsers.
      * Posterafbeelding wordt mogelijk niet voor de eerste keer weergegeven in de Microsoft® Edge-browser.
      * Posterafbeelding kan na het laden van de video in Internet Explorer 9 worden verborgen wanneer progressief afspelen wordt gebruikt.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

De gebruikershandleiding bevindt zich in de map Adobe HTML5 Viewer SDK van de client-installatiemap. Component API-documentatie vindt u in de submap docs van de clientinstallatie.

**Bugfixes voor 3.0.2**

* VideoPlayer - Video kan niet worden afgespeeld in Internet Explorer 11 in Windows 7.
* Inhoudsopgave -  `initialframe` heeft geen invloed op de staande modus op mobiele apparaten voor de HTML5 eCatalog-viewer.

**Nieuwe functies, verbeteringen en foutoplossingen voor 3.0.1**

* Algemeen

   * Toegevoegde HLS-streaming video playback als standaardmethode voor het afspelen van video voor de meeste desktopsystemen. Op Flash gebaseerde HDS-videostreaming is nog steeds beschikbaar als alternatieve afspeeloptie.
   * Toegevoegde componenten SearchManager, SearchPanel, SearchEffect, en SearchButton om nieuwe eigenschap van het Onderzoek in eCatalog kijkers te steunen.
   * Toegevoegde ondersteuning voor apparaten met zowel muis- als aanraakinvoer via de Chrome-browser.
   * Refactored Android™ versiedetectie om toekomstige versies van OS te steunen.
   * Voeg steun voor recht-aan-linkerrichtlijn in eCatalog-specifieke componenten van SDK toe.

* ControlBar

   * Optioneel schuiven toegevoegd voor inhoud ControlBar voor het geval deze niet in de beschikbare breedte past.

* FlyoutzoomView

   * Vast geval waarin `tip=0,-1,0` heeft een fout veroorzaakt die buiten het bereik valt.

**Compatibiliteitsnotities**

* Android™ 4.x

   * Als u de standaardinstelling wilt uitschakelen, moet blauw de volgende CSS-regel worden toegevoegd voor de component:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * Het afspelen van video kan worden gestopt wanneer bitsnelheidstreams in AVS-sets worden gewijzigd.

* Chroom

   * Om het even welke API vraag die component afdwingt herbouwt kan wegens interne caching van Chrome worden genegeerd.

* Galaxy SIII

   * Viewer kan soms niet in volledig scherm worden geladen.
   * Er is momenteel onvoldoende geheugen beschikbaar voor de weergave van het beeld.
   * Dubbeltikken op een beweging zoomt de viewer en de pagina in wanneer schaling aan de browserzijde actief is.

* Galaxy Nexus

   * Artefacten die over sommige meningscomponenten tonen.
   * Dubbeltikken op een beweging zoomt de viewer en de pagina in wanneer schaling aan de browserzijde actief is.

* iPad 3

   * De iPad 3 heeft een native resolutie van 2048 x 1536. Deze resolutie kan weergaveproblemen veroorzaken als de publicatie van het bedrijf IS, de afbeeldingsgroottebeperking lager is ingesteld.

* iPhone4

   * Pictogram voor opnieuw afspelen wordt na het schuiven door de pagina vervangen door het afspeelpictogram.

* Internet Explorer

   * Op IE 10 en oudere modus Volledig scherm neemt deze modus niet het volledige scherm in beslag, maar past deze de toepassing aan de grootte van het browservenster aan.
   * De rendermodus Kwartels wordt niet ondersteund.
   * Internet Explorer op mobiel wordt momenteel niet ondersteund.
   * Util.js kan er niet in slagen om te laden als asynchroon inbegrepen.
   * Het pictogram IconEffect blokkeert klikgebeurtenissen op componenten SpinView en ZoomView.

* Geïntegreerde apparaatvideospelers

   * Het in lagen plaatsen van UI-componenten via VideoPlayer wordt niet ondersteund wanneer VideoPlayer wordt gebruikt om de native speler van het apparaat aan te roepen.
   * Het afspelen van video in de native modus is inconsistent in Safari 6.
   * Bij native afspelen wordt het pictogram voor opnieuw afspelen vervangen door het afspeelpictogram na het schuiven van de pagina.

* Aanraakapparaten

   * De modus Volledig scherm neemt niet het volledige apparaatscherm in beslag, maar past de grootte van de toepassing aan het browservenster aan.
   * Aangepaste cursors werken niet op aanraakapparaten.
   * Paginaschaling op aanraakapparaten wordt momenteel niet ondersteund. Voor het insluiten van HTML5-viewers is de meta-tag viewport met de juiste instellingen vereist.

* Xoom

   * Dubbeltikken op een beweging zoomt de viewer en de pagina in wanneer schaling aan de browserzijde actief is.

**Bekende problemen en beperkingen**

* Alle componenten

   * In versie 2.7.2 en eerdere versies zijn enkele componenten aan het DOM toegevoegd met `insertBefore()` API. Als gevolg hiervan worden deze componenten onder aan de stapelvolgorde geplaatst, ongeacht wanneer de componentinstantie wordt gemaakt ten opzichte van andere componenten. Met versie 2.8.1 gebruiken alle componenten `appendChild()` API nu, wat betekent dat de component stapelvolgorde zou overeenkomen met de volgorde waarin de instantie wordt gemaakt.

   * Gebruiken `iscommand` geen ondersteuning voor het instellen van de indeling voor alfakanalen van de afbeelding. Component gebruiken `FMT` in plaats daarvan.
   * Eigenschap voor CSS-transformatie wordt momenteel niet ondersteund.

* Aanraakapparaten

   * Met een knijpbeweging op aanraakapparaten wordt geen zoomgebeurtenis gegenereerd

* Container

   * Rand, opvulling en marges op de container worden niet ondersteund. Adobe stelt voor stijlelementen toe te voegen aan bovenliggende DIV.
   * U moet expliciet de containergrootte instellen, anders kan de grootte van de componenten juist zijn.

* Afdrukcomponent

   * Vanwege beperkingen van de browser kan de afdrukcomponent in Internet Explorer 9 de inhoud op het papier mogelijk niet correct schalen.

* component IconEffect

   * IconEffect genereert een scriptfout in Internet Explorer als `autohide` is uitgeschakeld (ingesteld op `0`).

* Component ImageMapEffect

   * Vertraging met pictogram voor verplaatsen bij het pannen van een afbeelding in een weergavecomponent.

* De component MediaSet

   * Voor inline-elementen wordt dezelfde codering aangevraagd als voor de URL.

* component NavigationView

   * De component ondersteunt momenteel geen formaatwijziging.

* PageScrubber-component

   * Wanneer in iPhone 5 de PageScrubber-ballon op tekst is ingesteld, worden artefacten weergegeven wanneer de knop langs de track wordt verplaatst. Gebruiken `-webkit-background-clip: content;` in de stijl werkt dit rond de uitgave.

* Component SpinView

   * SpinView lijkt soms te bevriezen na een veegbeweging en het apparaat te roteren terwijl de afbeelding draait.

* De component Stalen

   * Als u een buiten-de-grenzenstaal selecteert, worden twee hooglichten weergegeven.
   * Automatisch schuiven met `selectSwatch()` onjuist werken.

* VideoPlayer

   * Videoframe wordt niet bijgewerkt als de zoekopdracht is ingesteld op 100 procent en de fallback is ingesteld op auto.
   * Het af en toe blokkeren van macro&#39;s kan voorkomen tijdens videoonderzoek op HLS het stromen wijze in Chrome, browsers Firefox, en Internet Explorer.
   * Posterafbeelding wordt mogelijk niet voor de eerste keer weergegeven in de Microsoft® Edge-browser.
   * Posterafbeelding kan na het laden van de video in Internet Explorer 9 worden verborgen wanneer progressief afspelen wordt gebruikt.

## Dynamic Media Image Serving 6.3.2 and Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Hulpprogramma IC - `downsample2x2` markering wordt niet meer ondersteund. Deze vlag was een slechte kwaliteit 2x2 downsampler die niet meer door IPS wordt gebruikt.
* CORS-header - De CORS-header is momenteel geconfigureerd voor `/is/content/` verzoeken.
