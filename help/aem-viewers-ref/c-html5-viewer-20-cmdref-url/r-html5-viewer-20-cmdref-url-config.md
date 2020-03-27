---
description: Parameter die alle viewers gemeen hebben.
seo-description: Parameter die alle viewers gemeen hebben.
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# config{#config}

Parameter die alle viewers gemeen hebben.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config-id </span></span> </p> </td> 
   <td colname="col2"> <p>Catalogus/id voor de viewerconfiguratie. </p> <p> Hiermee wordt een item in de afbeeldingscatalogus opgegeven dat de configuratieeigenschappen van de viewer bevat in de <span class="codeph"> catalogus::UserData </span>. Wanneer dit bevel aanwezig is, verzendt de kijker een <span class="codeph"> req=userdata </span> bevel voor <span class="codeph"> configId </span> naar de server en haalt eigenschappen uit het antwoord uit. De eigenschappen worden gebruikt om de viewer te initialiseren. Als de URL-tekenreeks dezelfde eigenschappen opgeeft, overschrijven deze de waarden uit de <span class="codeph"> catalogus::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle vieweropdrachten die u kunt opgeven in `catalog::UserData` , `asset`, `serverUrl`, `contentUrl`en `searchServerUrl``config` zelf.

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

Geen.

## Voorbeeld 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Een afbeeldingscatalogus met de naam 2020 bevat het item `preset-oct`. Het `catalog::UserData` veld van dit item in de catalogus bevat de volgende gegevens:

```
style=customStyle.css
```

Laad de viewer met de volgende opdracht:

```
config=2020/preset-oct
```

Dit is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

```
style=customStyle.css
```

## Voorbeeld 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Een afbeeldingscatalogus met de naam 2019 bevat het item `spin-oct`. Het `catalog::UserData` veld van dit item in de catalogus bevat de volgende gegevens:

```
zoomStep=3 
maxZoom=200
```

Laad de viewer met de volgende opdracht:

```
config=2019/spin-oct
```

Dit is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

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

Dit is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

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

Dit is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Voorbeeld 5 {#section-19b988551d1d492a9079948e0b04b38f}

Een viewervoorinstelling met de naam `Carousel_Dotted_light` van de volgende gegevens:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Laad de viewer met de volgende opdracht:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Dit is gelijk aan de volgende opdrachten die expliciet in de URL worden opgegeven:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

