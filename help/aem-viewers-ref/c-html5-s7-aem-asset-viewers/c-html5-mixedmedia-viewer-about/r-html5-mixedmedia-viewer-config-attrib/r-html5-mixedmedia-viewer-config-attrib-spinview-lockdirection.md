---
description: 'null'
seo-description: 'null'
seo-title: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Geeft aan of een wijziging in de centrifugerichting wordt toegestaan in het geval van een 2D-centrifugeerset. </p> <p>Wanneer deze optie is ingesteld op <span class="codeph"> 1 </span>, identificeert de component de primaire (horizontale of verticale) sleep-richting aan het begin van de beweging. Daarna blijft deze richting behouden totdat de beweging stopt. Als de gebruiker bijvoorbeeld een horizontale draaibeweging start en vervolgens besluit om de sleepbeweging in verticale richting voort te zetten, voert de component geen verticale draaibeweging uit. in plaats daarvan wordt alleen gekeken naar de horizontale beweging van de muis of de veegbeweging. </p> <p>Met de waarde 0 <span class="codeph"> </span> kan de gebruiker de draairichting op elk gewenst moment tijdens de bewegingsvoortgang wijzigen. De instelling heeft geen invloed als de centrifugeset 1D is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
