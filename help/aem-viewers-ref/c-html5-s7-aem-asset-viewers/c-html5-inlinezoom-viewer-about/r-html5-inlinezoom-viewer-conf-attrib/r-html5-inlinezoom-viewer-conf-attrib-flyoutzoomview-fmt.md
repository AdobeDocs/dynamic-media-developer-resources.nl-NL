---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld moet worden gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. </p> <p>De component heeft standaard een witte achtergrond. Daarom stelt u de CSS-eigenschap <span class="codeph"> background-color</span> in op <span class="codeph"> transparent</span> om deze volledig transparant te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
