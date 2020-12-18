---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`breedte`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Vormt hoe de component nieuwe beelden voor de hoofd en vliegend mening tijdens resize haalt. </p> <p>Wanneer ingesteld op <span class="codeph"> 0 </span>, laadt de component geen nieuwe afbeeldingen tijdens het wijzigen van de grootte. de afbeeldingsresolutie in de vervolgweergave verandert niet. </p> <p>Als u instelt op <span class="codeph"> 1 </span>, kunt u een of meer breedteonderbrekingspunten opgeven voor de afbeelding die in de hoofdweergave wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breekpunt,  <span class="varname"> breedte  </span>[;  <span class="varname"> breedte  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> Breedteonderbrekingspunten voor de afbeelding die in de hoofdweergave is geladen. De component gebruikt altijd de beste maatgrootte voor de eerste belasting. Nadat het formaat is gewijzigd, zorgt het ervoor dat de afbeelding in de hoofdweergave altijd wordt gedownload met de breedte die gelijk is aan het dichtstbijzijnde grotere onderbrekingspunt en op de client wordt geschaald. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
