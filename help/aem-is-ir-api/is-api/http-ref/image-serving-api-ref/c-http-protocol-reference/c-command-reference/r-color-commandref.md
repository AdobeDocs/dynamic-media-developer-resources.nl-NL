---
title: kleur
description: Laagkleur. Hiermee geeft u de voorgrondkleur en dekking van effen kleuren en effectlagen op en de vulkleur van het tekstvak voor tekstlagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# kleur{#color}

Laagkleur. Hiermee geeft u de voorgrondkleur en dekking van effen kleuren en effectlagen op en de vulkleur van het tekstvak voor tekstlagen.

` color= *`kleur`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kleur </span> </span> </p> </td> 
  <td class="stentry"> <p>Kleurwaarde voor Grijs, RGB of CMYK, met of zonder alfa. </p> </td> 
 </tr> 
</table>

Als er afbeeldings- en tekstlagen zijn, `color=` Hiermee vult u transparante en semi-dekkende gebieden binnen het selectiekader van de laag met de opgegeven kleur* voor* `rotate=` en `extend=` worden toegepast.

## Eigenschappen {#section-d6e74c36a49547849212e4db8927e678}

Laagkenmerk. Is van toepassing op huidige laag of op laag 0 als `layer=comp`.

De optie *`color`* wordt verondersteld te bestaan in de werkkleurruimte die overeenkomt met het pixeltype van *`color`*. en *`color`* nauwkeurig wordt omgezet als de laagafbeelding een ander pixeltype heeft op het moment van samenvoegen.

## Standaard {#section-60611c72876b4c45b5c85ce35608e5ec}

Geen standaardinstelling voor effen kleuren en effectlagen; er moet een kleur worden opgegeven. De standaardwaarde is 0,0,0,0 (volledig transparant) voor afbeeldings- en tekstlagen.

## Voorbeeld {#section-2d090493f4ec4e188bbc5565aa151a05}

In het volgende sjabloonfragment wordt de tekstachtergrond ingesteld op een dekkende kleur van 50% en wordt dezelfde kleur gebruikt om een halftransparante rand van 10 pixels toe te voegen rondom de afbeelding van laag 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Zie ook {#section-f0e059f857b64b61ab4f23312b8dc619}

[kleur](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Kleurbeheer](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
