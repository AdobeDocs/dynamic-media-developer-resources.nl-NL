---
description: Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt.
seo-description: Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`breedte`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Wanneer deze optie is ingesteld op <span class="codeph"> 0 </span>, laadt de component geen nieuwe afbeeldingen tijdens het vergroten/verkleinen en verandert de afbeeldingsresolutie in de vervolgweergave niet. </p> <p>Wanneer u de waarde <span class="codeph"> 1 instelt, </span> kunt u een of meer breedteonderbrekingspunten opgeven voor de afbeelding die in de hoofdweergave wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breekpunt, <span class="varname"> breedte </span>[; <span class="varname"> breedte </span>] </span> </p> </td> 
   <td colname="col2"> <p>Breedteonderbrekingspunten voor de afbeelding die in de hoofdweergave is geladen. De component zal altijd het best passend formaat voor de aanvankelijke lading gebruiken. Nadat het formaat is gewijzigd, wordt de afbeelding in de hoofdweergave altijd gedownload met de breedte die gelijk is aan het dichtstbijzijnde grotere onderbrekingspunt en op de client geschaald. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
