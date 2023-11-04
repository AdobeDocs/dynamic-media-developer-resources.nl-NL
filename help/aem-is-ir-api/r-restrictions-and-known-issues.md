---
description: Er zijn enkele beperkingen en bekende problemen die in overweging moeten worden genomen bij het gebruik van Dynamic Media Image Serving.
solution: Experience Manager
title: Beperkingen en bekende problemen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Beperkingen en bekende problemen{#restrictions-and-known-issues}

Er zijn enkele beperkingen en bekende problemen die in overweging moeten worden genomen bij het gebruik van Dynamic Media Image Serving.

## Documentatierrata {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Het aantal lijnen is niet groter dan het maximum van `\copyfitmaxlines` en het aantal expliciete regels in de tekstinvoer.
* In afbeeldingssets zijn gelijke accolades en haakjes vereist. Als accolades en haakjes niet overeenkomen, moeten deze URL-gecodeerd zijn.
* De globale waarschuwing voor de responstijd aan de serverzijde bevat reacties op fouten.
* De `id=` is momenteel vereist wanneer u de opdracht `rect=` gebruiken met een afbeelding of maskerverzoek.

## Bekende verschillen textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetische cursief wordt minder schuin gerenderd dan bij gebruik `text=`.
* Onderstrepen is iets lager en dunner dan bij gebruik `text=`.
* `\expnd` en `\expndtw` gebruikt met hoge negatieve waarden, worden tekens vóór elkaar geplaatst wanneer `text=`.

* `\charscaley` schalen anders dan bij gebruik `text=` maar heeft geen invloed op de regelhoogte.

* Als de laatste tekstregel niet past, wordt de hele regel neergezet in plaats van als afboeking te worden weergegeven.
* `\slmult` en `\sl` gedraagt zich anders dan MS Word en `text=`, worden zij slechts van kracht voor de huidige en volgende alinea&#39;s.

* `\sb` is van toepassing op de eerste alinea voor zowel MS Word als `text=`, Adobe InDesign en [!DNL Photoshop] doe dit niet.

* `\sa` is van toepassing op de laatste alinea voor zowel MS Word als `text=`, Adobe InDesign en [!DNL Photoshop] doe dit niet.

## Achterwaartse compatibiliteit {#section-a76842f751944f4fb664af296d064122}

* Het onderstrepingsteken ( `\_`) in een RTF-tekenreeks werkt niet met alle lettertypen die `textPs=`

* Ondersteuning voor niet-hoofdlettergevoelige macroverwerking.
* De cataloguscache is teruggebracht van 60 seconden naar 10 seconden.
* Met de functie voor omleiding van fouten worden nu alleen aanvragen omgeleid die verwijzen naar beschadigde afbeeldingen, lettertypen, kleurprofielen en afbeeldingen die in een catalogus zijn gepubliceerd, maar niet op schijf zijn gevonden.
* `posN=`, `anchor=`, `anchorN=`, `origin=`, en `originN=` Retourneert nu een parseringsfout als een van de wijzigingwaarden groter is dan 2147483648.

* Codering van geneste aanvragen wordt niet ondersteund. De overgang aan het nieuwe gedrag en uncodeert om het even welke genestelde verzoekwaarden die in URL- verzoeken op uw plaats en in uw bedrijfcatalogi worden gevonden.
* DefaultImage past nu miniatuurkenmerken toe bij gebruik van `req=tmb`.
* In vorige versies met `flip=`, is de positie van de afbeelding nooit gewijzigd, ongeacht het ankerpunt.

## Beperkingen die van toepassing zijn op bibliotheken van derden {#section-79768b96bf634e44ab672c5b893f343d}

De Digimarc-bibliotheek weigert een Digimarc-watermerk toe te passen op een afbeelding als deze al is gedetecteerd. Als een primaire afbeelding voldoende wordt bewerkt, is het mogelijk dat de Digimarc-bibliotheek nog steeds kan herkennen dat het watermerk is toegepast. Het kan echter zijn dat de informatie niet kan worden gelezen. Dit resulteert in een nieuwe afbeelding waarin de oorspronkelijke Digimarc-informatie die op de oorspronkelijke afbeelding is toegepast, niet kan worden verkregen. Met Beeldserver kunt u nu het Digimarc-watermerk toepassen dat is gedefinieerd in de bedrijfscatalogus.

## Beperkingen die van toepassing zijn op zowel het uitvoeren van afbeeldingen als het renderen van afbeeldingen {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Het is mogelijk dat beeldservers en het renderen van afbeeldingen niet alle CPU&#39;s ten volle benutten wanneer er meer dan vier CPU&#39;s beschikbaar zijn. Simuleer uw verkeer op deze machines om te zien hoe voordelig het met meer dan 4 cpu&#39;s is.
* Externe URL&#39;s die een omleiding retourneren (HTTP-status 301, 302 of 303) worden afgewezen.
* Bij configureren `errorRedirect.rootUrl` het IP-adres dat in deze eigenschap is gedefinieerd, moet in de liniaal worden opgenomen `<addressfilter>` tagwaarde op die server.

  *Voorbeeld*:

  Server A is gedefinieerd `errorRedirect.rootUrl=10.10.10.10` .

  Server B die het IP adres van 10.10.10.10 heeft, plaatst `<addressfilter>` -tagwaarde in het liniaalbestand om het IP-adres (10.10.10.10) op te nemen.

* Punttekst en tekstpad met positionering kunnen uitknippen bevatten.
* `text=` alleen van toepassing `\sa` en `\sb` op het gehele tekstblok en niet op basis van alinea.

* Wanneer u een bedrijf gebruikt dat is gedefinieerd in de URL en een ander bedrijf dat is gedefinieerd voor de `src=` of `mask=` voorvoegsel, moet u een voorwaartse schuine streep aan het bedrijf voor bepalen `src=` of `mask=` voor deze vorm van verzoek om te werken.

  *Voorbeeld*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  In plaats van: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Niet-piramided TIFF- of vignetverzoeken geven een vergelijkbaar foutbericht aan

  *&quot;Afbeelding `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` heeft geen geldige DSF en het gebied van 2,25 MPixel overschrijdt de max van 2 MPixel&quot;* .

  De beste manier is om gepiramideerde TIFF en vignetten te gebruiken. Als u niet-gepiramideerde golven of vignetten moet gebruiken, volg de onderstaande instructies om de formaatlimiet te verhogen.

  *Omzetten*:

  Voor afbeeldingen die niet-gepiramideerde vignetten renderen, verhoogt u de eigenschapswaarde voor IrMaxNonPyrVignetteSize in het dialoogvenster [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuratiebestand.

  Verhoog de eigenschapswaarde voor Niet-gepiramideerde TIFF voor Afbeeldingsservice `MaxNonDsfSize` in de [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuratiebestand.

* Adobe [!DNL Photoshop] In CS3 worden gelaagde PSD-bestanden standaard niet opgeslagen als een samengestelde afbeelding.

  *Symptomen*:

  De Adobe [!DNL Photoshop] In CS3 gelaagd PSD-bestand wordt weergegeven als zwart met de tekst &#39;Deze gelaagde&#39; [!DNL Photoshop] bestand is niet opgeslagen met een samengestelde afbeelding.&quot; voor het Beeld dat antwoordbeeld serveert of in IPS.

  *Workaround*:

  De Adobe opslaan [!DNL Photoshop] CS3-bestand met maximale compatibiliteit ingeschakeld.

* Wanneer u een ICC-profiel toewijst aan een CMYK/JPEG-antwoordafbeelding, worden kleuren in sommige browsers omgekeerd.*Omzetten*:

  De indeling van de reactieafbeelding wijzigen met `fmt=`

* De grootte van de HTTP-reactie op afbeelding data-after compressie, inclusief bestandsheader-is beperkt tot 16 MB.
* &quot; ..&quot; is niet toegestaan in een padelement in HTTP-aanvragen.
* Door de gebruiker gemaakte of gewijzigde bestanden kunnen worden verwijderd uit *[!DNL install_root]* of een submap. Kopieer deze bestanden naar een andere locatie voordat u de installatie ongedaan maakt.

## Beperkingen die alleen van toepassing zijn op beeldservers {#section-b08ad535e4454265b8157dec244c4faf}

* Voorgrondkleuren in de RTF ( `\cf`) worden niet ondersteund voor PhotoFont-tekst.
* Het synchroniseren van vet, cursief en vet/cursief wordt geweigerd als een fout voor PhotoFont-tekst.
* Verticale tekstdoorloop wordt niet ondersteund voor PhotoFont-tekst.
* PNG-afbeeldingen met 16 bits per kanaal worden niet ondersteund voor PhotoFont-tekst.
* Voor kleurcorrecties voor PNG-afbeeldingen met ingesloten kleurprofielen worden opties met harde codes gebruikt. Render-intentie is relatief colorimetrisch en Blackpoint-compensatie is ingeschakeld voor PhotoFont-tekst.
* Opzoeken op basis van bestanden wordt niet ondersteund wanneer vertaling van landinstellingen in bedrijf is ingeschakeld [!DNL ini] bestand.
* Bij Beeldbewerking wordt niet-gesloten geschreven [!DNL Photoshop] paden correct.
* Afbeeldingsserver ondersteunt momenteel niet de verwerking van TIFF-bestanden die zijn geëxporteerd met Adobe Media Encoder 4.0.1 of eerder. Adobe Media Encoder is inbegrepen bij Premiere Pro CS4, After Effects CS4 en Creative Suite 4 Production Premium.
* Gebruiken `text=` met lagen die zichzelf aanpassen, ondersteunt geen RTF-tekenreeksen die meer dan één instelling gebruiken voor regeluitvulling.

  *Voorbeeld*

  RTF-tekenreeks kan niet zowel de uitvulling van de linker- als rechterregel gebruiken voor een tekstlaag waarvan het formaat automatisch wordt aangepast.

* SVG heeft een eigen eigenschap voor het opzoekpad van lettertypen waarnaar wordt verwezen en die niet zijn ingesloten in het SVG-bestand.

  *Symptomen*

  Gerenderde SVG-afbeeldingen met lettertypedefinities gebruiken een onjuist lettertype.

  *Workaround*

  De eigenschap instellen `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Uitsnijden wordt momenteel gebruikt `bgColor=` in plaats van `color=` om een nieuw uitgebreid gebied te vullen.

* Kleuromzetting is mogelijk niet correct wanneer `bgColor=` komt niet overeen met de basiskleurruimte met kleurprofielen.
* De effecten van de buitenste laag worden niet gerenderd als de laag geen masker of alpha-gegevens heeft.

## Beperkingen die alleen van toepassing zijn op het renderen van afbeeldingen {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decalen en wandmaterialen kunnen niet worden verwijderd.
* De grootte van structuren is beperkt ten opzichte van de grootte van de vignetweergave. In zeldzame gevallen kan de standaardlimiet van 425% van de weergavegrootte problemen opleveren met een toepassing die zeer grote niet-herhaalbare structuren gebruikt. Als het niet mogelijk is de toepassing of inhoud te wijzigen om binnen de vooraf gedefinieerde beperkingen te werken, kan het percentage als volgt worden verhoogd. Een teksteditor gebruiken, openen [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], zoeken `IrMaxTextureSizeFactor` en voer een nieuw percentage in. De verandering treedt onmiddellijk in werking zonder de Server van het Beeld opnieuw te beginnen.

* De JavaScript-engines in Netscape en Opera cache-responsgegevens, zelfs als de nocache-header is ingesteld. Dit interfereert met het correct functioneren van stateful verzoeken.

  *Workaround*

  Voeg een tijdstempel of andere unieke id toe aan de aanvraagtekenreeks, zoals `"&.ts=currentTime`.

## Beperkingen die alleen van toepassing zijn op nutsbedrijven {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`soms crasht met een segmentatiefout wanneer deze wordt gestopt met een `control-c`.
