---
title: FlyoutZoomView.imagereload
description: Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Wanneer ingesteld op <span class="codeph"> 0 </span>, laadt de component geen nieuwe afbeeldingen tijdens het vergroten of verkleinen en verandert de afbeeldingsresolutie in de vervolgweergave niet. </p> <p>Wanneer ingesteld op <span class="codeph"> 1 </span> Hiermee kunt u een of meer breedteonderbrekingspunten opgeven voor de afbeelding die in de hoofdweergave wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breekpunt, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Breedteonderbrekingspunten voor de afbeelding die in de hoofdweergave is geladen. De component gebruikt altijd de best-passend grootte voor de aanvankelijke lading. Nadat het formaat is gewijzigd, zorgt u ervoor dat de afbeelding in de hoofdweergave altijd wordt gedownload met de breedte die gelijk is aan het dichtstbijzijnde grotere onderbrekingspunt en op de client wordt geschaald. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
