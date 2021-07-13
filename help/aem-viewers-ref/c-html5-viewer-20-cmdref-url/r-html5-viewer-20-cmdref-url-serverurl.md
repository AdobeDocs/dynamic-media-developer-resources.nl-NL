---
description: Parameter die alle viewers gemeen hebben.
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# serverUrl{#serverurl}

Parameter die alle viewers gemeen hebben.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Relatieve of absolute afbeeldingsserver voor het hoofdpad. </p> <p> Hiermee geeft u een relatief of absoluut pad op naar de afbeeldingsserver, vanwaar de viewer afbeeldingen ophaalt. Als het pad geen regelafstand <span class="filepath"> /</span> heeft, is dit relatief ten opzichte van de locatie van de HTML-pagina van de viewer. Als het pad een regelafstand <span class="filepath"> /</span> heeft, wordt een absoluut pad op dezelfde server opgegeven. </p> <p> Gebruik alleen een absoluut pad als de module Delen via e-mail is ingeschakeld in de viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel. Niet nodig voor standaard SaaS-gebruik (software als service).

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Voorbeelden {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
