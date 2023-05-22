---
description: Standaardantwoordafbeelding. Hiermee geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt wanneer een afbeelding niet kan worden gevonden.
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# defaultImage{#defaultimage}

Standaardantwoordafbeelding. Hiermee geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt wanneer een afbeelding niet kan worden gevonden.

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsobject. </p> </td> 
 </tr> 
</table>

*`object`* Dit kan een item uit een catalogus (inclusief een sjabloon) of een eenvoudig pad naar een afbeeldingsbestand zijn. Dit is handig als u ontbrekende afbeeldingen wilt vervangen door standaardafbeeldingen. Deze waarde overschrijft de waarde van de overeenkomende catalogus `attribute::DefaultImage`. Een lege waarde ( `defaultImage=`) schakelt de standaardverwerking van afbeeldingen uit.

>[!NOTE]
>
>Het standaardafbeeldingsmechanisme is niet van toepassing op SVG-objecten. Er wordt een fout geretourneerd als het in de aanvraag opgegeven object SVG niet kan worden gevonden.

Indien `attribute::DefaultImageMode=0`, *`object`* vervangt het volledige oorspronkelijke verzoek, zelfs als slechts één afbeelding in een compositie met meerdere afbeeldingen ontbreekt. De enige bevelen die van het originele verzoek worden behouden zijn: `wid=`, `hei=`, `fmt=`, `qlt=`.

Indien `attribute::DefaultImageMode=1`, vervangt het object alleen de ontbrekende afbeelding van de laag. worden de kenmerken voor de ontbrekende laag toegepast en wordt de samenstelling verwerkt en geretourneerd zoals gewoonlijk.

## Eigenschappen {#section-d30923d8dc4042eba10989212dd70887}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling. Genegeerd als `req=` is anders dan `img` of `tmb`.

## Beperkingen {#section-30df31bc8cac41cd917f1e45196779c2}

Externe afbeeldingsbronnen vallen niet onder het standaardafbeeldingsmechanisme; er wordt een fout geretourneerd als een externe afbeeldingsbron niet geldig is.

Beeldserver wordt teruggezet naar `DefaultImageMode=0` als geneste aanvragen voor het renderen van afbeeldingen of FXG-rendering mislukken.

## Standaard {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Zie ook {#section-745392143c3747a2955e1ae561f58e5f}

[kenmerk:DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [kenmerk: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
