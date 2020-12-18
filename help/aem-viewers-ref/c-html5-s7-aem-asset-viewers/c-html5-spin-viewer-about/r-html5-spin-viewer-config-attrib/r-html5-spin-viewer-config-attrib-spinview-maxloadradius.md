---
description: 'null'
seo-description: 'null'
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is. De waarde <span class="codeph"> -1</span> laadt alle frames in de set vooraf. De vooraf geladen frames worden altijd weergegeven met de oorspronkelijke resolutie die de SpinView aanvankelijk had geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de kwaliteit van vooraf geladen frames. Wanneer ingesteld op <span class="codeph"> 1</span> worden frames in hoge kwaliteit geladen, overeenkomend met de grootte van de component. Wanneer ingesteld op <span class="codeph"> 0</span> wordt alleen de voorvertoningstegel met lage resolutie geladen. </p> <p>Het vooraf laden in hoge resolutie verbetert de gebruikerservaring, vooral wanneer auto-spin wordt toegelaten. Tegelijkertijd, resulteert het in langzamere begintijd en hogere netwerkconsumptie, zo gebruik met voorzichtigheid. Wanneer een voorgeladen hoge resolutie wordt gebruikt, bevinden de voorgeladen frames zich altijd met de oorspronkelijke resolutie waarin de component aanvankelijk werd geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
