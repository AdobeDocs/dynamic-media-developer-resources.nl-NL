---
description: Laagkleur. Hiermee geeft u de voorgrondkleur en dekking van effen kleuren en effectlagen op en de vulkleur van het tekstvak voor tekstlagen.
seo-description: Laagkleur. Hiermee geeft u de voorgrondkleur en dekking van effen kleuren en effectlagen op en de vulkleur van het tekstvak voor tekstlagen.
seo-title: kleur
solution: Experience Manager
title: kleur
topic: Scene7 Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# color{#color}

Laagkleur. Hiermee geeft u de voorgrondkleur en dekking van effen kleuren en effectlagen op en de vulkleur van het tekstvak voor tekstlagen.

` color= *`kleur`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kleur  </span> </span> </p> </td> 
  <td class="stentry"> <p>Grijswaarde, RGB- of CMYK-kleurwaarde, met of zonder alfa. </p> </td> 
 </tr> 
</table>

In het geval van afbeeldings- en tekstlagen vult `color=` transparante en semi-dekkende gebieden binnen het selectiekader van de laag met de opgegeven kleur* voordat* `rotate=` en `extend=` worden toegepast.

## Eigenschappen {#section-d6e74c36a49547849212e4db8927e678}

Laagkenmerk. Wordt toegepast op de huidige laag of op laag 0 als `layer=comp`.

*`color`* wordt aangenomen dat deze voorkomt in de werkkleurruimte die overeenkomt met het pixeltype van  *`color`*. *`color`* nauwkeurig wordt omgezet als de laagafbeelding een ander pixeltype heeft op het moment van samenvoegen.

## Standaard {#section-60611c72876b4c45b5c85ce35608e5ec}

Geen standaardwaarde voor effen kleuren en effectlagen; er moet een kleur worden opgegeven. De standaardwaarde is 0,0,0,0 (volledig transparant) voor afbeeldings- en tekstlagen.

## Voorbeeld {#section-2d090493f4ec4e188bbc5565aa151a05}

In het volgende sjabloonfragment stellen we de tekstachtergrond in op een dekkende kleur van 50% en gebruiken we dezelfde kleur om een halftransparante rand van 10 pixels toe te voegen rondom de afbeelding van laag 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Zie ook {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
