---
description: Doel voor een klikactie in browser.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# ImageMap{#imagemap}

Doel voor een klikactie in browser.

Altijd gekoppeld aan een afbeelding. U kunt een `ImageMap` doel van `ImageInfo`.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| imageMapHandle | `xsd:string` | Afbeeldingskaart. |
| name | `xsd:string` | Naam afbeelding met hyperlinks. |
| regio | `xsd:string` | Coördinaten van afbeeldingen met hyperlinks. De indeling is gebaseerd op de HTML `<area>` tagkenmerk. |
| action | `xsd:string` | Andere kenmerken die in de HTML moeten worden opgenomen `<area>` -tag, inclusief de `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] waarde. |
| position | `xsd:string` | Positie in de notatie van de HTML `<area>` element [!DNL coords] kenmerk. Bijvoorbeeld: `coords ="0,0,84,128"`. |
| enabled | `xsd:boolean` | True if image map is enabled. |
| lastModified | `xsd:dateTime` | Datum en tijd waarop de afbeelding met hyperlinks voor het laatst is gewijzigd. |
