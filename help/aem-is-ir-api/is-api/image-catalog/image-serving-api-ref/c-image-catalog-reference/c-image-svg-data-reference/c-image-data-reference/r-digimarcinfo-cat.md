---
description: Digimarc-afbeeldingsgegevens. Hiermee schakelt u Digimarc-insluiting in en geeft u het type watermerk en de bijbehorende afbeeldingsspecifieke gegevens op.
seo-description: Digimarc-afbeeldingsgegevens. Hiermee schakelt u Digimarc-insluiting in en geeft u het type watermerk en de bijbehorende afbeeldingsspecifieke gegevens op.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 7%

---


# DigimarcInfo{#digimarcinfo}

Digimarc-afbeeldingsgegevens. Hiermee schakelt u Digimarc-insluiting in en geeft u het type watermerk en de bijbehorende afbeeldingsspecifieke gegevens op.

## Eigenschappen {#section-62af219e8bac422b8541841221c9ce4f}

Vier gehele getallen, gescheiden door komma&#39;s.

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*`Met `*` type schakelt u Digimarc-insluiting in en geeft u het type watermerk op:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Type watermerk</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Basis. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Afbeelding-id. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transactie-id. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Copyrightjaren. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`Hiermee `*` markeert u een bitveld met drie waarden. Stel bit 0 in om te verwijzen naar inhoud die is beveiligd tegen kopiëren, bit 1 om beperkte inhoud aan te geven en bit 2 om de inhoud van volwassenen aan te geven:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> vlaggen</span> </span> </p> </th> 
   <th class="entry"> <p><b>Beschrijving</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Met kopiëren beveiligd. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Beperkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Met kopiëren beveiligd, beperkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Natuurlijke inhoud. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Met kopiëren beveiligde inhoud voor volwassenen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Beperkte inhoud voor volwassenen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Met kopiëren beveiligde, beperkte, volwassen inhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

De interpretatie van `*`val1`*` en `*`val2`*` hangt af van `*`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Afbeelding-id. </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Transactie-id. </p> </td> 
   <td> <p>Niet gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Eerste copyrightjaar. </p> </td> 
   <td> <p>Tweede copyrightjaar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Standaard {#section-4bb97e5f79074be89cc691e73449eb43}

Geërfd van kenmerk::DigimarcInfo als het veld niet aanwezig is of leeg is.

## Voorbeelden {#section-0f14727a0a2a408781c9df71fed7f42d}

Met &quot;0,0,0,0&quot; schakelt u Digimarc-watermerken uit voor deze afbeelding.

Met &quot;1,5,0,0&quot; wordt een elementair watermerk opgegeven met de markering voor door volwassenen en kopieën beveiligde inhoud ingesteld.

&quot;2,0,4567,0&quot; geeft een watermerk met een afbeeldings-id aan.

&quot;3,2,56483,0&quot; geeft een watermerk aan met een transactie-id en de vlag voor beperkte inhoud ingesteld.

&quot;4,0,1998,2001&quot; verwijst naar een watermerk met copyrightjaren.

## Zie ook {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[kenmerk::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [kenmerk::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
