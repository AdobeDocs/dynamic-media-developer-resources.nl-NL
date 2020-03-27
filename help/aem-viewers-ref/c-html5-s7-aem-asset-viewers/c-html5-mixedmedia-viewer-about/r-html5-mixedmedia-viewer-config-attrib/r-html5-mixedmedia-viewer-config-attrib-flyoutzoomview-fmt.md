---
description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
seo-description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. </p> <p>De component heeft standaard een witte achtergrond. Daarom, om het volledig transparant te maken, plaats het achtergrond-kleur <span class="codeph"> CSS bezit aan</span> transparant <span class="codeph"></span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
