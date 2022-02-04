---
title: SpinView.maxloadradius
description: Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Een waarde van <span class="codeph"> -1</span> Hiermee worden alle frames in de set vooraf geladen. De vooraf geladen frames worden altijd weergegeven met de oorspronkelijke resolutie die de SpinView aanvankelijk had geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de kwaliteit van vooraf geladen frames. </p> <p>Wanneer ingesteld op <span class="codeph"> 1</span> de frames worden geladen in hoge kwaliteit, overeenkomend met de grootte van de component. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span> alleen de voorvertoningstegel met lage resolutie wordt geladen.</p> <p>Het vooraf laden in hoge resolutie verbetert de gebruikerservaring, vooral wanneer auto-spin wordt toegelaten. Tegelijkertijd, resulteert het in langzamere begintijd en hogere netwerkconsumptie, zodat zou het met zorg moeten worden gebruikt. Wanneer vooraf geladen frames met hoge resolutie wordt gebruikt, bevinden de vooraf geladen frames zich altijd in de oorspronkelijke resolutie waarin de component voor het eerst werd geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
