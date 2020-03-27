---
description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
seo-description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
seo-title: Verzoeken voor Embedded Image Server
solution: Experience Manager
title: Verzoeken voor Embedded Image Server
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verzoeken voor Embedded Image Server{#embedded-image-server-requests}

Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.

Geef de aanvraag als volgt op in de `src=` opdracht:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Het `is` token is hoofdlettergevoelig.

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

Wordt ook genegeerd `attribute::MaxPix` en `attribute::DefaultPix` van de afbeeldingscatalogus die van toepassing is op de ingesloten IS-aanvraag.

Als de resultaatafbeelding van de geneste aanvraag maskergegevens (alfa-gegevens) bevat, wordt deze altijd aan het materiaal doorgegeven. Gebruik een achtergrondafbeeldingslaag met een effen kleur om ongewenste alfa te voorkomen.

Het afbeeldingsresultaat van een ingesloten IS-aanvraag kan optioneel in de cache worden opgeslagen door de afbeelding op te nemen `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
