---
description: Samenstellingsjabloon. Hiermee kunt u een samenstellende sjabloon opgeven die zich in een andere catalogus dan de hoofdcatalogus bevindt.
seo-description: Samenstellingsjabloon. Hiermee kunt u een samenstellende sjabloon opgeven die zich in een andere catalogus dan de hoofdcatalogus bevindt.
seo-title: template
solution: Experience Manager
title: template
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# template{#template}

Samenstellingsjabloon. Hiermee kunt u een samenstellende sjabloon opgeven die zich in een andere catalogus dan de hoofdcatalogus bevindt.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>Sjabloon. </p></td> 
 </tr> 
</table>

*`template`* moet een item in een afbeeldingscatalogus zijn met de hoofdtekst van de sjabloon in  `catalog::Modifier`.

Wanneer `template=` aanwezig is, zal het voorwerp in de verzoekweg wordt gespecificeerd niet als bron voor laag 0 worden toegepast, maar kan als `src=` of `mask=` overal in het malplaatje worden van verwijzingen voorzien door de vooraf bepaalde wegvariabele `$object$` als &lt;a4 te gebruiken/> waarde. `src=` `catalog::Modifier` van het object dat is opgegeven in het aanvraagpad, wordt alleen toegepast in verband met de vervanging van het object  `$object$` binnen de sjabloon, terwijl dit altijd  `catalog::PostModifier` wordt toegepast.

Laag 0 wordt bepaald in het malplaatjelichaam en kan een beeld, stevige kleur, tekst, of genestelde of ingebedde verzoeklaag zijn.

`catalog:PostModifier` van  *`object`* wordt genegeerd wanneer  *`object`* wordt gebruikt met  `template=`.

## Standaard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Geen.

## Eigenschappen {#section-daf3afb1d09c45a6a394468d0874c439}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling.

## Voorbeeld {#section-9a4f260ed43342b186b0fe855f34bca6}

Zie de voorbeelden in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [vooraf gedefinieerde padvariabele](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
