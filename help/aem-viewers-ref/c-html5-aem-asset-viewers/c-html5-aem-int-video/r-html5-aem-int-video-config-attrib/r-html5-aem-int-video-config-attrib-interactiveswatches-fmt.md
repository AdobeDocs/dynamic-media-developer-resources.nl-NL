---
title: InteractiveSwatches.fmt
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Configuration attribute for Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. </p> <p>Als de opgegeven notatie eindigt met "<span class="codeph"> -alpha</span>", rendert de component de afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component de afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om het transparant te maken, stelt u daarom de <span class="codeph"> background-color</span> CSS-eigenschap naar <span class="codeph"> transparant</span>. </p> </td> 
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
