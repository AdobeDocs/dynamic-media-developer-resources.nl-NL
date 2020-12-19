---
description: Standaardantwoordafbeelding. Hiermee geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt wanneer een afbeelding niet kan worden gevonden.
seo-description: Standaardantwoordafbeelding. Hiermee geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt wanneer een afbeelding niet kan worden gevonden.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---


# defaultImage{#defaultimage}

Standaardantwoordafbeelding. Hiermee geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt wanneer een afbeelding niet kan worden gevonden.

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsobject. </p> </td> 
 </tr> 
</table>

*`object`* Dit kan een item uit een catalogus (inclusief een sjabloon) of een eenvoudig pad naar een afbeeldingsbestand zijn. Dit is handig als u ontbrekende afbeeldingen wilt vervangen door standaardafbeeldingen. Deze waarde negeert de waarde van de corresponderende catalogus `attribute::DefaultImage`. Bij een lege waarde ( `defaultImage=`) wordt de standaardverwerking van afbeeldingen uitgeschakeld.

>[!NOTE]
>
>Het standaardafbeeldingsmechanisme is niet van toepassing op SVG-objecten. Er wordt een fout geretourneerd als het in de aanvraag opgegeven SVG-object niet kan worden gevonden.

Als `attribute::DefaultImageMode=0`, *`object`* het volledige originele verzoek vervangt, zelfs als slechts één beeld in een multi-beeldsamenstelling ontbreekt. De enige bevelen die van het originele verzoek worden behouden zijn: `wid=`, `hei=`, `fmt=`, `qlt=`.

Bij `attribute::DefaultImageMode=1` vervangt het object alleen de ontbrekende afbeelding van de laag. worden de kenmerken voor de ontbrekende laag toegepast en wordt de samenstelling verwerkt en geretourneerd zoals gewoonlijk.

## Eigenschappen {#section-d30923d8dc4042eba10989212dd70887}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling. Genegeerd als `req=` anders is dan `img` of `tmb`.

## Beperkingen {#section-30df31bc8cac41cd917f1e45196779c2}

Externe afbeeldingsbronnen vallen niet onder het standaardafbeeldingsmechanisme; er wordt een fout geretourneerd als een externe afbeeldingsbron niet geldig is.

Beeldserver wordt teruggezet naar `DefaultImageMode=0` wanneer aanvragen voor het renderen van geneste afbeeldingen of voor FXG-rendering mislukken.

## Standaard {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Zie ook {#section-745392143c3747a2955e1ae561f58e5f}

[kenmerk::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [kenmerk: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
