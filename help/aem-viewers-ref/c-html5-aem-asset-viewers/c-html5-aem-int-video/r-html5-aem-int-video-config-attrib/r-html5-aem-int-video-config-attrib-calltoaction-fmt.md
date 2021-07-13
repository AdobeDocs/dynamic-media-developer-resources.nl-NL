---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Developer,User
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---

# CallToAction.fmt{#calltoaction-fmt}

Configuration attribute for Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. </p> <p>Als de opgegeven indeling eindigt met "<span class="codeph"> -alpha</span>", geeft de component de afbeeldingen weer als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component de afbeeldingen als dekkend. </p> </td> 
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
