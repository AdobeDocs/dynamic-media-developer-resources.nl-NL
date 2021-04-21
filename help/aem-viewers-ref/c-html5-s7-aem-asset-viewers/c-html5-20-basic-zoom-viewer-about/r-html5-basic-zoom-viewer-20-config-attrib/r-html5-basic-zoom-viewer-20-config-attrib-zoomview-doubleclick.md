---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken voor zoomacties. Als u instelt op <span class="codeph"> Geen </span>, wordt dubbelklikken/tikken uitgeschakeld. Indien ingesteld op <span class="codeph"> zoomen </span> klikken op de afbeelding, zoomt u in één zoomstap. Met CTRL en klikken zoomt u één zoomstap uit. Als u <span class="codeph"> reset </span> instelt, wordt met één klik op de afbeelding de zoomwaarde opnieuw ingesteld op het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span> wordt opnieuw ingesteld als de huidige zoomfactor op of buiten de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-50bcd15223174bb79ce08b31ea03d682}

Optioneel.

## Standaard {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` op desktopcomputers;  `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
