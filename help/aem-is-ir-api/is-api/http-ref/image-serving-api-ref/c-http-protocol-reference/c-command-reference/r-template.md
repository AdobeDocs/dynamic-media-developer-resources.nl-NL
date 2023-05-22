---
description: Samenstellingsjabloon. Hiermee kunt u een samenstellende sjabloon opgeven die zich in een andere catalogus dan de hoofdcatalogus bevindt.
solution: Experience Manager
title: template
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# template{#template}

Samenstellingsjabloon. Hiermee kunt u een samenstellende sjabloon opgeven in een andere catalogus dan de hoofdcatalogus.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>Sjabloon. </p></td> 
 </tr> 
</table>

*`template`* moet een item uit de afbeeldingscatalogus zijn in de sjabloonhoofdtekst in `catalog::Modifier`.

Wanneer `template=` is aanwezig, wordt het voorwerp dat in de verzoekweg wordt gespecificeerd niet toegepast als bron voor laag 0. Er kan echter naar worden verwezen als een `src=` of `mask=` overal in het malplaatje door de vooraf bepaalde wegvariabele te gebruiken `$object$` als `src=` waarde. `catalog::Modifier` van het object dat is opgegeven in het aanvraagpad, wordt alleen toegepast als `$object$` in de sjabloon, terwijl `catalog::PostModifier` wordt altijd toegepast.

Laag 0 wordt bepaald in het malplaatjelichaam en kan een beeld, stevige kleur, tekst, of genestelde of ingebedde verzoeklaag zijn.

`catalog:PostModifier` van *`object`* wordt genegeerd wanneer *`object`* wordt gebruikt met `template=`.

## Standaard {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Geen.

## Eigenschappen {#section-daf3afb1d09c45a6a394468d0874c439}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling.

## Voorbeeld {#section-9a4f260ed43342b186b0fe855f34bca6}

Zie de voorbeelden in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Vooraf gedefinieerde padvariabele](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
