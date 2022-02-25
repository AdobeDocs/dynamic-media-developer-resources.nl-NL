---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7cb75d38-a577-4e06-b679-c4e00db5059a
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. Als de opgegeven indeling eindigt met "-alpha", rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Stel de CSS-eigenschap voor de achtergrondkleur daarom in op transparant om deze transparant te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-50bcd15223174bb79ce08b31ea03d682}

Optioneel.

## Standaard {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## Voorbeeld {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
