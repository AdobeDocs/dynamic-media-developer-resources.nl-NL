---
description: Definitie van doel voor een klikactie in browser.
seo-description: Definitie van doel voor een klikactie in browser.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
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

