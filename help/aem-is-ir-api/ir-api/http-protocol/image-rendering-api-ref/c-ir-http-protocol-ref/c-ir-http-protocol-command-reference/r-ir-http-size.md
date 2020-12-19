---
description: Decal size. Hiermee geeft u de grootte van een decal-materiaal op.
seo-description: Decal size. Hiermee geeft u de grootte van een decal-materiaal op.
seo-title: size
solution: Experience Manager
title: size
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# size{#size}

Decal size. Hiermee geeft u de grootte van een decal-materiaal op.

` size= *`breedte,hoogte`*[ *`,dikte`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> breedte, hoogte  </span> </p> </td> 
  <td class="stentry"> <p>Grootte van het decimale object in coördinaateenheden van scènes (normaal, echt). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> dikte  </span> </p> </td> 
  <td class="stentry"> <p>De dikte van het decimale object in coördinaateenheden van de scène (normaal). </p> </td> 
 </tr> 
</table>

Als noch de breedte, noch de hoogte 0 is, wordt de afbeelding geschaald tot de exacte opgegeven afmetingen en blijft de hoogte-breedteverhouding van de afbeelding niet behouden. Als u een van beide waarden instelt op 0, blijft de hoogte-breedteverhouding van de afbeelding behouden.

Wanneer *`thickness`* is opgegeven, wordt een slagschaduw weergegeven als het vignetobject een geschikte lichtvector definieert. Stel *`thickness`* in op 0 om slagschaduwrendering uit te schakelen.

## Eigenschappen {#section-818e01e91fed4015951189c818ef28d8}

Materiaalkenmerk. uitsluitend gebruikt door deksels; genegeerd door alle andere materialen. `res=` wordt genegeerd als een breedte of hoogte groter is dan 0. Waarden mogen niet negatief zijn.

## Standaard {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` indien het decal-materiaal op een catalogusvermelding is gebaseerd; anders  `size=0,0,0`. De decimale grootte wordt berekend vanaf `res=` als *`wid`* en *`hei`* niet worden gespecificeerd of aan 0 worden geplaatst. Er wordt geen slagschaduw weergegeven als *`thickness`* niet is opgegeven of op 0 is ingesteld.

## Voorbeeld {#section-04fdc2b60b9e4071b672bf6a913738ad}

Een MSS voor een decal, dat op resolutie wordt geschaald die door 20 deg met de wijzers van de klok mee wordt geroteerd, en een dikte van 2,5 duim, voor een aangewezen slagschaduweffect heeft:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Zie ook {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Scènecoördinaten](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1),  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [kenmerk::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
