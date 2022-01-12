---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duur`*[, *`aantal`*][, *`vervagen`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u het aantal seconden dat de tekst van het uiteinde wordt weergegeven voordat deze wordt verborgen. Wanneer ingesteld op <span class="codeph"> -1</span>wordt het bericht altijd weergegeven, zelfs als de gebruiker de vervolgkeuzelijst activeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aantal</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u op hoe vaak de tekst wordt weergegeven wanneer u nieuwe afbeeldingen in de set weergeeft. Een waarde van <span class="codeph"> -1</span> betekent dat de tekst altijd wordt weergegeven wanneer een afbeelding in de set wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vervagen</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de duur op van een fade-animatie die optreedt wanneer de tekst verschijnt of verdwijnt. Een waarde van <span class="codeph"> 0</span> betekent geen vervagingsovergang. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
