---
description: Er zijn enkele beperkingen en bekende problemen die in overweging moeten worden genomen bij het gebruik van Scene7 Image Serving.
seo-description: Er zijn enkele beperkingen en bekende problemen die in overweging moeten worden genomen bij het gebruik van Scene7 Image Serving.
seo-title: Beperkingen en bekende problemen
solution: Experience Manager
title: Beperkingen en bekende problemen
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 0e9d6a0ccbb040b27cc89b933442d8530c60d5c8
workflow-type: tm+mt
source-wordcount: '1248'
ht-degree: 0%

---


# Beperkingen en bekende problemen{#restrictions-and-known-issues}

Er zijn enkele beperkingen en bekende problemen die in overweging moeten worden genomen bij het gebruik van Scene7 Image Serving.

## Documentatieferrata {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Het aantal regels zal niet het maximum van `\copyfitmaxlines` het plaatsen en het aantal expliciete lijnen in de tekstinput overschrijden.
* In afbeeldingssets zijn gelijke accolades en haakjes vereist. Als accolades en haakjes niet overeenkomen, moeten deze URL-gecodeerd zijn.
* De globale waarschuwing voor de responstijd aan de serverzijde bevat reacties op fouten.
* De opdracht `id=` is momenteel vereist wanneer u de opdracht `rect=` gebruikt met een afbeelding- of maskerverzoek.

## Bekende verschillen textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetische cursief wordt minder schuin gerenderd dan bij gebruik van `text=`.
* Onderstrepen is iets lager en smaller dan wanneer u `text=` gebruikt.
* `\expnd` en worden  `\expndtw` gebruikt met hoge negatieve waarden, waardoor tekens voor elkaar worden geplaatst wanneer ze worden gebruikt  `text=`.

* `\charscaley` wordt anders geschaald dan bij gebruik,  `text=` maar heeft geen invloed op de regelhoogte.

* Als de laatste tekstregel niet past, wordt de hele regel neergezet in plaats van als afboeking te worden weergegeven.
* `\slmult` en  `\sl` gedraagt zich anders dan MS Word en  `text=`gelden ze alleen voor de huidige en volgende alinea&#39;s.

* `\sb` is van toepassing op de eerste alinea voor zowel MS Word als  `text=`, Adobe InDesign en Photoshop doen dit niet.

* `\sa` is van toepassing op de laatste alinea voor zowel MS Word als  `text=`, Adobe InDesign en Photoshop doen dit niet.

## Achterwaartse compatibiliteit {#section-a76842f751944f4fb664af296d064122}

* Het onderstrepingsteken ( `\_`) in een RTF-tekenreeks segmenteren werkt niet met alle lettertypen die `textPs=` gebruiken

