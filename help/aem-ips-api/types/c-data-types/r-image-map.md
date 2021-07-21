---
description: Doel voor een klikactie in browser.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# ImageMap{#imagemap}

Doel voor een klikactie in browser.

Altijd gekoppeld aan een afbeelding. U kunt een `ImageMap` doel van `ImageInfo` krijgen.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Afbeeldingskaart. |
| `*`name`*` | `xsd:string` | Naam afbeelding met hyperlinks. |
| `*`regio`*` | `xsd:string` | Coördinaten van afbeeldingen met hyperlinks. De indeling is gebaseerd op het tagkenmerk HTML `<area>`. |
| `*`action`*` | `xsd:string` | Andere kenmerken die moeten worden opgenomen in de HTML-tag `<area>`, inclusief de URL `href`. |
| `*`shapeType`*` | `xsd:boolean` | Een waarde [!DNL RegionShape]. |
| `*`position`*` | `xsd:string` | Positie in de indeling van het `<area>`-kenmerk van het HTML-element [!DNL coords]. Bijvoorbeeld: `coords ="0,0,84,128"`. |
| `*`enabled`*` | `xsd:boolean` | True if image map is enabled. |
| `*`lastModified`*` | `xsd:dateTime` | Datum en tijd waarop de afbeelding met hyperlinks voor het laatst is gewijzigd. |
