---
description: Parameter die alle viewers gemeen hebben.
seo-description: Parameter die alle viewers gemeen hebben.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---


# contentUrl{#contenturl}

Parameter die alle viewers gemeen hebben.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u het basispad op naar aangepaste CSS-bestanden, ondertitelingsinhoud of navigatie-inhoud. </p> <p>Als het pad geen regelafstand <span class="filepath"> /</span> heeft, is dit relatief ten opzichte van de locatie van de HTML-pagina van de viewer. Als het pad een regelafstand <span class="filepath"> /</span> heeft, wordt een absoluut pad op dezelfde server opgegeven. </p> <p> Dit heeft geen invloed op het laden van het standaard-CSS-bestand wanneer u geen stijlopdracht opgeeft. </p> </td> 
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

