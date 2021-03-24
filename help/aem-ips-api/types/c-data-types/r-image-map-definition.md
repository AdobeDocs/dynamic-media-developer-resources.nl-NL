---
description: Definitie van doel voor een klikactie in browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# ImageMapDefinition{#imagemapdefinition}

Definitie van doel voor een klikactie in browser.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`name`*` | `xsd:string` | De naam van de definitie van de afbeelding met hyperlinks. |
| `*`shapeType`*` | `xsd:string` | Een van de waarden voor de gebiedvorm. |
| `*`regio`*` | `xsd:string` | Coördinaten van afbeeldingen met hyperlinks. De opmaak is gebaseerd op de tagkenmerken van HTML `<area>`. |
| `*`action`*` | `xsd:string` | Andere kenmerken die moeten worden opgenomen in de HTML-tag `<area>`, inclusief de URL `href`. |
| `*`enabled`*` | `xsd:boolean` | True if the image map is enabled. |

