---
description: Dekking. Hiermee bepaalt u de dekking van het materiaal.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 7910228217db2c97dccd306ce464c69da53ee576
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# opac{#opac}

Dekking. Hiermee bepaalt u de dekking van het materiaal.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>materiaaldekking (in procenten); 0...100 </p> </td> 
 </tr> 
</table>

De volgende materiaal/objectcombinaties ondersteunen een variabele dekking:

* Effen kleuren en herhaalbare structuren die zijn toegepast op overlappende objecten met structuur.
* Venster dat materialen bedekt die op venster dat kadervoorwerpen bedekt worden toegepast.
* Decalen die zijn toegepast op structuurobjecten of wandobjecten.

Als het materiaal een afbeelding met een alfakanaal bevat, kan `opac=` worden gebruikt om de afbeelding transparanter te maken, maar niet meer dekkend.

## Eigenschappen {#section-352f7b82ede54159b6afb90ae4b559ec}

Materiaalkenmerk. Genegeerd als de huidige objectselectie of het materiaal geen dekking ondersteunt.

## Standaard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`voor een volledig dekkend materiaal (als de afbeelding geen alfakanaal bevat).
