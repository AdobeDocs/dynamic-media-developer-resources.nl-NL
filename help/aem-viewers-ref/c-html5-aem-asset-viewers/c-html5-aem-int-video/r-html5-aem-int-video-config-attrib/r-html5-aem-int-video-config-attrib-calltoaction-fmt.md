---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: CallToAction.fmt
solution: Experience Manager
title: CallToAction.fmt
topic: Dynamic media
uuid: c85160e2-431f-42af-a468-c754bfe86ecd
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.fmt{#calltoaction-fmt}

Configuration attribute for Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. </p> <p>Als de opgegeven indeling eindigt met "<span class="codeph"> -alpha</span>", rendert de component de afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component de afbeeldingen als dekkend. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```

