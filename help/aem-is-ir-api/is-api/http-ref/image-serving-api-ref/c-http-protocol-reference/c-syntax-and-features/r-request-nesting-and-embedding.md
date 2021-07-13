---
description: Image Serving ondersteunt het onbeperkt nesten van aanvragen voor beeldweergave, het insluiten van aanvragen voor het renderen van afbeeldingen en het insluiten van afbeeldingen die zijn opgehaald van externe servers. Deze mechanismen worden alleen ondersteund door laagafbeeldingen en laagmaskers.
solution: Experience Manager
title: Nesten en insluiten aanvragen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Nesten en insluiten aanvragen{#request-nesting-and-embedding}

Image Serving ondersteunt het onbeperkt nesten van aanvragen voor beeldweergave, het insluiten van aanvragen voor het renderen van afbeeldingen en het insluiten van afbeeldingen die zijn opgehaald van externe servers. Deze mechanismen worden alleen ondersteund door laagafbeeldingen en laagmaskers.

>[!NOTE]
>
>Bepaalde e-mailclients en proxyservers kunnen de accolades coderen die worden gebruikt voor de syntaxis voor nesten en insluiten. Toepassingen waarvoor dit een probleem is, moeten haakjes gebruiken in plaats van accolades.

## Aanvragen voor geneste afbeeldingen {#section-6954202119e0466f8ff27c79f4f039c8}

Een volledige aanvraag voor het leveren van een afbeelding kan als een laagbron worden gebruikt door deze op te geven in de opdracht `src=` (of `mask=`) met behulp van de volgende syntaxis:

`…&src=is( nestedRequest)&…`

De token `is` is hoofdlettergevoelig.

Het geneste verzoek mag niet het hoofdpad van de server bevatten (gewoonlijk ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>De geneste tekens van het aanvraagscheidingsteken ( `'(',')'`) en de opdrachtscheidingstekens ( `'?'`, `'&'`, `'='`) binnen geneste aanvragen mogen niet HTTP-gecodeerd zijn. Geneste aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste (geneste) bestanden.

Regels voor voorbewerking worden toegepast op geneste aanvragen.

De volgende opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen (in de aanvraag-URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Als de resultaatafbeelding van de geneste aanvragen maskergegevens (alfa-gegevens) bevat, wordt deze als laagmasker doorgegeven aan de insluitlaag.

Ook worden `attribute::MaxPix`en `attribute::DefaultPix` van de afbeeldingscatalogus genegeerd die van toepassing is op het geneste verzoek.

Het afbeeldingsresultaat van een genest IS-verzoek kan optioneel in de cache worden opgeslagen door `cache=on` op te nemen. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.

## Aanvragen voor het renderen van ingesloten afbeelding {#section-69c5548db930412b9b90d9b2951a6969}

Wanneer Dynamic Media Image Rendering is ingeschakeld op de server, kunnen renderverzoeken worden gebruikt als laagbronnen door deze op te geven in de opdracht src= (of mask=). Gebruik de volgende syntaxis:

` …&src=ir( *[!DNL renderRequest]*)&…`

De token `ir` is hoofdlettergevoelig.

*[!DNL renderRequest]* Dit is de gebruikelijke aanvraag voor het renderen van afbeeldingen, exclusief het HTTP-hoofdpad  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>De geneste tekens van het aanvraagscheidingsteken ( `'(',')'`) en de opdrachtscheidingstekens ( `'?'`, `'&'`, `'='`) binnen geneste aanvragen mogen niet HTTP-gecodeerd zijn. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

De volgende opdrachten voor het renderen van afbeeldingen worden genegeerd wanneer deze worden opgegeven in geneste aanvragen:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Ook worden `attribute::MaxPix` en `attribute::DefaultPix` van de materiaalcatalogus genegeerd die op het genestelde teruggeven verzoek van toepassing is.

Het beeldresultaat van een genest verzoek van AIR kan naar keuze door `cache=on` te omvatten worden in het voorgeheugen ondergebracht. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.

## Ingesloten FXG-renderaanvragen {#section-c817e4b4f7da414ea5a51252ca7e120a}

Wanneer de FXG grafische renderer (ook bekend als [!DNL AGMServer]) is geïnstalleerd en ingeschakeld met Image Serving, kunnen FXG-aanvragen worden gebruikt als laagbronnen door deze op te geven in `src=` (of `mask=`)-opdrachten. Gebruik de volgende syntaxis:

`…&src=fxg( renderRequest)&…`

De token `fxg` is hoofdlettergevoelig.

>[!NOTE]
>
>FXG-rendering van afbeeldingen is alleen beschikbaar in de door Dynamic Media gehoste omgeving en vereist mogelijk extra licenties. Neem contact op met de technische ondersteuning van Dynamic Media voor meer informatie.

*[!DNL renderRequest]* is de gebruikelijke FXG-renderaanvraag, exclusief het HTTP-hoofdpad  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>De scheidingstekens ( `'(',')'`) en de opdrachtscheidingstekens ( `'?'`, `'&'`, `'='`) binnen geneste aanvragen mogen niet HTTP-gecodeerd zijn. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

De volgende FXG-opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Externe afbeeldingsbronnen {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP-servers.

>[!NOTE]
>
>Alleen het HTTP-protocol wordt ondersteund voor externe URL&#39;s.

Als u een externe URL wilt opgeven voor een opdracht `src=` of `mask=`, scheidt u het externe URL- of URL-fragment met haakjes:

`…&src=( foreignUrl)&…`

Belangrijk De scheidingstekens ( `'(',')'`) en de bevelafbakeningstekens ( `'?'`, `'&'`, `'='`) binnen genestelde verzoeken moeten niet HTTP-gecodeerd zijn. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

Volledige absolute URL&#39;s (als `attribute::AllowDirectUrls` is ingesteld) en URL&#39;s ten opzichte van `attribute::RootUrl` zijn toegestaan. Er treedt een fout op als een absolute URL is ingesloten en een kenmerk: `AllowDirectUrls` is 0, of als een relatieve URL wordt gespecificeerd en `attribute::RootUrl` leeg is.

Hoewel externe URL&#39;s niet rechtstreeks in de padcomponent van de aanvraag-URL kunnen worden opgegeven, is het mogelijk een voorbewerkingsregel in te stellen om de conversie van relatieve paden naar absolute URL&#39;s toe te staan (zie het voorbeeld hieronder).

Externe afbeeldingen worden door de server in het cachegeheugen opgeslagen volgens de headers die bij de HTTP-respons worden geleverd. Als er noch een `ETag` noch een laatste-Gewijzigde HTTP-antwoordheader aanwezig is, wordt de reactie niet in de cache geplaatst. Dit kan slechte prestaties voor herhaalde toegang tot het zelfde buitenlandse beeld veroorzaken, aangezien de Serving van het Beeld het beeld bij elke toegang moet re-halen en opnieuw bevestigen.

Dit mechanisme ondersteunt dezelfde indelingen voor afbeeldingsbestanden die worden ondersteund door het hulpprogramma Image Convert (IC), met uitzondering van bronafbeeldingen met 16 bits per component.

>[!NOTE]
>
>Bij Beeldserver wordt het hulpprogramma voor validatie automatisch uitgevoerd wanneer een extern image voor het eerst wordt gebruikt, om te controleren of het image geldig is en tijdens de overdracht niet is beschadigd. Dit kan een lichte vertraging bij eerste toegang veroorzaken. Voor de beste prestaties is het raadzaam de grootte van dergelijke afbeeldingen te beperken en/of een indeling voor afbeeldingsbestanden te gebruiken die goed comprimeert.

## Beperkingen {#section-fb68e3f0d40947feb94d7bf183b64929}

De grootte van de afbeelding die wordt gegenereerd door geneste/ingesloten aanvragen, wordt normaal gesproken automatisch geoptimaliseerd. Als plaatsing in cache van geneste aanvraagafbeeldingen is ingeschakeld, kunnen de prestaties toenemen door de exacte grootte van de geneste afbeelding op te geven, zodat er geen verdere schaling nodig is wanneer het cacheitem opnieuw wordt gebruikt.

De belangrijke Serving van het Beeld steunt dubbel-coderen van genestelde of ingebedde verzoeken niet. Geneste en ingesloten aanvragen moeten net als eenvoudige aanvragen HTTP-gecodeerd zijn.

## Voorbeelden {#section-d800cfc31abe46d2a964f8e7929231f1}

**Laagsjabloon met caching:**

Met nesten kunt u caching toevoegen aan een laagsjabloon. Een beperkt aantal achtergrondafbeeldingen wordt bedekt met zeer variabele tekst. De eerste sjabloontekenreeks ziet er als volgt uit:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Met kleine wijzigingen kunnen we de afbeelding met laag 0 vooraf schalen en deze blijvend in cache plaatsen, waardoor de serverlading afneemt:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Aanvragen voor Dynamic Media-beeldweergave insluiten**

Een sjabloon gebruiken die is opgeslagen in [!DNL myCatalog/myTemplate]; de afbeelding voor laag2 van de sjabloon genereren met Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Noteer de geneste accolades. Met de aanvraag Afbeelding renderen sluit u een aanroep terug naar Image Serving om een herhaalbare structuur op te halen.

## Zie ook {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Verzoek om PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Verwijzing van de Teruggave van Beeld,  [Malplaatjes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), de Hulpprogramma&#39;s van de  [Beelddienst](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
