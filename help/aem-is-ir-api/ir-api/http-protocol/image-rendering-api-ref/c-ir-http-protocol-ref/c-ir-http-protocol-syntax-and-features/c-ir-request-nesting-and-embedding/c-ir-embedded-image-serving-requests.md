---
title: Verzoeken voor Embedded Image Server
description: Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Verzoeken voor Embedded Image Server{#embedded-image-server-requests}

Een verzoek van de Server van het Beeld (IS) kan als materiaalbeeld worden gebruikt.

Geef de aanvraag op in het dialoogvenster `src=` als volgt:

` …&src=is( *[!DNL imageServingRequest]*)&…`

De `is` token is hoofdlettergevoelig.

De geneste aanvraag mag niet het hoofdpad van de afbeeldingsserver bevatten (doorgaans [!DNL http:// *[!DNL server]*/is/image/"]), maar bevat mogelijk regeltokens voor voorbewerking.

De volgende IS-opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen (in de aanvraag-URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Ook genegeerd `attribute::MaxPix` en `attribute::DefaultPix` van de afbeeldingscatalogus die van toepassing is op de ingesloten IS-aanvraag.

Als de resultaatafbeelding van de geneste aanvraag maskergegevens (alfa-gegevens) bevat, wordt deze altijd aan het materiaal doorgegeven. Gebruik een achtergrondafbeeldingslaag met een effen kleur om ongewenste alfa te voorkomen.

Het afbeeldingsresultaat van een ingesloten IS-aanvraag kan optioneel in de cache worden opgeslagen door `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld in een verschillend verzoek binnen een redelijke termijn opnieuw wordt gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
