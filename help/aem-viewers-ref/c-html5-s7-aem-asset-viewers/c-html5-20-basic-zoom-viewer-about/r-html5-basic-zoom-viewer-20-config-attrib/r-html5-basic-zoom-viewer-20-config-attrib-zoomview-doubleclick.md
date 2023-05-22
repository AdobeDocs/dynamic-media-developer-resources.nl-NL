---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
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

## Eigenschappen {#section-50bcd15223174bb79ce08b31ea03d682}

Optioneel.

## Standaard {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` op bureaubladcomputers; `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
