---
title: Fouten
description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Fouten{#errors}

Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.

De responsstatuswaarde is afhankelijk van het type fout; voor de meest voorkomende fouten is het &quot; 403 &quot; . Foutreacties voor aanvraagtypen die geen afbeelding zijn, komen overeen met de indeling die is opgegeven met `req=`. (Mogelijk wordt momenteel niet consistent geïmplementeerd.)

De hoeveelheid details in het foutbericht kan worden geconfigureerd met `attribute::ErrorDetail`.

**Foutafbeeldingen**

De Server van het beeld kan worden gevormd om foutenmeldingen terug te keren die in een beeld worden teruggegeven. Zie `attribute::ErrorImage` in de naslaggids voor de afbeeldingscatalogus voor meer informatie. Als de foutenafbeelding met succes wordt geproduceerd, is de status van de reactie van HTTP 200. Als er een fout optreedt bij het verwerken van de foutafbeelding, worden de standaard HTTP-foutreactie en het tekstbericht aan de client geretourneerd.

**Zie ook**

[kenmerk::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
