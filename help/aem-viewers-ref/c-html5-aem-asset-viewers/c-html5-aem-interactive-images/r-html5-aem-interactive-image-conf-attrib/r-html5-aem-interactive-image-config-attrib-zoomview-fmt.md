---
description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
seo-description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: 73a2196f-0ece-497a-9a12-376dafbbae56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.fmt{#zoomview-fmt}

Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Daarom stelt u de CSS-eigenschap voor de <span class="codeph"> achtergrondkleur</span> in op <span class="codeph"> transparant</span>om deze transparant te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
