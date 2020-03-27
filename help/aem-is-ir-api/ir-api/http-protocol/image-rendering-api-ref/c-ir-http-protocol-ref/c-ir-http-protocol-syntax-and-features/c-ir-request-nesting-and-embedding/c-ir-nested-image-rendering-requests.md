---
description: Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.
seo-description: Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.
seo-title: Aanvragen voor het renderen van geneste afbeeldingen
solution: Experience Manager
title: Aanvragen voor het renderen van geneste afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Aanvragen voor het renderen van geneste afbeeldingen{#nested-image-rendering-requests}

Voor geavanceerde toepassingen is het mogelijk het resultaat van een renderbewerking als een materiaalafbeelding te gebruiken, net als een afbeelding die is verkregen uit Beeldbewerking.

Een renderverzoek kan als materiaalbeeld worden gebruikt door het in het `src=` bevel als volgt te specificeren:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Het `ir` token is hoofdlettergevoelig.

Het geneste verzoek mag (gewoonlijk `http:// *[!DNL server]*/ir/render/'`) niet het hoofdpad voor het renderen van afbeeldingen bevatten, maar kan regeltokens voor voorbewerking bevatten.

De volgende opdrachten worden genegeerd wanneer deze worden opgegeven in geneste aanvragen (in de aanvraag-URL of in `catalog::Modifier` of `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Wordt ook genegeerd `attribute::MaxPix` en `attribute::DefaultPix` van de materiaalcatalogus die van toepassing is op het geneste renderverzoek.

Het beeldresultaat van een genest verzoek van AIR kan naar keuze in het voorgeheugen onder worden gebracht door te omvatten `cache=on`. Het in cache plaatsen van tussentijdse gegevens is standaard uitgeschakeld. Caching zou slechts moeten worden toegelaten wanneer het middenbeeld naar verwachting in een verschillend verzoek binnen een redelijke termijn opnieuw zal worden gebruikt. Standaard cachebeheer op de server is van toepassing. Gegevens worden in cache opgeslagen in een indeling zonder gegevensverlies.
