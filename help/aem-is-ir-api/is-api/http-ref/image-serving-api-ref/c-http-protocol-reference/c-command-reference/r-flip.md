---
title: omdraaien
description: Laag omdraaien. Hiermee wordt de laag horizontaal, verticaal of beide gespiegeld na het toepassen van crop= en vóór rotate= en extend=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# omdraaien{#flip}

Laag omdraaien. Hiermee wordt de laag horizontaal, verticaal of beide gespiegeld na het toepassen van crop= en vóór rotate= en extend=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Draai de laag horizontaal om (links-rechts). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> bedrieglijk </span> </p> </td> 
  <td class="stentry"> <p>Draai de laag verticaal (omhoog-omlaag). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Draai zowel horizontaal als verticaal om. </p> </td> 
 </tr> 
</table>

Het kan ook op tekstlagen worden toegepast.

Sommige opdrachten, waaronder `extend=`wordt impliciet toegepast op laag 0 in plaats van op de samengestelde laag wanneer `layer=comp` is geselecteerd. In dergelijke scenario&#39;s, worden alle bevelen die automatisch aan laag 0 worden toegewezen toegepast vóór de bevelen die van toepassing zijn op `layer=comp`. Wanneer `layer=comp`, `extend=` wordt toegepast vóór `flip=`.

>[!NOTE]
>
>De gespiegelde laag wordt gepositioneerd op basis van het laaganker. Verschil `flip=` resulteren in verschillende laagposities wanneer het anker zich niet in het midden van de laag bevindt.

## Eigenschappen {#section-294da2af7be746b5adfc35e29ee68217}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-502044f81a89492198d5f12a738459ea}

Geen.

## Zie ook {#section-47f6484deccd420983df15ec163b4a83}

[roteren=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
