---
title: contentUrl
description: Parameter die alle viewers gemeen hebben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# contentUrl{#contenturl}

Parameter die alle viewers gemeen hebben.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het basispad op naar aangepaste CSS-bestanden, ondertitelingsinhoud of navigatie-inhoud. </p> <p>Als het pad geen regelafstand heeft <span class="filepath"> /</span>, is deze relatief ten opzichte van de locatie van de HTML-pagina van de viewer. Als het pad een regelafstand heeft <span class="filepath"> /</span>, wordt een absoluut pad op dezelfde server opgegeven. </p> <p> Dit heeft geen invloed op het laden van het standaard-CSS-bestand wanneer u geen stijlopdracht opgeeft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Voorbeelden {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
