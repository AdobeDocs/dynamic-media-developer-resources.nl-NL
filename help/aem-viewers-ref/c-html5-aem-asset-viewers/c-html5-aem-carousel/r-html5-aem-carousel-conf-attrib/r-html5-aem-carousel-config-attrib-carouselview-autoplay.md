---
description: Configuration attribute for Carousel Viewer.
seo-description: Configuration attribute for Carousel Viewer.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---


# CarouselView.autoplay{#carouselview-autoplay}

Configuration attribute for Carousel Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duur][,richting]</span> </p> </td> 
   <td colname="col2"> <p> Geeft aan of de banner in de carrousel moet worden weergegeven en de richting van de automatische lus. </p> <p>Stel in op <span class="codeph"> 0</span> voor auto-lus off. </p> <p>Stel <span class="codeph"> 1</span> in op auto-loop aan met overgangsduur in seconden die wordt bepaald door <span class="codeph"> duration</span>. </p> <p>De richting van de auto-lijn wordt gecontroleerd met <span class="codeph"> richting</span>. De <span class="codeph"> direction</span> heeft de waaier tussen <span class="codeph"> 1</span> van rechts naar links en <span class="codeph"> 0</span> van links naar rechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```

