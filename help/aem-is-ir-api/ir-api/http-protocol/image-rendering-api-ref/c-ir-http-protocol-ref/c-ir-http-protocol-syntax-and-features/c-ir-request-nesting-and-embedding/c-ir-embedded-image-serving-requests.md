---
description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
solution: Experience Manager
title: Verzoeken voor Embedded Image Server
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
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
