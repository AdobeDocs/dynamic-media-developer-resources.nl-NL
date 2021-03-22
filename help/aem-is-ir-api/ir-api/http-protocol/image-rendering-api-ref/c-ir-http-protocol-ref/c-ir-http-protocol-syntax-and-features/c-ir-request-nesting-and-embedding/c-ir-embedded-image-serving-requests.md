---
description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
seo-description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
seo-title: Verzoeken voor Embedded Image Server
solution: Experience Manager
title: Verzoeken voor Embedded Image Server
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Verzoeken voor Embedded Image Server{#embedded-image-server-requests}

Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.

Geef het verzoek als volgt op in de opdracht `src=`:

` …&src=is( *[!DNL imageServingRequest]*)&…`

De token `is` is hoofdlettergevoelig.

Het geneste verzoek mag niet het hoofdpad van de afbeeldingsserver bevatten (doorgaans [!DNL http:// *[!DNL server]*/is/image/&quot;]), maar kan regeltokens voor voorbewerking bevatten.

De volgende IS bevelen worden genegeerd wanneer gespecificeerd in genestelde verzoeken (of in het verzoek URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Ook worden `attribute::MaxPix` en `attribute::DefaultPix` van de afbeeldingscatalogus genegeerd die op de ingesloten IS-aanvraag van toepassing is.

Als de resultaatafbeelding van de geneste aanvraag maskergegevens (alfa-gegevens) bevat, wordt deze altijd aan het materiaal doorgegeven. Gebruik een achtergrondafbeeldingslaag met een effen kleur om ongewenste alfa te voorkomen.

Het afbeeldingsresultaat van een ingesloten IS-aanvraag kan optioneel in de cache worden opgeslagen door `cache=on` op te nemen. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
