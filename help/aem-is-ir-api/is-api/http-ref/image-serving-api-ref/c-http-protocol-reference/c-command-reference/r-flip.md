---
description: Laag omdraaien. Hiermee wordt de laag horizontaal, verticaal of beide gespiegeld na het toepassen van crop= en vóór rotate= en extend=.
seo-description: Laag omdraaien. Hiermee wordt de laag horizontaal, verticaal of beide gespiegeld na het toepassen van crop= en vóór rotate= en extend=.
seo-title: omdraaien
solution: Experience Manager
title: omdraaien
topic: Scene7 Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# spiegelen{#flip}

Laag omdraaien. Hiermee wordt de laag horizontaal, verticaal of beide gespiegeld na het toepassen van crop= en vóór rotate= en extend=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Laag horizontaal spiegelen (links-rechts). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> bedrieglijk  </span> </p> </td> 
  <td class="stentry"> <p>Laag verticaal spiegelen (omhoog-omlaag). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>Draai zowel horizontaal als verticaal om. </p> </td> 
 </tr> 
</table>

Kan ook op tekstlagen worden toegepast.

Sommige opdrachten, zoals `extend=`, worden impliciet toegepast op laag 0 in plaats van op de samengestelde laag wanneer `layer=comp` is geselecteerd. In dergelijke scenario&#39;s, zullen alle bevelen die automatisch aan laag 0 worden toegewezen vóór de bevelen worden toegepast die op `layer=comp` van toepassing zijn. Wanneer `layer=comp`, `extend=` wordt toegepast vóór `flip=`.

>[!NOTE]
>
>De gespiegelde laag wordt geplaatst op basis van het laaganker; verschillende spiegelwaarden resulteren in verschillende laagposities wanneer het anker zich niet in het midden van de laag bevindt.

## Eigenschappen {#section-294da2af7be746b5adfc35e29ee68217}

Laag, opdracht. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-502044f81a89492198d5f12a738459ea}

Geen.

## Zie ook {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
