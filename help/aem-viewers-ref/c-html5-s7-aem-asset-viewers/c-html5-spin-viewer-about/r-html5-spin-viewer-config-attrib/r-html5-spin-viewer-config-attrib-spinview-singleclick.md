---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van één klik of tik voor zoomacties. Instellen op <span class="codeph"> none </span> Hiermee schakelt u zoomen met één klik of tikken uit. Indien ingesteld op <span class="codeph"> draaien </span> als u op de afbeelding klikt, wordt in één zoomstap ingezoomd; Met CTRL en klikken zoomt u één zoomstap uit. Instellen op <span class="codeph"> reset </span> zorgt dat met één klik op de afbeelding het zoomniveau wordt ingesteld op het eerste centrifugeniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige zoomfactor op of boven de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` op bureaubladcomputers; `none` op aanraakapparaten.

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
