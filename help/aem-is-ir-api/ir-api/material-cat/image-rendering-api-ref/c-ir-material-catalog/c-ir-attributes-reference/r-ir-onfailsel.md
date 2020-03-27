---
description: Foutafhandeling van selectie kiezen. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht sel= mislukt omdat de opgegeven pixellocatie zich niet binnen het maskergebied van een selecteerbaar object bevindt.
seo-description: Foutafhandeling van selectie kiezen. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht sel= mislukt omdat de opgegeven pixellocatie zich niet binnen het maskergebied van een selecteerbaar object bevindt.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailSel{#onfailsel}

Foutafhandeling van selectie kiezen. Hiermee wordt de actie opgegeven die moet worden uitgevoerd als de opdracht sel= mislukt omdat de opgegeven pixellocatie zich niet binnen het maskergebied van een selecteerbaar object bevindt.

## Eigenschappen {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Overnemen van <span class="codeph"> standaard::OnFailSel </span>. </p> </td> 
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
