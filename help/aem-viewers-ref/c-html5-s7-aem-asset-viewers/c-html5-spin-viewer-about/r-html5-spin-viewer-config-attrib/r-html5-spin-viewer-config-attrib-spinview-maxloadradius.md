---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is. Een waarde van <span class="codeph"> -1</span> Hiermee worden alle frames in de set vooraf geladen. De vooraf geladen frames worden altijd weergegeven met de oorspronkelijke resolutie die de SpinView aanvankelijk had geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de kwaliteit van vooraf geladen frames. Wanneer ingesteld op <span class="codeph"> 1</span> frames worden geladen in hoge kwaliteit, die overeenkomt met de grootte van de component. Wanneer ingesteld op <span class="codeph"> 0</span> alleen de voorvertoningstegel met lage resolutie wordt geladen. </p> <p>Het vooraf laden in hoge resolutie verbetert de gebruikerservaring, vooral wanneer auto-spin wordt toegelaten. Tegelijkertijd, resulteert het in langzamere begintijd en hogere netwerkconsumptie, zo gebruik met voorzichtigheid. Wanneer een voorgeladen afbeelding met hoge resolutie wordt gebruikt, hebben de vooraf geladen frames altijd de oorspronkelijke resolutie waarop de component aanvankelijk werd geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
