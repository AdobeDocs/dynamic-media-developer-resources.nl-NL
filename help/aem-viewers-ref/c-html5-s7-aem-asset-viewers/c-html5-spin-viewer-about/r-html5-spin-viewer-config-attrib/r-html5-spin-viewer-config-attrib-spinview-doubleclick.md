---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken om handelingen te draaien. Als u instelt op <span class="codeph"> Geen </span>, wordt dubbelklikken/tikken uitgeschakeld. Indien ingesteld op <span class="codeph"> zoomen </span> en klikken op de afbeelding draait in één centrifugestap; Met CTRL en klikken draait u één centrifuge uit. Als u de instelling <span class="codeph"> reset </span> instelt, wordt de centrifugeerknop opnieuw ingesteld op het eerste centrifugeniveau. Voor <span class="codeph"> zoomReset </span> wordt opnieuw ingesteld als de huidige centrifugefactor op of voorbij de gespecificeerde grens is, anders wordt het centrifugeren toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`reset` op desktopcomputers;  `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
