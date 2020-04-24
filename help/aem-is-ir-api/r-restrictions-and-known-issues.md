---
description: Er zijn sommige beperkingen en bekende kwesties die zouden moeten worden overwogen wanneer het gebruiken van het Serven van het Beeld Scene7.
seo-description: Er zijn sommige beperkingen en bekende kwesties die zouden moeten worden overwogen wanneer het gebruiken van het Serven van het Beeld Scene7.
seo-title: Beperkingen en bekende problemen
solution: Experience Manager
title: Beperkingen en bekende problemen
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Beperkingen en bekende problemen{#restrictions-and-known-issues}

Er zijn sommige beperkingen en bekende kwesties die zouden moeten worden overwogen wanneer het gebruiken van het Serven van het Beeld Scene7.

## Documentatierrata {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Het aantal regels overschrijdt niet het maximum van de `\copyfitmaxlines` instelling en het aantal expliciete regels in de tekstinvoer.
* In afbeeldingssets zijn gelijke accolades en haakjes vereist. Als accolades en haakjes niet overeenkomen, moeten deze URL-gecodeerd zijn.
* De globale waarschuwing voor de responstijd aan de serverzijde bevat reacties op fouten.
* De `id=` opdracht is momenteel vereist wanneer u de `rect=` opdracht gebruikt met een aanvraag voor een afbeelding of masker.

## Bekende verschillen textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetische cursief wordt minder schuin gerenderd dan bij gebruik `text=`.
* Onderstrepen is iets lager en dunner dan bij gebruik `text=`.
* `\expnd` en worden gebruikt met hoge negatieve waarden, waardoor tekens voor elkaar worden geplaatst wanneer ze worden gebruikt `\expndtw` `text=`.

* `\charscaley` de schaal wordt anders geschaald dan bij gebruik, `text=` maar heeft geen invloed op de regelhoogte.

* Als de laatste tekstregel niet past, wordt de hele regel neergezet in plaats van als afboeking te worden weergegeven.
* `\slmult` en `\sl` gedraagt zich anders dan MS Word en `text=`gelden ze alleen voor de huidige en volgende alinea&#39;s.

* `\sb` is van toepassing op de eerste alinea voor zowel MS Word als `text=`Adobe InDesign en Photoshop doen dit niet.

* `\sa` is van toepassing op de laatste alinea voor zowel MS Word als `text=`Adobe InDesign en Photoshop doen dit niet.

## Achterwaartse compatibiliteit {#section-a76842f751944f4fb664af296d064122}

* Het afbreken van het onderstrepingsteken ( `\_`) in een RTF-tekenreeks werkt niet met alle lettertypen die `textPs=`

* Ondersteuning voor niet-hoofdlettergevoelige macroverwerking.
* De cataloguscache is teruggebracht van 60 seconden naar 10 seconden.
* Met de functie voor omleiding van fouten worden nu alleen aanvragen omgeleid die verwijzen naar beschadigde afbeeldingen, lettertypen, kleurprofielen en afbeeldingen die in een catalogus zijn gepubliceerd, maar niet op schijf zijn gevonden.
* `posN=`, `anchor=`, `anchorN=`, `origin=`en retourneert `originN=` nu een parseringsfout als een van de wijzigingwaarden groter is dan 2147483648.

* Codering van geneste aanvragen wordt niet ondersteund. De overgang aan het nieuwe gedrag en uncodeert om het even welke genestelde verzoekwaarden die in URL- verzoeken op uw plaats en in uw bedrijfcatalogi worden gevonden.
* DefaultImage past nu duimnagelattributen toe wanneer het gebruiken `req=tmb`.
* In eerdere versies `flip=`werd de positie van de afbeelding nooit gewijzigd, ongeacht het ankerpunt.

## Beperkingen die van toepassing zijn op bibliotheken van derden {#section-79768b96bf634e44ab672c5b893f343d}

De Digimarc-bibliotheek weigert een Digimarc-watermerk toe te passen op een afbeelding als deze al is gedetecteerd. Als een hoofdafbeelding voldoende wordt bewerkt, is het mogelijk dat de Digimarc-bibliotheek nog steeds kan herkennen dat het watermerk is toegepast. Het kan echter zijn dat de informatie niet kan worden gelezen. Dit resulteert in een nieuwe afbeelding waarin de oorspronkelijke Digimarc-informatie die op de oorspronkelijke afbeelding is toegepast, niet kan worden verkregen. Met Beeldserver kunt u nu het Digimarc-watermerk toepassen dat is gedefinieerd in de catalogus van het bedrijf.

## Beperkingen die van toepassing zijn op zowel Beeldbewerking als Afbeeldingsweergave {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Het is mogelijk dat imageservers en het renderen van afbeeldingen niet alle CPU&#39;s ten volle benutten wanneer er meer dan vier CPU&#39;s beschikbaar zijn. Simuleer uw verkeer op deze machines om te zien hoe voordelig het met meer dan 4 cpu&#39;s is.
* Externe URL&#39;s die een omleiding retourneren (HTTP-status 301, 302 of 303) worden afgewezen.
* Wanneer het vormen `errorRedirect.rootUrl` van het IP adres in dit bezit wordt bepaald moet in de waarde van de liniaalmarkering op die server worden omvat `<addressfilter>` .

   *Voorbeeld*:

   Server A heeft gedefinieerd `errorRedirect.rootUrl=10.10.10.10` .

   Server B, die het IP-adres van 10.10.10.10 heeft, stelt de `<addressfilter>` tagwaarde in het liniaalbestand in om het IP-adres (10.10.10.10) op te nemen.

* Punttekst en tekstpad met positionering kunnen uitknippen bevatten.
* `text=` wordt alleen toegepast `\sa` `\sb` en niet op het gehele tekstblok en niet op de alinea.

* Wanneer u een bedrijf gebruikt dat is gedefinieerd in de URL en een ander bedrijf dat is gedefinieerd voor de `src=` optie of `mask=` modifier, moet u een forward slash voorvoegsel toevoegen aan het bedrijf dat is gedefinieerd voor `src=` of `mask=` voor deze vorm van aanvraag.

   *Voorbeeld*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   In plaats van: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Niet-piramided TIFF- of vignetverzoeken geven een vergelijkbaar foutbericht aan

   *&quot;De afbeelding`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`heeft geen geldige DSF en het gebied van 2,25 MPixel overschrijdt de maximale waarde van 2 MPixel&quot;* .

   De beste manier is om gepiramideerde TIFF en vignetten te gebruiken. Als u niet-gepiramideerde golven of vignetten moet gebruiken, volg de onderstaande instructies om de formaatlimiet te verhogen.

   *Omgaan*:

   Voor afbeeldingen die niet-gepiramideerde vignetten renderen, verhoogt u de eigenschapswaarde voor IrMaxNonPyrVignetteSize in het configuratiebestand [!DNL *[!DNL install_root]*/ImageServing/bin/ImageServerRegistry.xml].

   Voor Beeld dat niet-piramided TIFFs dient, verhoog de bezitswaarde voor `MaxNonDsfSize` in het [!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml] configuratiedossier.

* In Adobe Photoshop CS3 worden PSD-bestanden met lagen standaard niet opgeslagen als een samengestelde afbeelding.

   *Symptomen*:

   Het gelaagde PSD-bestand van Adobe Photoshop CS3 wordt weergegeven als zwart met de tekst &quot;Dit gelaagde Photoshop-bestand is niet opgeslagen met een samengestelde afbeelding.&quot; voor het Beeld dat antwoordbeeld serveert of in IPS.

   *Oplossing*:

   Sla het Adobe Photoshop CS3-bestand op met maximale compatibiliteit ingeschakeld.

* Wanneer u een ICC-profiel toewijst aan een antwoordafbeelding in CMYK/JPEG, worden kleuren in sommige browsers omgekeerd.*Omgaan*:

   De indeling van de reactieafbeelding wijzigen met `fmt=`

* De grootte van de HTTP-reactie op afbeelding data-after compressie, inclusief bestandsheader-is beperkt tot 16 MB.
* &quot; ..&quot; is niet toegestaan in een padelement in HTTP-aanvragen.
* Als u de installatie ongedaan maakt, verwijdert u mogelijk het door de gebruiker gemaakte of gewijzigde bestand uit *[!DNL install_root]* een submap. Kopieer deze bestanden naar een andere locatie voordat u de installatie ongedaan maakt.

## Beperkingen die alleen van toepassing zijn op beeldservers {#section-b08ad535e4454265b8157dec244c4faf}

* Voorgrondkleuren in de RTF-opdracht ( `\cf`) worden niet ondersteund voor PhotoFont-tekst.
* Het synchroniseren van vet, cursief en vet/cursief wordt geweigerd als een fout voor PhotoFont-tekst.
* Verticale tekststroom wordt niet ondersteund voor PhotoFont-tekst.
* PNG-afbeeldingen met 16 bits per kanaal worden niet ondersteund voor PhotoFont-tekst.
* Voor kleurcorrecties voor PNG-afbeeldingen met ingesloten kleurprofielen worden opties met harde codes gebruikt. Render-intentie is relatief colorimetrisch en Blackpoint-compensatie is ingeschakeld voor PhotoFont-tekst.
* Opzoeken op basis van bestanden wordt niet ondersteund wanneer vertaling van landinstellingen is ingeschakeld in [!DNL ini] het bedrijfsbestand.
* Met Beeldserver worden niet-gesloten Photoshop-paden niet correct geschreven.
* De afbeeldingsserver biedt momenteel geen ondersteuning voor het verwerken van TIFF-bestanden die zijn geëxporteerd met Adobe Media Encoder 4.0.1 of lager. Adobe Media Encoder wordt geleverd bij Premiere Pro CS4, After Effects CS4 en Creative Suite 4 Production Premium.
* Het gebruik `text=` met lagen die zichzelf aanpassen ondersteunt geen RTF-tekenreeksen die meer dan één instelling gebruiken voor regeluitvulling.

   *Voorbeeld*

   RTF-tekenreeks kan niet zowel de uitvulling van de linker- als rechterregel gebruiken voor een tekstlaag waarvan het formaat automatisch wordt aangepast.

* SVG heeft een eigen eigenschap voor het opzoekpad van lettertypen waarnaar wordt verwezen en die niet zijn ingesloten in het SVG-bestand.

   *Symptomen*

   Gerenderde SVG-afbeeldingen met lettertypedefinities gebruiken een onjuist lettertype.

   *Workaround*

   Stel de eigenschap in `svgProvider.fontRoot=` [!DNL *[!DNL install_root]* /ImageServing/conf/PlatformServer.conf].

* Uitsnijden wordt momenteel gebruikt `bgColor=` in plaats van nieuw uitgebreid gebied `color=` te vullen.

* Kleuromzetting is mogelijk niet correct als deze `bgColor=` niet overeenkomt met de basiskleurruimte met kleurprofielen.
* Buitenlaageffecten worden niet gerenderd als de laag geen masker- of alpha-gegevens heeft.

## Beperkingen die alleen van toepassing zijn op het renderen van afbeeldingen {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decalen en wandmaterialen kunnen niet worden verwijderd.
* De grootte van structuren is beperkt ten opzichte van de grootte van de vignetweergave. In zeldzame gevallen kan de standaardlimiet van 425% van de weergavegrootte problemen opleveren met een toepassing die zeer grote niet-herhaalbare structuren gebruikt. Als het niet mogelijk is de toepassing of inhoud te wijzigen om binnen de vooraf gedefinieerde beperkingen te werken, kan het percentage als volgt worden verhoogd. Open [!DNL *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml] met een teksteditor, zoek `IrMaxTextureSizeFactor` en voer een nieuw percentage in. De verandering treedt onmiddellijk in werking zonder de Server van het Beeld opnieuw te beginnen.

* De JavaScript-engines in Netscape en Opera cache-responsgegevens, zelfs als de nocache-header is ingesteld. Dit interfereert met het correct functioneren van stateful verzoeken.

   *Workaround*

   Voeg een tijdstempel of andere unieke id toe aan de tekenreeks request, zoals `"&.ts=currentTime`.

## Beperkingen die alleen van toepassing zijn op nutsbedrijven {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`soms crasht met een segmentatiefout wanneer gestopt met een `control-c`.
