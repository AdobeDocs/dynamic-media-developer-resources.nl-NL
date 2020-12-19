---
description: Selecteer object op pixellocatie.
seo-description: Selecteer object op pixellocatie.
seo-title: sel
solution: Experience Manager
title: sel
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---


# sel{#sel}

Selecteer object op pixellocatie.

` sel= *``*, *``*[, *`xyniveau`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>Locatiecoördinaten kiezen in pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> niveau  </span> </p> </td> 
  <td class="stentry"> <p>Groepsniveau (int). </p> </td> 
 </tr> 
</table>

Selecteert de groep of het voorwerp bij de pixelcoördinaten die door *`x, y`* worden gespecificeerd en begint een nieuw MSS. Als er geen selecteerbaar object is op de keuzesocatie of als de keuzesocatie niet geldig is, wordt de actie uitgevoerd die wordt opgegeven door `attribute::OnFailSel`.

*`level`* Hiermee geeft u aan of u de buitenste groep wilt selecteren of een diepgaande lijn naar een geneste groep of object wilt doorlopen. Als *`level`* niet wordt gespecificeerd, wordt de buitenste groep geselecteerd. Stel de waarde in op 1 om één groepsniveau onder de buitenste groep te selecteren. Stel dit in op een groot getal (bijvoorbeeld 99) om het binnenste selecteerbare object of de binnenste groep te selecteren.

## Eigenschappen {#section-8f27e84d88734a62a5e398e0c9972bdc}

Selectieopdracht; MSS-scheidingsteken. De objectselectie is blijvend totdat een ander object is geselecteerd, met `obj=` of `sel=`.

*`x, y`* moet liggen tussen 0, 0 (linkerbovenhoek van de afbeelding) en  *`wid`*-1,  *`hei`*-1 (rechteronderhoek van de afbeelding), waarbij  *`wid`* en  *`hei`* is ingesteld op de grootte van de niet-geschaalde vignetweergave.

Indien opgegeven, moet *`level`* 0 of groter zijn.

## Standaard {#section-e13c705a3e76468894b4ec190ed8a893}

Geen voor *`x, y`*. *`level`* is standaard ingesteld op 0.

## Zie ook {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [kenmerk::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
