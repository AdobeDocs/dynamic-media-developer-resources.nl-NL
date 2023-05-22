---
title: config
description: Parameter die alle viewers gemeen hebben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# config{#config}

Parameter die alle viewers gemeen hebben.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Catalogus/id voor de viewerconfiguratie. </p> <p> Hiermee wordt een item in een afbeeldingscatalogus opgegeven dat de configuratieeigenschappen van de viewer bevat in <span class="codeph"> catalogus::UserData </span>. Wanneer deze opdracht aanwezig is, verzendt de viewer een <span class="codeph"> req=userdata </span> opdracht for <span class="codeph"> configId </span> naar de server en extraheert eigenschappen uit het antwoord. De eigenschappen worden gebruikt om de viewer te initialiseren. Als de URL-tekenreeks dezelfde eigenschappen opgeeft, worden de waarden van <span class="codeph"> catalogus::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle vieweropdrachten die u kunt opgeven in `catalog::UserData` verwachten `asset`, `serverUrl`, `contentUrl`, `searchServerUrl`, en `config` zelf.

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

Geen.

## Voorbeeld 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Een afbeeldingscatalogus met de naam 2020 bevat het item `preset-oct`. De `catalog::UserData` in het veld van dit item in de catalogus staan de volgende gegevens:

```
style=customStyle.css
```

Laad de viewer met de volgende opdracht:

```
config=2020/preset-oct
```

Dit voorbeeld is gelijk aan de volgende opdracht die expliciet in de URL is opgegeven:

```
style=customStyle.css
```

## Voorbeeld 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Een afbeeldingscatalogus met de naam 2019 bevat het item `spin-oct`. De `catalog::UserData` in het veld van dit item in de catalogus staan de volgende gegevens:

```
zoomStep=3 
maxZoom=200
```

Laad de viewer met de volgende opdracht:

```
config=2019/spin-oct
```

Dit voorbeeld is gelijk aan de volgende opdracht die expliciet in de URL is opgegeven:

```
zoomStep=3&maxZoom=200
```

## Voorbeeld 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Een voorinstelling voor viewers met de naam `Shoppable_Banner` bevat de volgende gegevens:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Laad de viewer met de volgende opdracht:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Dit voorbeeld is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Voorbeeld 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Een voorinstelling voor viewers met de naam `Shoppable_Video_Dark` bevat de volgende gegevens:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Laad de viewer met de volgende opdracht:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Dit voorbeeld is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Voorbeeld 5 {#section-19b988551d1d492a9079948e0b04b38f}

Een voorinstelling voor viewers met de naam `Carousel_Dotted_light` de volgende gegevens:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Laad de viewer met de volgende opdracht:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Dit voorbeeld is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
