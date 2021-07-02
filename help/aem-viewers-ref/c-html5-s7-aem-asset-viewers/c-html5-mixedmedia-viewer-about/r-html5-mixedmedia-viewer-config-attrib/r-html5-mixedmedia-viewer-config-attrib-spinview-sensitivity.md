---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de gevoeligheid van de horizontale en verticale centrifuge die wordt uitgevoerd met een muis of een veegbeweging. </p> <p> <span class="codeph"> Met </span> xSensitivity stelt u in hoeveel volledige horizontale productrotaties worden gemaakt wanneer de gebruiker de muis horizontaal van de ene kant van de weergave naar de andere sleept. Met de volgende drie opties ziet de gebruiker bijvoorbeeld drie volledige centrifuges voor één volledige sleepbeweging. </p> <p>Op dezelfde manier bepaalt <span class="codeph"> Gevoeligheid</span> de gevoeligheid van de verticale centrifuge. De waarde 1 houdt in dat een volledige verticale sleep of veegbeweging de weergavehoek wijzigt van het bovenste centrifuge naar het onderste (of andersom). </p> <p>Als u een negatieve waarde instelt voor <span class="codeph"> Gevoeligheid</span>, wordt de richting van de verticale centrifuge omgekeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
