---
title: OnFailObj
description: Foutafhandeling objectselectie. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht obj= mislukt omdat het opgegeven pad niet kan worden vergeleken in de hiërarchie van het vignetobject.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---

# OnFailObj{#onfailobj}

Foutafhandeling objectselectie. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht obj= mislukt omdat het opgegeven pad niet kan worden vergeleken in de hiërarchie van het vignetobject.

## Eigenschappen {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Overnemen van <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>De vorige selectie behouden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Selectie opheffen; pogingen om een materiaal toe te passen of objecten tonen/verbergen worden genegeerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Retourneer een fout. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selecteer de standaardgroep (de eerste groep in de vignethiërarchie die renderbare objecten bevat). </p> </td> 
 </tr> 
</table>

## Standaard {#section-a5a95a2b4a204a4eae350e5b544d1513}

Overgenomen van `default::OnFailObj` indien niet gedefinieerd.

## Zie ook {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [kenmerk::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
