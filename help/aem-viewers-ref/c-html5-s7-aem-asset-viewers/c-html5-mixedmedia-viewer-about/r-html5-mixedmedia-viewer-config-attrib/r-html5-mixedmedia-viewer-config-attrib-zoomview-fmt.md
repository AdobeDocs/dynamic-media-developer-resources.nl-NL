---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: f13faa03-3b69-4cae-aaf5-55edd4aa5c84
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 1%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om dit transparant te maken, stelt u de CSS-eigenschap <span class="codeph"> background-color</span> daarom in op <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
