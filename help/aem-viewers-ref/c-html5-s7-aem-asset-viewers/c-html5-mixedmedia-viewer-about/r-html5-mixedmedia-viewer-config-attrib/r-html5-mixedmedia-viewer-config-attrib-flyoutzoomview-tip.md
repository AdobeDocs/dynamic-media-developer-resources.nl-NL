---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Viewers,SDK/API,Mediasets mixen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u het aantal seconden dat de tekst van het uiteinde wordt weergegeven voordat deze wordt verborgen. Wanneer ingesteld op <span class="codeph"> -1</span>, wordt het bericht altijd weergegeven, zelfs als de gebruiker de flyout activeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u op hoe vaak de tekst wordt weergegeven wanneer u nieuwe afbeeldingen in de set weergeeft. De waarde <span class="codeph"> -1</span> betekent dat de tekst altijd wordt weergegeven wanneer een afbeelding in de set wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> vervagen</span></span> </p> </td> 
   <td colname="col2"> Hiermee geeft u de duur op van een fade-animatie die optreedt wanneer de tekst verschijnt of verdwijnt. De waarde <span class="codeph"> 0</span> geeft aan dat er geen vervagingsovergang is. </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
