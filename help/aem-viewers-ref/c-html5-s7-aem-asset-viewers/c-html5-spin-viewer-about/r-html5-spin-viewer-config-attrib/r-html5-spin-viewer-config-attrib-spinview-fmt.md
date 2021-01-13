---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
topic: Dynamic media
uuid: 6004d8ab-7dc7-451d-b0e2-4f6d308203d1
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---


# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om dit transparant te maken, stelt u de CSS-eigenschap <span class="codeph"> background-color</span> daarom in op <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
