---
title: CarouselView.autoplay
description: Configuration attribute for Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# CarouselView.autoplay{#carouselview-autoplay}

Configuration attribute for Carousel Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duur][,richting]</span> </p> </td> 
   <td colname="col2"> <p> Geeft aan of de banner in de carrousel moet worden weergegeven en de richting van de automatische lus. </p> <p>Instellen op <span class="codeph"> 0</span> voor auto-lus uit. </p> <p>Set <span class="codeph"> 1</span> aan auto-lijn aan met overgangsduur in seconden die door wordt gecontroleerd <span class="codeph"> duur</span>. </p> <p>De richting van de automatische lus wordt geregeld met <span class="codeph"> richting</span>. De <span class="codeph"> richting</span> heeft het bereik tussen <span class="codeph"> 1</span> van rechts naar links en <span class="codeph"> 0</span> van links naar rechts. </p> </td> 
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
