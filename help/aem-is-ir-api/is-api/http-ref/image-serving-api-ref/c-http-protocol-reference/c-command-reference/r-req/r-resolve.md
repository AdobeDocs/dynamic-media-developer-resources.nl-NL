---
description: Foutopsporingsverzoek. Met deze foutopsporingsopdracht wordt de aanvraag geparseerd en vooraf verwerkt, worden de opzoekingen in de afbeeldingscatalogus, de opname van de catalogus, de macro- en variabelevervangingen enzovoort uitgevoerd, net als req=img.
solution: Experience Manager
title: oplossen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# resolve{#resolve}

Foutopsporingsverzoek. Met deze foutopsporingsopdracht wordt de aanvraag geparseerd en vooraf verwerkt, worden de opzoekingen in de afbeeldingscatalogus uitgevoerd, wordt de catalogus:Modifier-insluitingen, macro- en variabelevervangingen enz., net als req=img.

`req=resolve`

De laatste verzoektekenreeks wordt geretourneerd in plaats van de resultaatafbeelding, met het MIME-type `text/plain`.

De HTTP-respons is niet cacheable.
