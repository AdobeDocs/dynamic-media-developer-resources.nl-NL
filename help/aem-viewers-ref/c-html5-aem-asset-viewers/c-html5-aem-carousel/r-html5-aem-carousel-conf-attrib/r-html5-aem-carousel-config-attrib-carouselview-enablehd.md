---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie in-, beperken of uitschakelen voor apparaten waarbij <span class="codeph"> devicePixelRatio</span> groter is dan <span class="codeph"> 1</span>, dat wil zeggen apparaten met een hoge dichtheid, zoals iPhone4 en soortgelijke apparaten. </p> <p>Als actief dan beperkt de component de grootte van het de beeldverzoek van IS alsof het apparaat slechts een pixelverhouding van <span class="codeph"> 1 </span> had en die manier de bandbreedte vermindert. </p> <p>Zie het onderstaande voorbeeld. </p> </td> 
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
