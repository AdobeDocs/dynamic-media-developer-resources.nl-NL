---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specificeert het beeldformaat dat door de component voor het laden van beelden van de Server van het Beeld wordt gebruikt. De indeling is elke waarde die door de afbeeldingsserver en de clientbrowser wordt ondersteund. </p> <p>Als de afbeeldingsindeling eindigt met <span class="codeph"> -alpha</span>, rendert de component de afbeeldingen als transparante inhoud. Voor alle andere waarden voor de afbeeldingsindeling worden afbeeldingen in de component als dekkend behandeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
