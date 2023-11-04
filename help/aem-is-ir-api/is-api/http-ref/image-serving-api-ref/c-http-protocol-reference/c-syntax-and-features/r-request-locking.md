---
description: Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.
solution: Experience Manager
title: Verzoek vergrendelen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Verzoek vergrendelen{#request-locking}

Om de kans op het knoeien met verzoeken te verminderen, wordt een eenvoudige sluitingsfaciliteit verstrekt.

Als attribute::RequestLock wordt geplaatst, moet een slotwaarde aan het verzoek worden toegevoegd, in vorm van `&xxxx`, waarbij xxxx een hexadecimale waarde van vier cijfers is. Deze hexadecimale waarde wordt gegenereerd met behulp van een eenvoudig hash-algoritme dat wordt toegepast op het *modifiers* deel van het verzoek (na &#39;?&#39; waarmee het URL-pad wordt gescheiden van het *modifiers*). Dit moet worden gedaan nadat het verzoek volledig http-encoded is, maar alvorens het (naar keuze) wordt verduisterd. Na het ontduisteren van het verzoek, gebruikt de server het zelfde het hakken algoritme op het bepalingskoord (met uitzondering van de laatste 5 karakters, die de slotwaarde bevatten). Als de gegenereerde sleutel niet overeenkomt met de vergrendeling, wordt het verzoek afgewezen.

>[!IMPORTANT]
>
>Als u deze functie inschakelt, moet u er rekening mee houden dat er bepaalde gebruiksbeperkingen zijn, waaronder:<br>- De Dynamic Media-gebruikersinterface bevat mogelijk niet de juiste gegevens voor de **[!UICONTROL Last Published]** veld. Dit heeft echter geen invloed op de uitgeverij.<br>- HLS-videostreaming werkt momenteel niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** zijn ingeschakeld.<br>- Sommige Dynamic Media Viewers werken momenteel niet wanneer **[!UICONTROL Request obfuscation]** en **[!UICONTROL Request locking]** zijn ingeschakeld.

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

[HTTP-codering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Obfuscatie aanvragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [kenmerk::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
