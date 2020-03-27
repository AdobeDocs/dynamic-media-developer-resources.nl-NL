---
description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
seo-description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
seo-title: Fouten
solution: Experience Manager
title: Fouten
topic: Scene7 Image Serving - Image Rendering API
uuid: a08f3f5a-3013-4d35-9612-25190a4c99fa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fouten{#errors}

Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.

De responsstatuswaarde is afhankelijk van het type fout; voor de meest voorkomende fouten is het &quot; 403 &quot; . De reacties van de fout voor niet-beeldverzoektypes in overeenstemming met het formaat gespecificeerd met `req=`. (Kan momenteel niet consistent worden geïmplementeerd.)

De hoeveelheid details inbegrepen in het foutenbericht is configureerbaar met `attribute::ErrorDetail`.

## Foutafbeeldingen {#section-92e9b20b2507433daa96923abc95f777}

De Server van het beeld kan worden gevormd om foutenmeldingen terug te keren die in een beeld worden teruggegeven.

Zie [kenmerk::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) in the image catalog reference for details.

Als de foutenafbeelding met succes wordt geproduceerd, is de status van de reactie van HTTP 200. Als er een fout optreedt bij het verwerken van de foutafbeelding, worden de standaard HTTP-foutreactie en het tekstbericht aan de client geretourneerd.

## Standaardafbeelding {#section-66bf25fe6b434081bfae96d38d9be25e}

U kunt instellen dat een ontbrekende afbeelding wordt vervangen door een standaardafbeelding. De standaardafbeelding kan met `attribute::DefaultImage` of met de `defaultImage=` opdracht worden opgegeven.

## Zie ook {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
