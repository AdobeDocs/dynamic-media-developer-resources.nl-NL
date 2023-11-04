---
description: Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.
solution: Experience Manager
title: Fouten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Fouten{#errors}

Als een aanvraag niet met succes kan worden voltooid, retourneert de server een foutafbeelding of een andere HTTP-antwoordstatus dan 200, samen met een foutbericht.

De responsstatuswaarde is afhankelijk van het type fout; voor de meeste voorkomende fouten is de waarde &#39;403&#39;. Foutreacties voor aanvraagtypen die geen afbeelding zijn, komen overeen met de indeling die is opgegeven met `req=`. (Kan momenteel niet consistent worden geïmplementeerd.)

De hoeveelheid details in het foutbericht kan worden geconfigureerd met `attribute::ErrorDetail`.

## Foutafbeeldingen {#section-92e9b20b2507433daa96923abc95f777}

De Server van het beeld kan worden gevormd om foutenmeldingen terug te keren die in een beeld worden teruggegeven.

Zie [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) in de naslaggids voor de afbeeldingscatalogus voor meer informatie.

Als de foutenafbeelding met succes wordt geproduceerd, is de status van de reactie van HTTP 200. Als er een fout optreedt bij het verwerken van de foutafbeelding, worden de standaard HTTP-foutreactie en het tekstbericht aan de client geretourneerd.

## Standaardafbeelding {#section-66bf25fe6b434081bfae96d38d9be25e}

U kunt instellen dat een ontbrekende afbeelding wordt vervangen door een standaardafbeelding. De standaardafbeelding kan worden opgegeven met `attribute::DefaultImage` of de `defaultImage=` gebruiken.

## Zie ook {#section-e261d7f224ca4546bb64bf8cb909db08}

[kenmerk::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
