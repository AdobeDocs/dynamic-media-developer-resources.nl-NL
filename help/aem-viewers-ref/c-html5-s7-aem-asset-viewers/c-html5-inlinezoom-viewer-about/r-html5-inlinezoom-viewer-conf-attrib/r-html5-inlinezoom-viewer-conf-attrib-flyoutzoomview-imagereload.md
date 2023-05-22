---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt. </p> <p>Instellen op <span class="codeph"> 0 </span>, laadt de component geen nieuwe afbeeldingen tijdens het vergroten of verkleinen en verandert de afbeeldingsresolutie in de vervolgweergave niet. </p> <p>Instellen op <span class="codeph"> 1 </span> Hiermee kunt u een of meer breedteonderbrekingspunten opgeven voor de afbeelding die in de hoofdweergave wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breekpunt, <span class="varname"> width </span>; <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p>Breedteonderbrekingspunten voor de afbeelding die in de hoofdweergave is geladen. </p> <p>De component gebruikt altijd de beste maatgrootte voor de eerste belasting. Nadat het formaat is gewijzigd, zorgt u ervoor dat de afbeelding in de hoofdweergave altijd wordt gedownload met de breedte die gelijk is aan het dichtstbijzijnde grotere onderbrekingspunt en op de client wordt geschaald. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
