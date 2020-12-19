---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`breedte`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt. </p> <p>Stel in op <span class="codeph"> 0 </span>, de component laadt geen nieuwe afbeeldingen tijdens het vergroten/verkleinen en de afbeeldingsresolutie in de vervolgweergave verandert niet. </p> <p>Met de instelling <span class="codeph"> 1 </span> kunt u een of meer breedteonderbrekingspunten opgeven voor de afbeelding die in de hoofdweergave is geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breekpunt,  <span class="varname"> breedte  </span>;  <span class="varname"> width  </span> </span> </p> </td> 
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
