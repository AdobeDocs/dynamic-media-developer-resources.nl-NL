---
description: Bestandsopties voor PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# [!DNL PDFOptions]{#pdfoptions}

Bestandsopties voor PDF.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| proces | `xsd:string` | Keuze uit &quot;PDF-processen&quot;. |
| resolutie | `xsd:double` | Bestandsresolutie. |
| kleurruimte | `xsd:string` | Modus voor kleurruimte na het script. |
| pdfCatalog | `xsd:boolean` | Of een PDF van meerdere pagina&#39;s na het renderen in een eCatalog moet worden gecombineerd (de standaardwaarde is true). |
| extractSearchWords | `xsd:boolean` | Of zoekwoorden uit het PDF-bestand moeten worden geëxtraheerd. |
| extractLinks | `xsd:boolean` | Of u PDF-koppelingen wilt extraheren naar afbeeldingen met hyperlinks die zijn toegewezen aan gerasterde pagina&#39;s in IPS. |
