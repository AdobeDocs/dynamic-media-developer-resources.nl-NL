---
description: Foutopsporingsverzoek. Met deze foutopsporingsopdracht wordt de aanvraag geparseerd en vooraf verwerkt, worden de opzoekingen in de afbeeldingscatalogus, de opname van de catalogus, de macro- en variabelevervangingen enzovoort uitgevoerd, net als req=img.
solution: Experience Manager
title: oplossen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# oplossen{#resolve}

Foutopsporingsverzoek. Met deze foutopsporingsopdracht wordt de aanvraag geparseerd en vooraf verwerkt, worden de opzoekingen in de afbeeldingscatalogus uitgevoerd, wordt de catalogus:Modifier-insluitingen, macro- en variabelevervangingen enz., net als req=img.

`req=resolve`

De laatste verzoektekenreeks wordt geretourneerd in plaats van de resultaatafbeelding, met het MIME-type `text/plain`.

De HTTP-respons is niet cacheable.
