---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat de component voor het laden van beelden van de Server van het Beeld gebruikt. Als de opgegeven indeling eindigt met <span class="codeph"> -alpha</span>, worden afbeeldingen door de component als transparante inhoud gerenderd. Voor alle andere afbeeldingsindelingen behandelt de component afbeeldingen als dekkend. De component heeft standaard een witte achtergrond. Om het transparant te maken, stelt u daarom de <span class="codeph"> background-color</span> CSS-eigenschap naar <span class="codeph"> transparant</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optioneel.

## Standaard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Voorbeeld {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
