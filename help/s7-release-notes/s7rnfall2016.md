---
description: De recentste versienota's voor de versie van Adobe Scene7 Fall 2016 - deel van de oplossing van de Adobe Experience Manager in de Adobe Marketing Cloud.
seo-description: De recentste versienota's voor de versie van Adobe Scene7 Fall 2016 - deel van de oplossing van de Adobe Experience Manager in de Adobe Marketing Cloud.
seo-title: Versie Scene7 herfst 2016
solution: Experience Manager
title: Versie Scene7 herfst 2016
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2263'
ht-degree: 0%

---


# Versie Scene7 herfst 2016{#scene-fall-release}

De recentste versienota&#39;s voor de versie van Adobe Scene7 Fall 2016 - deel van de oplossing van de Adobe Experience Manager in de Adobe Marketing Cloud.

## Versie Scene7 herfst 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

De meest recente release bevat informatie over de [!DNL Adobe Scene7] release van de [!DNL Adobe Experience Manager] oplossing in de [!DNL Adobe Marketing Cloud]herfst van 2016.

* [Algemeen](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 het Publiceren Systeem](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Viewers (afbeeldingen met 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Viewers (afbeelding met 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Viewers (afbeelding met 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Beeld Serend 6.3.2 en het Teruggeven van het Beeld 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Algemeen {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe maakt het spannend om de beschikbaarheid van HTTP/2-levering van inhoud bekend te maken, wat de verbeterde prestaties ten goede komt.

Zie [HTTP2 Veelgestelde vragen](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html)over het leveren van inhoud.

## Scene7 het Publiceren Systeem {#section-24487cb493444d808fb7193f0a00cdd4}

Zie [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html voor volledige documentatie](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Nieuwe functies, verbeteringen en foutoplossingen**

* Functie voor videorecut is verwijderd uit [!DNL Adobe Scene7 Publishing System] gebruikersinterface.
* Toegevoegde authentificatie aan alle servers Scene7 waar nodig en mogelijk.
* Opgeloste problemen in verband met de lijstweergave in de prullenbak.
* Verwijderd **Create SPSAdmin** gebruikerseigenschap van het Beheer van de Gebruiker wegens veiligheidsoverwegingen.
* FTP WebAdmin ondersteunt nu OKTA-verificatie.
* Verwijderd de eigenschap van het standaardwachtwoord dat voor nieuwe gebruikers van het Portaal van Media werd gecreeerd.
* Bugfixatie die het tijdelijke wachtwoord impliceert dat werd geproduceerd toen een nieuwe gebruiker werd toegevoegd. Het wachtwoord voldoet niet aan de vereiste wachtwoordvereisten.
* Opgeloste problemen met WebAdmin-hoofdschijf vol.
* Bugfixatie waarbij een gebruiker wordt uitgeschakeld die niet onmiddellijk in de gebruikersinterface wordt weergegeven.
* Opgeloste problemen waarbij een gebruiker is verwijderd en die u later niet opnieuw hebt gemaakt.
* De moeilijke situatie die met het Welkome die e-mail impliceert naar nieuwe gebruikers wordt verzonden Scene7 die geen authentificatie om bepaalde montages omvatte te controleren.
* Opgeloste problemen waarbij een FTP-mappenlijst niet kan worden opgehaald als een map speciale tekens in de naam bevat.
* Vorm OKTA dienstverleners voor milieu Scene7.
* Toegevoegde ondersteuning voor Organizer-id voor Marketing Cloud voor Viewer Analytics.
* Geïmplementeerde consument Scene7 SAML.

## Viewers (afbeeldingen met 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Zie [Referentiehandleiding](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)voor viewers voor volledige documentatie.

**Bugfixes voor afbeeldingen met 5.5.3**

* Compatibiliteit met RequireJS- en DOJO-bibliotheken.

   Geconsolideerde SDK JS-caching tijdens viewerimplementatie.

## Viewers (afbeelding met 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Zie [Referentiehandleiding](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)voor viewers voor volledige documentatie.

**Bugfixes voor afbeeldingen in 5.5.2**

* Video kan niet worden afgespeeld in Internet Explorer 11 in Windows 7.
* `initialframe` had geen invloed op de staande modus op mobiele apparaten voor HTML5 eCatalog.

## Viewers (afbeelding met 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Zie [Referentiehandleiding](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)voor viewers voor volledige documentatie.

**Nieuwe functies, verbeteringen en foutoplossingen voor Image Serving 5.5.1**

* HTML5 eCatalog-viewer met zoekfunctie.
* Toegevoegde HLS-streaming video playback als standaardmethode voor het afspelen van video voor de meeste desktopsystemen. HDS-videostreaming op basis van Flash is nog steeds beschikbaar als alternatieve afspeeloptie.
* Toegevoegde ondersteuning voor apparaten met zowel muis- als aanraakinvoer via Chrome-browser.
* Ondersteuning voor Organizer-id voor Marketing Cloud toegevoegd aan de Analytics-integratie.
* Werk de JavaScript-bibliotheek AppMeasurement bij naar versie 1.6.1.
* Extra ondersteuning voor oriëntatie van rechts naar links in de eCatalog-viewer.
* Probleem opgelost waarbij een fout buiten het bereik werd `tip=0,-1,0` veroorzaakt.

**Compatibiliteitsnotities**

* Blackberry

   * Incompatibiliteit met oudere AVS-sets. Clients moeten mogelijk AVS-sets opnieuw uploaden om het afspelen mogelijk te maken.

* Algemeen

   * Schalen aan de browserzijde kan de interface en afbeeldingen vervagen als de gebruiker inzoomt op de pagina. UI-opmaak wordt mogelijk ook onjuist weergegeven, afhankelijk van zoomen. Dit gaat over op het volledige scherm.
   * Vanwege groottebeperkingen op mobiele apparaten gebruikt de gemengde Media Viewer een diabeweging om frames in ingesloten afbeeldingssets te wisselen in plaats van op de ingesloten stalenscomponent te tikken. De component is er als visuele indicator.
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

   * De mobiele apparaten van HTC onze bevindingen tonen aan dat het onvermogen om inheems knijpbeweging onbruikbaar te maken een &quot;eigenschap&quot;van de omslag van HTML UI (van HTC Sense) is. Hierdoor kan de hele pagina worden ingezoomd wanneer een zoombeweging met knijpbeweging in de viewer wordt gebruikt. Stel voor dat u dubbeltikt.
   * Pictogrammen met afbeeldingen met hyperlinks kunnen elkaar overlappen als de afbeeldingen met hyperlinks klein zijn en dicht bij elkaar liggen.

* HTML5-video

   * Internet Explorer 9: aangepaste posterafbeeldingen worden niet weergegeven.
   * `IntialBitRate` modifier wordt alleen ondersteund bij het afspelen van software-HLS en Flash HDS. Dit werkt niet wanneer het afspelen de native speler gebruikt.
   * Op dit moment wordt het progressieve afspelen van OGG en WebM niet ondersteund.
   * Browserschaling kan ertoe leiden dat de videospeler op een onjuiste grootte wordt weergegeven (inclusief de weergave-instellingen van het besturingsvenster van Windows OS)
   * Videozoekopdrachten waarbij gebruik wordt gemaakt van HLS-streaming op Safari kunnen inconsistent zijn.

* Internet Explorer

   * De modus Kwarten wordt momenteel niet ondersteund.
   * De compatibiliteitsmodus wordt momenteel niet ondersteund.
   * Internet Explorer op mobiel wordt momenteel niet ondersteund.

* iOS

   * Grote eCatalogs kunnen ertoe leiden dat de browser vastloopt op iPad 2.
   * iPhone 6+-telefoons worden door de viewers als tablets gedetecteerd.

* Safari

   * Safari 6.1 of hoger: Instellingen voor Internet-plug-ins kunnen het afspelen van Flash-video voorkomen.
   * Video &#39;seek&#39; met gebruik van HLS-streaming op Safari kan inconsistent zijn.
   * Kan niet zoeken tot einde van video in Safari 6 met gebruik van HLS-streaming.

**Bekende problemen en beperkingen**

* De modifiers van de Beelddienst van `iscommands` worden niet toegevoegd aan het `req=set` verzoek door ontwerp. Modifiers die alleen van invloed zijn op de beeldweergave, werken prima. Modifiers die van invloed zijn op de grootte, moeten in een complex element worden gebruikt. Bijvoorbeeld:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flyout] IE9 blijft soms op het scherm nadat u de muis hebt uitgeschakeld.
* Schalen in de browser leidt tot een onjuiste formaatwijziging.
* iPad 2: Big eCatalog asset crasht Safari op iOS.
* Alle viewers

   * Watermerken, verduistering en vergrendeling worden niet ondersteund.
   * Voorinstellingen voor afbeeldingen worden niet ondersteund.
   * Het toevoegen of verwijderen van viewer uit het DOM met behulp van `display:none` CSS of door het dynamisch los te koppelen van het bovenliggende knooppunt wordt op dit moment niet ondersteund.

* HTML5 All Viewers

   * Het insluiten van een viewer in een tabel kan resulteren in een onjuiste grootte of plaatsing van de viewer in een andere modus dan de modus Volledig scherm. U kunt beter DIV&#39;s gebruiken.
   * Parameters met expliciete instantienamen in de code schrijven voor dat instantienamen in de URL ook moeten worden overschreven (bijvoorbeeld `zoomView.iconfeffect=0`).
   * Uitsnijden van de opdracht Afbeeldingsserver wordt momenteel niet ondersteund.
   * De knop Sluiten werkt alleen als de viewer is geopend in het onderliggende venster.
   * De `iscommands` optie biedt geen ondersteuning voor wijzigingstoetsen voor afbeeldingsservers die de afbeeldingsgrootte beïnvloeden.

* HTML5 eCatalog

   * Als u naar andere HTML-pagina navigeert en soms terugkeert, wordt de eerste pagina hersteld.
   * Paginalay-out wordt soms onjuist weergegeven na het roteren van het iOS-apparaat. Als u naar de pagina zoomt, wordt de indeling gecorrigeerd.
   * Interne koppelingen verwijzen alleen naar de meest linkse pagina in spreads met meerdere pagina&#39;s. Heeft invloed op mobiele apparaten in de staande modus.
   * InitalFrame koppelt alleen aan de meest linkse pagina in spreads met meerdere pagina&#39;s. Heeft invloed op mobiele apparaten in de staande modus.
   * Vanwege beperkingen van de browser is de afdrukfunctie niet beschikbaar in IE9.

* HTML5 MixedMedia

   * Soundtrack-afspelen wordt momenteel niet ondersteund.

* HTML5 Social

   * Als u de miniaturen correct wilt weergeven in een uitgaande e-mail, moet de `serverurl` optie een absolute URL hebben.

* HTML5-video

   * Er kan een fout met betrekking tot de maximale grootte optreden voor de posterafbeelding. Bedrijf moet mogelijk de limietinstelling voor het publiceren van Image Serving verhogen.
   * De video titels vereisen een bedrijfregels als het ontvangen van de HTML- pagina van een externe server (niet een server Scene7) wordt gediend. Neem contact op met de Technische Ondersteuning van Adobe voor hulp.
   * Bij bijhouden van Analytics wordt mogelijk een onjuist afspeelpercentage gerapporteerd vanwege buffering
   * Zwart frame in plaats van posterafbeelding wordt mogelijk weergegeven op iPad- of Android-apparaten.
   * Het zwarte frame kan op het scherm opvlammen tijdens het laden van de viewer op iPad- of Android-apparaten.
   * Zwarte randen worden weergegeven aan de zijde van de component VideoPlayer wanneer de achtergrond op iPad-apparaten is ingesteld op wit/transparant.
   * Het laatste videoframe kan op iPad worden vervormd met iOS 7.
   * Soms treedt macroblokkering op tijdens het zoeken naar video&#39;s in de streamingmodus HLS in Chrome-, Firefox- en Internet Explorer-browsers.
   * Posterafbeelding wordt mogelijk niet voor de eerste keer weergegeven in een Microsoft Edge-browser.
   * Posterafbeelding kan na het laden van de video in Internet Explorer 9 worden verborgen wanneer progressief afspelen wordt gebruikt.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

De gebruikershandleiding bevindt zich in de map Adobe HTML5 Viewer SDK van de clientinstallatie. Component API-documentatie vindt u in de submap docs van de clientinstallatie.

**Bugfixes voor 3.0.2**

* VideoPlayer - Video kan niet worden afgespeeld in Internet Explorer 11 in Windows 7
* Inhoudsopgave - heeft geen invloed op de staande modus op mobiele apparaten voor de HTML5 eCatalog-viewer. `initialframe`

**Nieuwe functies, verbeteringen en foutoplossingen voor 3.0.1**

* Algemeen

   * Toegevoegde HLS-streaming video playback als standaardmethode voor het afspelen van video voor de meeste desktopsystemen. HDS-videostreaming op basis van Flash is nog steeds beschikbaar als alternatieve afspeeloptie.
   * Toegevoegde componenten SearchManager, SearchPanel, SearchEffect, en SearchButton om nieuwe eigenschap van het Onderzoek in eCatalog kijkers te steunen.
   * Toegevoegde ondersteuning voor apparaten met zowel muis- als aanraakinvoer via de Chrome-browser.
   * De vernieuwde Android-versiedetectie ter ondersteuning van toekomstige versies van het besturingssysteem
   * Voeg steun voor recht-aan-linkerrichtlijn in eCatalog-specifieke componenten van SDK toe.

* ControlBar

   * Optioneel schuiven toegevoegd voor inhoud ControlBar voor het geval deze niet in de beschikbare breedte past.

* FlyoutzoomView

   * Probleem verholpen waarbij een fout buiten bereik werd `tip=0,-1,0` veroorzaakt.

**Compatibiliteitsnotities**

* Android 4.x

   * Als u de standaardinstelling wilt uitschakelen, moet blauw de volgende CSS-regel voor component worden toegevoegd:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

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

   * De iPad 3 heeft een native resolutie van 2048 x 1536. Dit kan weergaveproblemen veroorzaken als de publicatie van het bedrijf IS, waarbij de afbeeldingsgroottebeperking lager is ingesteld.

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
   * Paginaschaling op aanraakapparaten wordt momenteel niet ondersteund. Voor het insluiten van HTML5-viewers is de metatag viewport met de juiste instellingen vereist.

* Xoom

   * Dubbeltikken op een beweging zoomt de viewer en de pagina in wanneer schaling aan de browserzijde actief is.

**Bekende problemen en beperkingen**

* Alle componenten

   * In versies 2.7.2 en eerdere versies zijn sommige componenten met behulp van `insertBefore()` API aan de DOM toegevoegd. Als gevolg hiervan worden deze componenten onder aan de stapelvolgorde geplaatst, ongeacht wanneer de componentinstantie wordt gemaakt ten opzichte van andere componenten. Met versie 2.8.1 gebruiken alle componenten nu `appendChild()` API, wat betekent dat de component stapelvolgorde zou overeenkomen met de volgorde waarin de instantie wordt gemaakt.

   * Het gebruik van `iscommand` modifier voor het instellen van de indeling voor alfakanalen van de afbeelding wordt niet ondersteund. Gebruik in plaats `FMT` hiervan componentparameter.
   * Eigenschap voor CSS-transformatie wordt momenteel niet ondersteund.

* Aanraakapparaten

   * Met een knijpbeweging op aanraakapparaten wordt geen zoomgebeurtenis gegenereerd

* Container

   * Rand, opvulling en marges op de container worden niet ondersteund. Adobe raadt u aan stijlelementen toe te voegen aan het bovenliggende DIV-bestand.
   * De behoefte om de containergrootte uitdrukkelijk te plaatsen of de componenten kunnen correct worden gerangschikt.

* Afdrukcomponent

   * Vanwege beperkingen van de browser kan de afdrukcomponent in Internet Explorer 9 de inhoud op het papier mogelijk niet correct schalen.

* component IconEffect

   * IconEffect genereert een scriptfout in Internet Explorer als deze `autohide` is uitgeschakeld (ingesteld op `0`).

* Component ImageMapEffect

   * Vertraging met pictogram voor verplaatsen bij het pannen van een afbeelding in een weergavecomponent.

* De component MediaSet

   * Voor inline-elementen wordt dezelfde codering aangevraagd als voor de URL.

* component NavigationView

   * De component ondersteunt momenteel geen formaatwijziging.

* PageScrubber-component

   * Op iPhone 5 wordt, wanneer de PageScrubber-ballon op tekst is ingesteld, artefacten weergegeven wanneer de knop langs de track wordt verplaatst. Het gebruik `-webkit-background-clip: content;` in de stijl werkt rond de uitgave.

* Component SpinView

   * SpinView lijkt soms te bevriezen na een veegbeweging en het apparaat te roteren terwijl de afbeelding draait.

* De component Stalen

   * Wanneer u een buiten-de-grenzenstaal selecteert, worden 2 markeringen weergegeven.
   * Automatisch schuiven terwijl de `selectSwatch()` methode onjuist werkt.

* VideoPlayer

   * Videoframe wordt niet bijgewerkt als de zoekopdracht is ingesteld op 100 procent en de fallback is ingesteld op auto.
   * Het af en toe blokkeren van macro&#39;s kan voorkomen tijdens videozoekacties in de streamingmodus HLS in de browsers Chrome, Firefox en Internet Explorer.
   * Posterafbeelding wordt mogelijk niet voor de eerste keer weergegeven in een Microsoft Edge-browser.
   * Posterafbeelding kan na het laden van de video in Internet Explorer 9 worden verborgen wanneer progressief afspelen wordt gebruikt.

## Scene7 Beeld Serend 6.3.2 en het Teruggeven van het Beeld 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC-hulpprogramma - markering wordt niet meer ondersteund. `downsample2x2` Deze vlag was een slechte kwaliteit 2x2 downsampler die niet meer door IPS wordt gebruikt.
* CORS-header - Momenteel is de CORS-header geconfigureerd voor `/is/content/` aanvragen.

