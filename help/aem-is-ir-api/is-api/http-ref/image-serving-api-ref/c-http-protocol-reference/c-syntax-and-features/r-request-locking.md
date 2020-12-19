---
description: Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.
seo-description: Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.
seo-title: Verzoek vergrendelen
solution: Experience Manager
title: Verzoek vergrendelen
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Verzoek om vergrendeling{#request-locking}

Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.

Als attribute::RequestLock wordt geplaatst, moet een slotwaarde aan het verzoek worden toegevoegd, in vorm van `&xxxx`, met xxxx een hexadecimale waarde van vier cijfers is. Deze hexadecimale waarde wordt geproduceerd gebruikend een eenvoudig het hakken algoritme dat op het *modifiers* gedeelte van het verzoek wordt toegepast (na &#39;?&#39; die het URL-pad scheidt van de *modifiers*). Dit moet worden gedaan nadat het verzoek volledig http-encoded is, maar alvorens het (naar keuze) wordt verduisterd. Nadat de-obfuscating van het verzoek, zal de server het zelfde het hakken algoritme op het bepalingskoord (exclusief de laatste 5 karakters, die de slotwaarde bevatten) gebruiken. Als de gegenereerde sleutel niet overeenkomt met de vergrendeling, wordt het verzoek afgewezen.

>[!IMPORTANT]
>
>Als u deze functie inschakelt, moet u er rekening mee houden dat er bepaalde gebruiksbeperkingen zijn, waaronder:<br>- In de Dynamic Media-gebruikersinterface worden mogelijk niet de juiste gegevens voor het veld **[!UICONTROL Last Published]** weergegeven. Dit heeft echter geen invloed op de uitgeverij.<br>- HLS-videostreaming werkt momenteel niet wanneer **[!UICONTROL Request obfuscation]** en  **[!UICONTROL Request locking]** wordt ingeschakeld.<br>- Momenteel werken sommige Dynamic Media Viewers niet wanneer  **[!UICONTROL Request obfuscation]** en  **[!UICONTROL Request locking]** worden ingeschakeld.

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

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
