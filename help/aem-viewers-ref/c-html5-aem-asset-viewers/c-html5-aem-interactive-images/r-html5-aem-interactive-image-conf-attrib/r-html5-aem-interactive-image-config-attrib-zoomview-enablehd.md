---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie in-, beperken of uitschakelen voor apparaten waarbij de <span class="codeph"> PixelRatio</span> van het apparaat groter is dan <span class="codeph"> 1</span>. Heeft invloed op apparaten met een hoge dichtheid, zoals iPhone4 en soortgelijke apparaten. Indien actief, beperkt de component de grootte van het verzoek van het beeld IS alsof het apparaat een pixelverhouding van <span class="codeph"> 1</span>had, daardoor verminderend de bandbreedte. </p> </td> 
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
