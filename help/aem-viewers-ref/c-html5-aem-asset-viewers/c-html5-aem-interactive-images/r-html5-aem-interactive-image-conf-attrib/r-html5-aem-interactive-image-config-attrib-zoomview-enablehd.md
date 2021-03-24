---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie in-, beperken of uitschakelen voor apparaten waarbij <span class="codeph"> devicePixelRatio</span> groter is dan <span class="codeph"> 1</span>. Heeft invloed op apparaten met een hoge dichtheid, zoals iPhone4 en soortgelijke apparaten. Indien actief, beperkt de component de grootte van het de beeldverzoek van IS alsof het apparaat een pixelverhouding van <span class="codeph"> 1 </span> had, daardoor verminderend de bandbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> getal</span></span> </p> </td> 
   <td colname="col2"> <p> Als u de limietinstelling gebruikt, schakelt de component hoge pixeldichtheid alleen in tot de opgegeven limiet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