* Ondersteuning voor niet-hoofdlettergevoelige macroverwerking.
* De cataloguscache is teruggebracht van 60 seconden naar 10 seconden.
* Met de functie voor omleiding van fouten worden nu alleen aanvragen omgeleid die verwijzen naar beschadigde afbeeldingen, lettertypen, kleurprofielen en afbeeldingen die in een catalogus zijn gepubliceerd, maar niet op schijf zijn gevonden.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=`en retourneert  `originN=` nu een parseringsfout als een van de wijzigingwaarden groter is dan 2147483648.

* Codering van geneste aanvragen wordt niet ondersteund. De overgang aan het nieuwe gedrag en uncodeert om het even welke genestelde verzoekwaarden die in URL- verzoeken op uw plaats en in uw bedrijfcatalogi worden gevonden.
* DefaultImage past nu duimnagelattributen toe wanneer het gebruiken `req=tmb`.
* In eerdere versies met `flip=` is de positie van de afbeelding nooit gewijzigd, ongeacht het ankerpunt.

## Beperkingen die van toepassing zijn op bibliotheken van derden {#section-79768b96bf634e44ab672c5b893f343d}

De Digimarc-bibliotheek weigert een Digimarc-watermerk toe te passen op een afbeelding als deze al is gedetecteerd. Als een primaire afbeelding voldoende wordt bewerkt, is het mogelijk dat de Digimarc-bibliotheek nog steeds kan herkennen dat het watermerk is toegepast. Het kan echter zijn dat de informatie niet kan worden gelezen. Dit resulteert in een nieuwe afbeelding waarin de oorspronkelijke Digimarc-informatie die op de oorspronkelijke afbeelding is toegepast, niet kan worden verkregen. Met Beeldserver kunt u nu het Digimarc-watermerk toepassen dat is gedefinieerd in de catalogus van het bedrijf.

## Beperkingen die van toepassing zijn op zowel het renderen van afbeeldingen als het renderen van afbeeldingen {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Het is mogelijk dat imageservers en het renderen van afbeeldingen niet alle CPU&#39;s ten volle benutten wanneer er meer dan vier CPU&#39;s beschikbaar zijn. Simuleer uw verkeer op deze machines om te zien hoe voordelig het met meer dan 4 cpu&#39;s is.
* Externe URL&#39;s die een omleiding retourneren (HTTP-status 301, 302 of 303) worden afgewezen.
* Bij het configureren van `errorRedirect.rootUrl` moet het IP-adres dat in deze eigenschap is gedefinieerd, worden opgenomen in de `<addressfilter>`-tagwaarde op die server.

   *Voorbeeld*:

   Server A heeft `errorRedirect.rootUrl=10.10.10.10` gedefinieerd.

   Server B, die het IP adres van 10.10.10.10 heeft, plaatst de `<addressfilter>` markeringswaarde in het heersersdossier om zijn IP adres (10.10.10.10) te omvatten.

* Punttekst en tekstpad met positionering kunnen uitknippen bevatten.
* `text=` wordt alleen toegepast  `\sa` en niet per alinea  `\sb` op het gehele tekstblok.

* Wanneer u een bedrijf gebruikt dat is gedefinieerd in de URL en een ander bedrijf dat is gedefinieerd voor de optie `src=` of `mask=`, moet u een slash voorvoegsel toevoegen aan het bedrijf dat is gedefinieerd voor `src=` of `mask=`, anders werkt deze aanvraag niet.

   *Voorbeeld*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   In plaats van: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Niet-piramided TIFF- of vignetverzoeken geven een vergelijkbaar foutbericht aan

   *&quot;De afbeelding  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` heeft geen geldige DSF en het gebied van 2,25 MPixel overschrijdt de max. van 2 MPixel&quot;* .

   De beste manier is om gepiramideerde TIFF en vignetten te gebruiken. Als u niet-gepiramideerde golven of vignetten moet gebruiken, volg de onderstaande instructies om de formaatlimiet te verhogen.

   *Omgaan*:

   Voor het teruggeven van Beeld niet-piramided vignettes, verhoog de bezitswaarde voor IrMaxNonPyrVignetteSize in het [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuratiedossier.

   Verhoog de eigenschapswaarde voor `MaxNonDsfSize` in het [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuratiebestand voor afbeeldingen die niet-gepiramideerde TIFF&#39;s leveren.

* Adobe Photoshop CS3 slaat gelaagde PSD-bestanden standaard niet op als een samengestelde afbeelding.

   *Symptomen*:

   Het gelaagde PSD-bestand van Adobe Photoshop CS3 wordt weergegeven als zwart met de tekst &quot;Dit gelaagde Photoshop-bestand is niet opgeslagen met een samengestelde afbeelding.&quot; voor het Beeld dat antwoordbeeld serveert of in IPS.

   *Oplossing*:

   Sla het Adobe Photoshop CS3-bestand op met maximale compatibiliteit ingeschakeld.

* Wanneer u een ICC-profiel toewijst aan een antwoordafbeelding in CMYK/JPEG, worden kleuren in sommige browsers omgekeerd.*Omgaan*:

   De indeling van de reactieafbeelding wijzigen met `fmt=`

* De grootte van de HTTP-reactie op afbeelding data-after compressie, inclusief bestandsheader-is beperkt tot 16 MB.
* &quot;..&quot; is niet toegestaan in een padelement in HTTP-aanvragen.
* Als u de installatie ongedaan maakt, wordt mogelijk door de gebruiker gemaakt of gewijzigd bestand verwijderd uit *[!DNL install_root]* of een submap. Kopieer deze bestanden naar een andere locatie voordat u de installatie ongedaan maakt.

## Beperkingen die alleen van toepassing zijn op beeldservers {#section-b08ad535e4454265b8157dec244c4faf}

* Voorgrondkleuren in de RTF-opdracht ( `\cf`) worden niet ondersteund voor PhotoFont-tekst.
* Het synchroniseren van vet, cursief en vet/cursief wordt geweigerd als een fout voor PhotoFont-tekst.
* Verticale tekststroom wordt niet ondersteund voor PhotoFont-tekst.
* PNG-afbeeldingen met 16 bits per kanaal worden niet ondersteund voor PhotoFont-tekst.
* Voor kleurcorrecties voor PNG-afbeeldingen met ingesloten kleurprofielen worden opties met harde codes gebruikt. Render-intentie is relatief colorimetrisch en Blackpoint-compensatie is ingeschakeld voor PhotoFont-tekst.
* Opzoeken op basis van bestanden wordt niet ondersteund wanneer vertaling van landinstellingen is ingeschakeld in het [!DNL ini]-bestand van het bedrijf.
* Met Beeldserver worden niet-gesloten Photoshop-paden niet correct geschreven.
* De afbeeldingsserver ondersteunt momenteel niet de verwerking van TIFF-bestanden die zijn geëxporteerd met Adobe Media Encoder 4.0.1 of eerder. Adobe Media Encoder is inbegrepen bij Premiere Pro CS4, After Effects CS4 en Creative Suite 4 Production Premium.
* Het gebruik van `text=` met lagen die zichzelf vergroten/verkleinen ondersteunt geen RTF-tekenreeksen die meer dan één instelling gebruiken voor regeluitvulling.

   *Voorbeeld*

   RTF-tekenreeks kan niet zowel de uitvulling van de linker- als rechterregel gebruiken voor een tekstlaag waarvan het formaat automatisch wordt aangepast.

* SVG heeft een eigen eigenschap voor het opzoekpad van lettertypen waarnaar wordt verwezen en die niet zijn ingesloten in het SVG-bestand.

   *Symptomen*

   Gerenderde SVG-afbeeldingen met lettertypedefinities gebruiken een onjuist lettertype.

   *Workaround*

   Stel de eigenschap `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] in.

* Uitsnijden gebruikt momenteel `bgColor=` in plaats van `color=` om een nieuw uitgebreid gebied te vullen.

* Kleuromzetting is mogelijk niet correct wanneer `bgColor=` niet overeenkomt met de basiskleurruimte met kleurprofielen.
* De effecten van de buitenste laag worden niet gerenderd als de laag geen masker of alpha-gegevens heeft.

## Beperkingen die alleen van toepassing zijn op het renderen van afbeeldingen {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decalen en wandmaterialen kunnen niet worden verwijderd.
* De grootte van structuren is beperkt ten opzichte van de grootte van de vignetweergave. In zeldzame gevallen kan de standaardlimiet van 425% van de weergavegrootte problemen opleveren met een toepassing die zeer grote niet-herhaalbare structuren gebruikt. Als het niet mogelijk is de toepassing of inhoud te wijzigen om binnen de vooraf gedefinieerde beperkingen te werken, kan het percentage als volgt worden verhoogd. Open [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml] in een teksteditor, zoek `IrMaxTextureSizeFactor` en voer een nieuw percentage in. De verandering treedt onmiddellijk in werking zonder de Server van het Beeld opnieuw te beginnen.

* De JavaScript-engines in Netscape en Opera cache-responsgegevens, zelfs als de nocache-header is ingesteld. Dit interfereert met het correct functioneren van stateful verzoeken.

   *Workaround*

   Voeg een tijdstempel of andere unieke id toe aan de aanvraagtekenreeks, zoals `"&.ts=currentTime`.

## Beperkingen die alleen van toepassing zijn op nutsbedrijven {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`soms crasht met een segmentatiefout wanneer gestopt met een  `control-c`.
