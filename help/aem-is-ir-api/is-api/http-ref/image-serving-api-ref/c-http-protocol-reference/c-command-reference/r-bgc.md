---
description: Achtergrondkleur weergeven. Hiermee geeft u de achtergrondkleur voor de samengestelde afbeelding (weergaveafbeelding) op.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# bgc{#bgc}

Achtergrondkleur weergeven. Hiermee geeft u de achtergrondkleur voor de samengestelde afbeelding (weergaveafbeelding) op.

`bgc= *`kleur`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kleur</span></span> </p> </td> 
  <td class="stentry"> <p>Waarde van grijs-, RGB- of CMYK-kleur. </p></td> 
 </tr> 
</table>

Hiermee geeft u een dekkende vulkleur op die moet worden gebruikt voor de weergaveachtergrond. Alleen zichtbaar als de samengestelde afbeelding transparante gebieden heeft of als de samengestelde afbeelding een andere hoogte-breedteverhouding heeft dan de weergaverechthoek. Genegeerd als `fmt=tif-alpha` of `fmt=png-alpha`, of `req=mask`.

>[!NOTE]
>
>Het achtervoegsel &#39;s&#39; voor kleuren wordt genegeerd door `bgc=`. Kleurwaarden opgegeven met `bgc=` worden altijd gekoppeld aan de desbetreffende uitvoerkleurruimte.

## Eigenschappen {#section-b729b50b1ea7433b82ba34ecd61839cd}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling. Genegeerd als `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, of `fmt=swf-alpha`.

Elke alpha-waarde die met kleur is opgegeven, wordt genegeerd.

*`color`* wordt verondersteld tot de uitvoerkleurruimte te behoren (zoals opgegeven met `icc=`) en moet hetzelfde pixeltype hebben als de uitvoerafbeelding. Als de pixeltypen niet overeenkomen, *`color`* wordt geconverteerd met behulp van naïeve conversie.

## Standaard {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Voorbeeld {#section-7bcdfbc0e1274e86a69d39186b090789}

Geef een expliciete achtergrondkleur op voor een miniatuuraanvraag:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Zie ook {#section-1e55f9f98f1847918a1725836a27cfaa}

[kleur](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [kenmerk::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Kleurbeheer](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
