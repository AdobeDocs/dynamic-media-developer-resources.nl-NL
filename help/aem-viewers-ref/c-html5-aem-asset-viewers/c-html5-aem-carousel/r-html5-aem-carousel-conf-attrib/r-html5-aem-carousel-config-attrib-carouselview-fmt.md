---
description: CarouselView.fmt
solution: Experience Manager
title: CarouselView.fmt
topic: Dynamic media
uuid: deba25f3-f074-42db-b1d5-d4bf22e25773
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---


# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. </p> <p>Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. </p> <p>Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om dit transparant te maken, stelt u de CSS-eigenschap <span class="codeph"> background-color</span> daarom in op <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
