---
title: FlyoutZoomView.fmt
description: Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, worden afbeeldingen door de component als transparante inhoud gerenderd. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. </p> <p>De component heeft standaard een witte achtergrond. Om het transparant te maken, stelt u daarom de <span class="codeph"> background-color</span> CSS-eigenschap naar <span class="codeph"> transparant</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
