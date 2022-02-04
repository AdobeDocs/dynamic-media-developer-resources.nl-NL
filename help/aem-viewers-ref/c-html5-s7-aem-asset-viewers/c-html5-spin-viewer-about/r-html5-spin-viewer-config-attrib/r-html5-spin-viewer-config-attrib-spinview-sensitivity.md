---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`Gevoeligheid`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> Gevoeligheid</span>]</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de gevoeligheid van de horizontale en verticale centrifuge die wordt uitgevoerd met een muis of een veegbeweging. </p> <p> <span class="codeph"> xSensitivity</span> Hiermee stelt u in hoeveel volledige horizontale productrotaties worden gemaakt wanneer de gebruiker de muis horizontaal van de ene kant van de weergave naar de andere sleept. Met de volgende drie opties ziet de gebruiker bijvoorbeeld drie volledige centrifuges voor één volledige sleepbeweging. </p> <p>Evenzo <span class="codeph"> Gevoeligheid</span> bepaalt de gevoeligheid van de verticale centrifuge. De waarde 1 houdt in dat een volledige verticale sleep of veegbeweging de weergavehoek wijzigt van het bovenste centrifuge naar het onderste (of omgekeerd). </p> <p>Een negatieve waarde instellen voor <span class="codeph"> Gevoeligheid</span> Hiermee draait u de richting van de verticale centrifuge om. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
