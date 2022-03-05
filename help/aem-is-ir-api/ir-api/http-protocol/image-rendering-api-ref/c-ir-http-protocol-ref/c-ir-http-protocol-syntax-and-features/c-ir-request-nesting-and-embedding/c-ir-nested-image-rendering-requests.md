---
title: Aanvragen voor het renderen van geneste afbeeldingen
description: Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Aanvragen voor het renderen van geneste afbeeldingen{#nested-image-rendering-requests}

Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Image Serving.

Een renderverzoek kan als een materiaalafbeelding worden gebruikt door deze op te geven in het dialoogvenster `src=` als volgt:

` …&src=ir{ *[!DNL renderRequest]*}&…`

De `ir` token is hoofdlettergevoelig.

De geneste aanvraag mag het hoofdpad voor het renderen van afbeeldingen niet bevatten (doorgaans `http:// *[!DNL server]*/ir/render/'`), maar bevat mogelijk regeltokens voor voorbewerking.

De volgende opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen (in de aanvraag-URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Ook genegeerd `attribute::MaxPix` en `attribute::DefaultPix` van de materiaalcatalogus die van toepassing is op de geneste renderaanvraag.

Het beeldresultaat van een genest verzoek van AIR kan naar keuze in het voorgeheugen worden opgeslagen door te omvatten `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld in een verschillend verzoek binnen een redelijke termijn opnieuw wordt gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
