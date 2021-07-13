---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van één klik of tik voor zoomacties. Als u instelt op <span class="codeph"> Geen </span>, wordt zoomen met één klik/tikken uitgeschakeld. Als dit is ingesteld op <span class="codeph"> om </span> te draaien en op de afbeelding te klikken, zoomt u in één zoomstap. Met CTRL en klikken zoomt u één zoomstap uit. Als u <span class="codeph"> reset </span> instelt, wordt met één klik op de afbeelding het zoomen opnieuw ingesteld op het eerste centrifugeniveau. Voor <span class="codeph"> zoomReset </span> wordt opnieuw ingesteld als de huidige zoomfactor op of buiten de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` op desktopcomputers;  `none` op aanraakapparaten.

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
