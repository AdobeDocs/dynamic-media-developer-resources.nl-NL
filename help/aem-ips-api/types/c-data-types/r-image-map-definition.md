---
description: Definitie van doel voor een klikactie in browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
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
