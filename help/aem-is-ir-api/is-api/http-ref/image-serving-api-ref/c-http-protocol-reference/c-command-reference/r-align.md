---
description: Afbeelding uitlijnen met weergave. Hiermee wordt de samengestelde afbeelding uitgelijnd (mogelijk na het schalen, als scl= ook is opgegeven) binnen de weergaverechthoek die wordt gedefinieerd door wid= en hei=.
seo-description: Afbeelding uitlijnen met weergave. Hiermee wordt de samengestelde afbeelding uitgelijnd (mogelijk na het schalen, als scl= ook is opgegeven) binnen de weergaverechthoek die wordt gedefinieerd door wid= en hei=.
seo-title: align
solution: Experience Manager
title: align
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# align{#align}

Afbeelding uitlijnen met weergave. Hiermee wordt de samengestelde afbeelding uitgelijnd (mogelijk na het schalen, als scl= ook is opgegeven) binnen de weergaverechthoek die wordt gedefinieerd door wid= en hei=.

` align= *``*, *`horizvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>horizontale uitlijning (reëel, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> omkeren  </span> </span> </p> </td> 
  <td class="stentry"> <p>verticale uitlijning (reëel, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Geef `align=-1,-1` op om de linkerbovenhoek van de samengestelde afbeelding uit te lijnen met de linkerbovenhoek van de weergave. Geef `align=1,1` op om de rechteronderkant van de afbeelding uit te lijnen met de rechteronderhoek van de weergave. Voor standaardafbeeldings- en miniatuuraanvragen wordt elk gedeelte van de weergave dat niet wordt gedekt door samengestelde afbeeldingsgegevens, gevuld met `bgc=`.

## Eigenschappen {#section-3fbec8206fc944eda4746d8be84f3b41}

Kenmerk weergeven. ( `align=` wordt ook gebruikt om de groepering tussen een watermerkbeeld en het samengestelde beeld te bepalen waarop het watermerk wordt toegepast.) Ongeacht de huidige laaginstelling. Wordt genegeerd wanneer slechts een van `wid=` en `hei=` is opgegeven en wanneer `fit=constrain` of `fit=stretch` is opgegeven.

## Standaard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, waarmee de afbeelding in het midden van de weergaverechthoek wordt geplaatst.

## Voorbeeld {#section-2c9447aa2e184fb8ab1a4370dc61d554}

Het volgende verzoek past `myImage` in een 200x200-pixelweergaverechthoek.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Als `myImage` precies vierkant is, vult het de volledige meningsrechthoek. Als `myImage` een staande hoogte-breedteverhouding heeft, wordt deze geschaald tot 200 pixels hoog en wordt deze horizontaal gecentreerd in de weergave. Als `myImage` een liggende hoogte-breedteverhouding heeft, wordt deze geschaald tot 200 pixels breed en uitgelijnd op de bovenrand van de weergave. In alle gevallen is de geretourneerde afbeelding precies 200 x 200 pixels groot. spaties die niet door de geschaalde `myImage` worden bestreken, worden gevuld met `attribute::BkgColor` (bgc= opgeven om de achtergrondkleur dynamisch te regelen).

## Zie ook {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Watermerken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
