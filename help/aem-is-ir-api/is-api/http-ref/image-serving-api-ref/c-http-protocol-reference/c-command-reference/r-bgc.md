---
description: Achtergrondkleur weergeven. Hiermee geeft u de achtergrondkleur voor de samengestelde afbeelding (weergaveafbeelding) op.
seo-description: Achtergrondkleur weergeven. Hiermee geeft u de achtergrondkleur voor de samengestelde afbeelding (weergaveafbeelding) op.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

Achtergrondkleur weergeven. Hiermee geeft u de achtergrondkleur voor de samengestelde afbeelding (weergaveafbeelding) op.

`bgc= *`kleur`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kleur</span></span> </p> </td> 
  <td class="stentry"> <p>Grijswaarde, RGB- of CMYK-kleurwaarde. </p></td> 
 </tr> 
</table>

Hiermee geeft u een dekkende vulkleur op die moet worden gebruikt voor de weergaveachtergrond. Alleen zichtbaar als de samengestelde afbeelding transparante gebieden heeft of als de samengestelde afbeelding een andere hoogte-breedteverhouding heeft dan de weergaverechthoek. Genegeerd als `fmt=tif-alpha` of `fmt=png-alpha`, of `req=mask`.

>[!NOTE]
>
>Het kleurachtervoegsel &#39;s&#39; wordt genegeerd `bgc=`. De kleurwaarden die met worden opgegeven, `bgc=` worden altijd gekoppeld aan de desbetreffende uitvoerkleurruimte.

## Eigenschappen {#section-b729b50b1ea7433b82ba34ecd61839cd}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling. Genegeerd als `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, of `fmt=swf-alpha`.

Elke alpha-waarde die met kleur is opgegeven, wordt genegeerd.

*`color`* wordt aangenomen dat deze tot de uitvoerkleurruimte behoren (zoals opgegeven met `icc=`) en hetzelfde pixeltype hebben als de uitvoerafbeelding. Als de pixeltypen niet overeenkomen, *`color`* wordt deze omgezet met behulp van naïeve conversie.

## Standaard {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Voorbeeld {#section-7bcdfbc0e1274e86a69d39186b090789}

Geef een expliciete achtergrondkleur op voor een miniatuuraanvraag:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Zie ook {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
