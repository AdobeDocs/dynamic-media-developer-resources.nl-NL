---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Schakelt de automatische centrifugeanimatie in of uit. Voor de beste ervaring met automatisch draaien wordt aanbevolen om alle frames vooraf te laden door <span class="codeph"> maxloadradius</span> in te stellen op <span class="codeph"> -1</span>. Merk op, echter, dat dit in verhoogde ladingstijd en hoger bandbreedtegebruik resulteert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p> Het aantal seconden per volledige centrifuge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> richting</span></span> </p> </td> 
   <td colname="col2"> <p> De centrifugeerrichting die <span class="codeph"> 0</span> is voor het spinnen oost en <span class="codeph"> 1</span> voor het spinnen west. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Het aantal volledige rotaties dat is uitgevoerd voordat het automatisch centrifugeren wordt gestopt. Het getal is een drijvende-kommagetal. Stel in op <span class="codeph"> -1</span> voor een oneindige automatische centrifuge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
