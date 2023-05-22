---
description: Afbeelding uitlijnen met weergave. Hiermee wordt de samengestelde afbeelding uitgelijnd (mogelijk na het schalen, als scl= ook is opgegeven) binnen de weergaverechthoek die wordt gedefinieerd door wid= en hei=.
solution: Experience Manager
title: align
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# align{#align}

Afbeelding uitlijnen met weergave. Hiermee wordt de samengestelde afbeelding uitgelijnd (mogelijk na het schalen, als scl= ook is opgegeven) binnen de weergaverechthoek die wordt gedefinieerd door wid= en hei=.

` align= *`horiz`*, *`omkeren`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>horizontale uitlijning (reëel, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> omkeren </span> </span> </p> </td> 
  <td class="stentry"> <p>verticale uitlijning (reëel, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Opgeven `align=-1,-1` als u de linkerbovenhoek van de samengestelde afbeelding wilt uitlijnen met de linkerbovenhoek van de weergave, geeft u `align=1,1` Als u de onderkant, rechts van de afbeelding, wilt uitlijnen met de rechteronderkant van de weergave. Voor standaardverzoeken om afbeeldingen en miniaturen wordt elk gedeelte van de weergave dat niet wordt gedekt door samengestelde afbeeldingsgegevens, gevuld met `bgc=`.

## Eigenschappen {#section-3fbec8206fc944eda4746d8be84f3b41}

Kenmerk weergeven. ( `align=` wordt ook gebruikt om de uitlijning te definiëren tussen een watermerkafbeelding en de samengestelde afbeelding waarop het watermerk wordt toegepast.) Ongeacht de huidige laaginstelling. Genegeerd als slechts één van `wid=` en `hei=` wordt opgegeven en wanneer `fit=constrain` of `fit=stretch`.

## Standaard {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, waarmee de afbeelding in het midden van de weergaverechthoek wordt geplaatst.

## Voorbeeld {#section-2c9447aa2e184fb8ab1a4370dc61d554}

De volgende aanvraag is geschikt `myImage` in een weergaverechthoek van 200 x 200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Indien `myImage` is precies vierkant, vult het de volledige meningsrechthoek. Indien `myImage` heeft een staande hoogte-breedteverhouding, wordt het geschaald tot 200 pixels hoog en wordt horizontaal gecentreerd in de weergave. Indien `myImage` heeft een liggende hoogte-breedteverhouding, wordt deze geschaald tot 200 pixels breed en wordt uitgelijnd op de bovenrand van de weergave. In alle gevallen is de geretourneerde afbeelding precies 200 x 200 pixels groot. elke ruimte die niet door de geschaalde `myImage` is gevuld met `attribute::BkgColor` (specificeer bgc= om de achtergrondkleur dynamisch te controleren).

## Zie ook {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Watermerken](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
