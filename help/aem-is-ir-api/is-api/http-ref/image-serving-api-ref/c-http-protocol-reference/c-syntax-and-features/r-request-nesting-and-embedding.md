---
description: Image Serving ondersteunt het onbeperkt nesten van aanvragen voor beeldweergave, het insluiten van aanvragen voor het renderen van afbeeldingen en het insluiten van afbeeldingen die zijn opgehaald van externe servers. Deze mechanismen worden alleen ondersteund door laagafbeeldingen en laagmaskers.
seo-description: Image Serving ondersteunt het onbeperkt nesten van aanvragen voor beeldweergave, het insluiten van aanvragen voor het renderen van afbeeldingen en het insluiten van afbeeldingen die zijn opgehaald van externe servers. Deze mechanismen worden alleen ondersteund door laagafbeeldingen en laagmaskers.
seo-title: Nesten en insluiten aanvragen
solution: Experience Manager
title: Nesten en insluiten aanvragen
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Nesten en insluiten aanvragen{#request-nesting-and-embedding}

Image Serving ondersteunt het onbeperkt nesten van aanvragen voor beeldweergave, het insluiten van aanvragen voor het renderen van afbeeldingen en het insluiten van afbeeldingen die zijn opgehaald van externe servers. Deze mechanismen worden alleen ondersteund door laagafbeeldingen en laagmaskers.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Bepaalde e-mailclients en proxyservers kunnen de accolades coderen die worden gebruikt voor de syntaxis voor nesten en insluiten. Toepassingen waarvoor dit een probleem is, moeten haakjes gebruiken in plaats van accolades.

## Aanvragen voor geneste afbeeldingen {#section-6954202119e0466f8ff27c79f4f039c8}

Een volledige aanvraag voor het leveren van een afbeelding kan als een laagbron worden gebruikt door deze in de `src=` (of `mask=`) opdracht op te geven met behulp van de volgende syntaxis:

`…&src=is( nestedRequest)&…`

Het `is` token is hoofdlettergevoelig.

Het geneste verzoek mag niet het hoofdpad van de server bevatten (doorgaans ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>De geneste tekens van het aanvraagscheidingsteken ( `'(',')'`) en het bevelscheidingsteken ( `'?'`, `'&'`, `'='`) binnen genestelde verzoeken moeten niet HTTP-gecodeerd zijn. Geneste aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste (geneste) bestanden.

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

Wordt ook genegeerd `attribute::MaxPix`en `attribute::DefaultPix` van de afbeeldingscatalogus die van toepassing is op het geneste verzoek.

Het afbeeldingsresultaat van een geneste IS-aanvraag kan optioneel in de cache worden opgeslagen door de aanvraag op te nemen `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.

## Aanvragen voor het renderen van ingesloten afbeelding {#section-69c5548db930412b9b90d9b2951a6969}

Wanneer Scene7 het Teruggeven van het Beeld op de server wordt toegelaten, geef verzoeken terug kunnen als laagbronnen worden gebruikt door hen in src= (of mask=) bevel te specificeren. Gebruik de volgende syntaxis:

` …&src=ir( *[!DNL renderRequest]*)&…`

Het `ir` token is hoofdlettergevoelig.

*[!DNL renderRequest]* Dit is de gebruikelijke aanvraag voor het renderen van afbeeldingen, exclusief het HTTP-hoofdpad ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>De geneste tekens van het aanvraagscheidingsteken ( `'(',')'`) en het bevelscheidingsteken ( `'?'`, `'&'`, `'='`) binnen genestelde verzoeken moeten niet HTTP-gecodeerd zijn. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

De volgende opdrachten voor het renderen van afbeeldingen worden genegeerd wanneer deze worden opgegeven in geneste aanvragen:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Wordt ook genegeerd `attribute::MaxPix` en `attribute::DefaultPix` van de materiaalcatalogus die van toepassing is op het geneste renderverzoek.

Het beeldresultaat van een genest verzoek van AIR kan naar keuze in het voorgeheugen onder worden gebracht door te omvatten `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.

## Ingesloten FXG-renderaanvragen {#section-c817e4b4f7da414ea5a51252ca7e120a}

Wanneer de FXG grafische renderer (ook bekend als [!DNL AGMServer]) is geïnstalleerd en ingeschakeld met Image Serving, kunnen FXG-aanvragen worden gebruikt als laagbronnen door deze op te geven in `src=` (of `mask=`) opdrachten. Gebruik de volgende syntaxis:

`…&src=fxg( renderRequest)&…`

Het `fxg` token is hoofdlettergevoelig.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>FXG grafisch teruggeven is beschikbaar slechts in Scene7 ontvangen milieu en kan extra vergunning vereisen. De Steun van Scene7 van het contact voor meer informatie.

*[!DNL renderRequest]* is de gebruikelijke FXG-renderaanvraag, exclusief het HTTP-hoofdpad ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>De scheidingstekens ( `'(',')'`) en de opdrachtscheidingstekens ( `'?'`, `'&'`, `'='`) binnen geneste aanvragen mogen niet via HTTP worden gecodeerd. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

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

Als u een externe URL voor een `src=` opdracht of een `mask=` opdracht wilt opgeven, scheidt u het externe URL- of URL-fragment met haakjes:

`…&src=( foreignUrl)&…`

Belangrijk De scheidingstekens ( `'(',')'`) en de bevelafbakeningstekens ( `'?'`, `'&'`, `'='`) binnen genestelde verzoeken moeten niet HTTP-Gecodeerd zijn. Ingesloten aanvragen moeten feitelijk op dezelfde manier worden gecodeerd als de aanvraag voor buitenste insluiten.

Volledige absolute URL&#39;s (indien `attribute::AllowDirectUrls` ingesteld) en URL&#39;s ten opzichte van `attribute::RootUrl` zijn toegestaan. Er treedt een fout op als een absolute URL is ingesloten en een kenmerk: 0 `AllowDirectUrls` is of als een relatieve URL is opgegeven en leeg `attribute::RootUrl` is.

Hoewel externe URL&#39;s niet rechtstreeks in de padcomponent van de aanvraag-URL kunnen worden opgegeven, is het mogelijk een voorbewerkingsregel in te stellen om de conversie van relatieve paden naar absolute URL&#39;s toe te staan (zie het voorbeeld hieronder).

Externe afbeeldingen worden door de server in het cachegeheugen opgeslagen volgens de headers die bij de HTTP-respons worden geleverd. Als er geen responsheader van het type Last-Modified HTTP `ETag` aanwezig is, wordt de reactie niet in de cache geplaatst. Dit kan slechte prestaties voor herhaalde toegang tot het zelfde buitenlandse beeld veroorzaken, aangezien de Serving van het Beeld het beeld bij elke toegang moet re-halen en opnieuw bevestigen.

Dit mechanisme ondersteunt dezelfde indelingen voor afbeeldingsbestanden die worden ondersteund door het hulpprogramma Image Convert (IC), met uitzondering van bronafbeeldingen met 16 bits per component.

>[!NOTE] {class=&quot;- topic/note &quot;}
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

**Verzoeken om scene7-beeldrendering insluiten**

een sjabloon gebruiken die is opgeslagen in [!DNL myCatalog/myTemplate]; produceer het beeld voor laag2 van het malplaatje gebruikend Scene7 het Teruggeven van het Beeld:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Noteer de geneste accolades. Met de aanvraag Afbeelding renderen sluit u een aanroep terug naar Image Serving om een herhaalbare structuur op te halen.

## Zie ook {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Verzoek om voorbewerking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Verwijzing naar rendering van afbeeldingen, [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Hulpprogramma&#39;s voor [afbeeldingsservices](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
