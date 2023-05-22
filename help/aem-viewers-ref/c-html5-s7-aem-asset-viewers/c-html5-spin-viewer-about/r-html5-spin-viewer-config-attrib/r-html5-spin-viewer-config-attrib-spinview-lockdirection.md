---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Geeft aan of een wijziging in de centrifugerichting is toegestaan als er 2D-centrifugeset is. </p> <p>Wanneer ingesteld op <span class="codeph"> 1 </span>De component identificeert de primaire sleep- of veegrichting (horizontaal of verticaal) aan het begin van de beweging. Daarna blijft deze richting behouden totdat de beweging stopt. Als de gebruiker bijvoorbeeld een horizontale draaibeweging start en vervolgens besluit om de sleepbeweging in verticale richting voort te zetten, voert de component geen verticale draaibeweging uit. In plaats daarvan wordt alleen gekeken naar de horizontale beweging van de muis of veegbeweging. </p> <p>Een waarde van <span class="codeph"> 0 </span> Hiermee kan de gebruiker de draairichting op elk gewenst moment tijdens de bewegingsvoortgang wijzigen. De instelling heeft geen effect als de centrifugeset 1D is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
