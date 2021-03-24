---
description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Mediasets mixen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. </p> <p>De component heeft standaard een witte achtergrond. Om de klasse volledig transparant te maken, stelt u de CSS-eigenschap <span class="codeph"> background-color</span> daarom in op <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
