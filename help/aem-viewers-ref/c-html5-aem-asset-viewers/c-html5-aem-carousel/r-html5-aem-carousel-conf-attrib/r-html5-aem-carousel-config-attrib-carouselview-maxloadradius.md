---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`voorlader`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span>, laadt de component alle carrouselframes vooraf wanneer deze niet-actief zijn. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span> laadt de component alleen het frame dat momenteel zichtbaar is, het vorige en het volgende frame. </p> <p><span class="codeph"><span class="varname"> Met </span></span>voorladen bepaalt u hoeveel onzichtbare frames rondom het momenteel weergegeven frame worden voorgeladen wanneer het frame niet actief is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
