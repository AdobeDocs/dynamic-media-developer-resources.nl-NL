---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duur`*][, *`richting`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Schakelt de automatische centrifugeanimatie in of uit. Voor een optimale ervaring met automatisch draaien is het raadzaam alle frames vooraf te laden door <span class="codeph"> maxloadradius</span> tot <span class="codeph"> -1</span>. Deze instelling resulteert echter in een hogere laadtijd en een hoger bandbreedtegebruik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p> Het aantal seconden per volledige centrifuge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> richting</span></span> </p> </td> 
   <td colname="col2"> <p> De draairichting <span class="codeph"> 0</span> voor het spinnen in het oosten en <span class="codeph"> 1</span> voor het draaiende westen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Het aantal volledige rotaties dat is uitgevoerd voordat het automatisch centrifugeren wordt gestopt. Het getal is een drijvende-kommagetal. Instellen op <span class="codeph"> -1</span> voor een oneindige auto die draait. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
