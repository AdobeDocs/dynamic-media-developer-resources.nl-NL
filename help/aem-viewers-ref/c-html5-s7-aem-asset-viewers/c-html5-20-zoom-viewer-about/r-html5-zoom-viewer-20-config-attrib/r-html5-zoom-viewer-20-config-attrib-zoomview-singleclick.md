---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van één klik of tik voor zoomacties. Instellen op <span class="codeph"> none </span> Hiermee schakelt u zoomen met één klik of tikken uit. Indien ingesteld op <span class="codeph"> zoomen </span> als u op de afbeelding klikt, wordt in één zoomstap ingezoomd; Met CTRL en klikken zoomt u één zoomstap uit. Instellen op <span class="codeph"> reset </span> zorgt ervoor dat een enkele klik op de afbeelding het zoomniveau terugzet naar het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige zoomfactor op of boven de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - op bureaubladcomputers; `none` op aanraakapparaten.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
