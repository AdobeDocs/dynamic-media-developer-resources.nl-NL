---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken voor zoomacties. Instellen op <span class="codeph"> none </span> Hiermee schakelt u dubbelklikken/tikken in of uit. Indien ingesteld op <span class="codeph"> zoomen </span> als u op de afbeelding klikt, wordt in één zoomstap ingezoomd; Met CTRL en klikken zoomt u één zoomstap uit. Instellen op <span class="codeph"> reset </span> zorgt ervoor dat een enkele klik op de afbeelding het zoomniveau terugzet naar het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige zoomfactor op of boven de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` op bureaubladcomputers; `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
