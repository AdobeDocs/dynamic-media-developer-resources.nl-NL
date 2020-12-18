---
description: Doel voor een klikactie in browser.
seo-description: Doel voor een klikactie in browser.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# ImageMap{#imagemap}

Doel voor een klikactie in browser.

Altijd gekoppeld aan een afbeelding. U kunt een `ImageMap` doel van `ImageInfo` krijgen.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Afbeeldingskaart. |
| ` *`name`*` | `xsd:string` | Naam afbeelding met hyperlinks. |
| ` *`regio`*` | `xsd:string` | Coördinaten van afbeeldingen met hyperlinks. De indeling is gebaseerd op het tagkenmerk HTML `<area>`. |
| ` *`action`*` | `xsd:string` | Andere kenmerken die moeten worden opgenomen in de HTML-tag `<area>`, inclusief de URL `href`. |
| ` *`shapeType`*` | `xsd:boolean` | Een waarde [!DNL RegionShape]. |
| ` *`position`*` | `xsd:string` | Positie in de indeling van het `<area>`-kenmerk van het HTML-element [!DNL coords]. Bijvoorbeeld: `coords ="0,0,84,128"`. |
| ` *`enabled`*` | `xsd:boolean` | True if image map is enabled. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum en tijd waarop de afbeelding met hyperlinks voor het laatst is gewijzigd. |

