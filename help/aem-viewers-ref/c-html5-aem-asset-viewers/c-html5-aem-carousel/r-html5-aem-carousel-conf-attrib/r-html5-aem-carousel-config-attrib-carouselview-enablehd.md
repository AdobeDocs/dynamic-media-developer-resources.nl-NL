---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie in-, beperken of uitschakelen voor apparaten waarbij <span class="codeph"> devicePixelRatio</span> groter is dan <span class="codeph"> 1</span>, dat wil zeggen apparaten met high-density display zoals iPhone4 en soortgelijke apparaten. </p> <p>Als actief dan beperkt de component de grootte van het de beeldverzoek van IS alsof het apparaat slechts een pixelverhouding van <span class="codeph"> 1 </span> had en die manier de bandbreedte vermindert. </p> <p>Zie het onderstaande voorbeeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> getal</span></span> </p> </td> 
   <td colname="col2"> <p> Als u de instelling <span class="codeph"></span> gebruikt, schakelt de component hoge pixeldichtheid alleen in tot de opgegeven limiet. </p> <p>Zie het onderstaande voorbeeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
