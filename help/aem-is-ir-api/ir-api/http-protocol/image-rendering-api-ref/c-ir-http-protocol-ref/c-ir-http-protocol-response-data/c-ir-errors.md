---
description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
seo-description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
seo-title: Fouten
solution: Experience Manager
title: Fouten
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Fouten{#errors}

Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.

De responsstatuswaarde is afhankelijk van het type fout; voor de meest voorkomende fouten is het &quot; 403 &quot; . De reacties van de fout voor niet-beeldverzoektypes in overeenstemming met het formaat met `req=` wordt gespecificeerd. (Mogelijk is dit momenteel niet consistent geïmplementeerd.)

De hoeveelheid details inbegrepen in het foutenbericht is configureerbaar met `attribute::ErrorDetail`.

**Foutafbeeldingen**

De Server van het beeld kan worden gevormd om foutenmeldingen terug te keren die in een beeld worden teruggegeven. Zie `attribute::ErrorImage` in de verwijzing naar de afbeeldingscatalogus voor meer informatie. Als de foutenafbeelding met succes wordt geproduceerd, is de status van de reactie van HTTP 200. Als er een fout optreedt bij het verwerken van de foutafbeelding, worden de standaard HTTP-foutreactie en het tekstbericht aan de client geretourneerd.

**Zie ook**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
