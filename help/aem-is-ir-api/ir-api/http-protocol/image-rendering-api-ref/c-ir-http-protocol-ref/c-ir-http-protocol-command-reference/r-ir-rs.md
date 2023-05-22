---
title: rs
description: Geavanceerde renderinstellingen. Geeft geavanceerde renderinstellingen op die moeten worden toegepast bij het renderen van de huidige selectie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

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

Wordt gebruikt voor het verfijnen van het uiterlijk van renderbewerkingen. Als u reeksen met renderinstellingen wilt maken, gebruikt u de renderfunctie van het Vignet Authoring Tool (onderdeel van het Dynamic Media-pakket voor het schrijven van afbeeldingen).

## Eigenschappen {#section-9a2b2228789046658cb80eddf343af75}

Materiaalkenmerk.

## Standaard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Voorbeeld {#section-47e4811882574441a4d517e42a35f352}

Na wat experimenteren met het maken van afbeeldingen, wordt bepaald dat onscherp maskeren (USM) de juiste hoeveelheid verscherping biedt voor de desbetreffende toepassing en het desbetreffende materiaal. De tekenreeks met renderinstellingen die USM configureert, wordt naar de `rs=` gebruiken met dit materiaal:

`…&rs=U2V20W50X2&…`

## Zie ook {#section-930116e735024a008c994547ba36ee40}

[catalogus:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
