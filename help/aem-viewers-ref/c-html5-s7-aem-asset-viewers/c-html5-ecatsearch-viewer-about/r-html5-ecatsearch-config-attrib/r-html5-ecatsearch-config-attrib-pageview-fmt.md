---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
uuid: bbae406c-9169-4944-8e91-f2d7c8011520
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---


# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, rendert de component afbeeldingen als transparante inhoud. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om dit transparant te maken, stelt u de CSS-eigenschap <span class="codeph"> background-color</span> daarom in op <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optioneel.

## Standaard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Voorbeeld {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
