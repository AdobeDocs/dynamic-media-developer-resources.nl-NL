---
description: Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.
seo-description: Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.
seo-title: Aanvragen voor het renderen van geneste afbeeldingen
solution: Experience Manager
title: Aanvragen voor het renderen van geneste afbeeldingen
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# Aanvragen voor geneste rendering van afbeeldingen{#nested-image-rendering-requests}

Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.

Een renderverzoek kan als materiaalbeeld worden gebruikt door het in het `src=` bevel als volgt te specificeren:

` …&src=ir{ *[!DNL renderRequest]*}&…`

De token `ir` is hoofdlettergevoelig.

Het geneste verzoek mag niet het pad naar het renderen van de afbeelding (doorgaans `http:// *[!DNL server]*/ir/render/'`) bevatten, maar kan wel regeltokens voor voorbewerking bevatten.

De volgende opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen (in de aanvraag-URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Ook worden `attribute::MaxPix` en `attribute::DefaultPix` van de materiaalcatalogus genegeerd die op het genestelde teruggeven verzoek van toepassing is.

Het beeldresultaat van een genest verzoek van AIR kan naar keuze door `cache=on` te omvatten worden in het voorgeheugen ondergebracht. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
