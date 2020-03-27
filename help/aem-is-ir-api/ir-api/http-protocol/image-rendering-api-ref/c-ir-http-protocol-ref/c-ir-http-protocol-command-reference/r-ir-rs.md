---
description: Geavanceerde renderinstellingen. Geeft geavanceerde renderinstellingen op die moeten worden toegepast bij het renderen van de huidige selectie.
seo-description: Geavanceerde renderinstellingen. Geeft geavanceerde renderinstellingen op die moeten worden toegepast bij het renderen van de huidige selectie.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rs{#rs}

Geavanceerde renderinstellingen. Geeft geavanceerde renderinstellingen op die moeten worden toegepast bij het renderen van de huidige selectie.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Tekenreeks renderinstellingen. </p></td> 
 </tr> 
</table>

Wordt gebruikt voor het verfijnen van het uiterlijk van renderbewerkingen. Gebruik de teruggevende eigenschap van het Hulpmiddel van de Authoring van Vignet (een deel van het Scene7 pakket van de Authoring van het Beeld) om teruggegeven montagestekenreeksen tot stand te brengen.

## Eigenschappen {#section-9a2b2228789046658cb80eddf343af75}

Materiaalkenmerk.

## Standaard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Voorbeeld {#section-47e4811882574441a4d517e42a35f352}

Na wat experimenteren met het maken van afbeeldingen, wordt bepaald dat onscherp maskeren (USM) de juiste hoeveelheid verscherping biedt voor de desbetreffende toepassing en het desbetreffende materiaal. De tekenreeks met renderinstellingen die USM configureert, wordt gekopieerd naar de `rs=` opdracht die u met dit materiaal wilt gebruiken:

`…&rs=U2V20W50X2&…`

## Zie ook {#section-930116e735024a008c994547ba36ee40}

[catalogus:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
