---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Instellen op <span class="codeph"> 1</span> om het vooraf laden van de ingezoomde afbeelding mogelijk te maken. </p> <p>Instellen op <span class="codeph"> 0</span> om de zoomafbeelding indien nodig stapsgewijs te laden. </p> <p> <p>Als u deze optie inschakelt, kan dit resulteren in een aanzienlijk hoger bandbreedtegebruik omdat de ingezoomde afbeelding in zijn geheel moet worden geladen, zelfs als de gebruiker geen zoomactie uitvoert. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
