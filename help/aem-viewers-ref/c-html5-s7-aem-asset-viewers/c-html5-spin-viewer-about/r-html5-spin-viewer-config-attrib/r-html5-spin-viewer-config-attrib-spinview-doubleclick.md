---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken om handelingen te draaien. Instellen op <span class="codeph"> none </span> Schakelt dubbelklikken/tikken om te draaien uit. Indien ingesteld op <span class="codeph"> zoomen </span>, door in één centrifugestap op de afbeelding te klikken; Met CTRL en klikken draait u één centrifuge uit. Instellen op <span class="codeph"> reset </span> zorgt ervoor dat met één klik op de afbeelding de centrifuge wordt teruggezet op het oorspronkelijke centrifugeniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige centrifugefactor gelijk is aan of groter is dan de opgegeven limiet, anders wordt de centrifuge toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`reset` op desktopcomputers; `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
