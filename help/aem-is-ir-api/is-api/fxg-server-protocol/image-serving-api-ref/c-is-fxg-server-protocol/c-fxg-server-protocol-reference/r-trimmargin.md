---
description: Bijsnijdmarge instellen. Hiermee stelt u de snijmarge in die in het PDF-bestand is ingesteld.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Bijsnijdmarge instellen. Hiermee stelt u de snijmarge in die in het PDF-bestand is ingesteld.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punten

Standaard wordt `trimMargin` ingesteld op de volledige grootte van het document dat wordt gedefinieerd door `viewWidth` en `viewHeight`. De waarden *[!DNL left]*, *[!DNL bottom]* en *[!DNL right]* worden standaard ingesteld op de waarde *[!DNL top]* als deze niet is opgegeven.
