---
title: OnFailSel
description: Foutafhandeling van selectie kiezen. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht sel= mislukt omdat de opgegeven pixellocatie zich niet binnen het maskergebied van een selecteerbaar object bevindt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# OnFailSel{#onfailsel}

Foutafhandeling van selectie kiezen. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de `sel=` de opdracht mislukt omdat de opgegeven pixellocatie zich niet binnen het maskergebied van een selecteerbaar object bevindt.

## Eigenschappen {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Overnemen van <span class="codeph"> default::OnFailSel </span>. </p> </td> 
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

## Standaard {#section-c25f458f9f8f4236963a95779529e664}

Overgenomen van `default::OnFailSel` indien niet gedefinieerd.

## Zie ook {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [kenmerk::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
