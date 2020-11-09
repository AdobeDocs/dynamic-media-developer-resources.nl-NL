---
description: Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.
seo-description: Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.
seo-title: Verzoek vergrendelen
solution: Experience Manager
title: Verzoek vergrendelen
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 6b51248cdc6a6b9d36893545640dbbeb11a0c414
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Verzoek vergrendelen{#request-locking}

Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.

Als attribute::RequestLock wordt geplaatst, moet een slotwaarde aan het verzoek, in vorm van worden toegevoegd, `&xxxx`, met xxxx een vier cijferhexadecimale waarde is. Deze hexadecimale waarde wordt gegenereerd met een eenvoudig hash-algoritme dat wordt toegepast op het gedeelte *modifiers* van het verzoek (na &#39;?&#39; dat het URL-pad scheidt van de *wijzigingstoetsen*). Dit moet worden gedaan nadat het verzoek volledig http-encoded is, maar alvorens het (naar keuze) wordt verduisterd. Nadat de-obfuscating van het verzoek, zal de server het zelfde het hakken algoritme op het bepalingskoord (exclusief de laatste 5 karakters, die de slotwaarde bevatten) gebruiken. Als de gegenereerde sleutel niet overeenkomt met de vergrendeling, wordt het verzoek afgewezen.

>[!IMPORTANT]
>
>Als u deze functie inschakelt, dient u er rekening mee te houden dat er bepaalde gebruiksbeperkingen zijn, waaronder de volgende:<br>- De gebruikersinterface Dynamische media geeft mogelijk niet de juiste details voor het **[!UICONTROL Last Published]** veld weer. Dit heeft echter geen invloed op de uitgeverij.<br>- HLS-videostreaming werkt momenteel niet wanneer **[!UICONTROL Request Obfuscation]** en **[!UICONTROL Request Locking]** wordt ingeschakeld.

C++ steekproefcode om de waarde van de verzoekslot te produceren:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Zie ook {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
