---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u het aantal seconden dat de tekst van het uiteinde wordt weergegeven voordat deze wordt verborgen. Wanneer ingesteld op <span class="codeph"> -1</span>, wordt het bericht altijd weergegeven, zelfs als de gebruiker de flyout activeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aantal</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u op hoe vaak de tekst wordt weergegeven wanneer u nieuwe afbeeldingen in de set weergeeft. De waarde <span class="codeph"> -1</span> betekent dat de tekst altijd wordt weergegeven wanneer een afbeelding in de set wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vervagen</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de duur op van een fade-animatie die optreedt wanneer de tekst verschijnt of verdwijnt. De waarde <span class="codeph"> 0</span> betekent geen vervagingsovergang. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
