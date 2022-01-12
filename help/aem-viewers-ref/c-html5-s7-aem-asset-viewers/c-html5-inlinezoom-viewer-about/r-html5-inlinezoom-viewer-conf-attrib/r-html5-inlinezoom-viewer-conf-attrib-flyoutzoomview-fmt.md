---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld moet worden gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, worden afbeeldingen door de component als transparante inhoud gerenderd. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. </p> <p>De component heeft standaard een witte achtergrond. Om het transparant te maken, stelt u daarom de <span class="codeph"> background-color</span> CSS-eigenschap naar <span class="codeph"> transparant</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
