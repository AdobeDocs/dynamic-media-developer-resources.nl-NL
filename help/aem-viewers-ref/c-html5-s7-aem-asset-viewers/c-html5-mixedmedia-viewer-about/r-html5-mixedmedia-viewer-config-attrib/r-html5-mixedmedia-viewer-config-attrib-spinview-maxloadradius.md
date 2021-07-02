---
description: Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> De waarde <span class="codeph"> -1</span> laadt alle frames in de set vooraf. De vooraf geladen frames worden altijd weergegeven met de oorspronkelijke resolutie die de SpinView aanvankelijk had geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de kwaliteit van vooraf geladen frames. </p> <p>Wanneer ingesteld op <span class="codeph"> 1</span>, worden de frames in hoge kwaliteit geladen, overeenkomend met de grootte van de component. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span> wordt alleen de voorvertoningstegel met lage resolutie geladen. </p> <p>Het vooraf laden in hoge resolutie verbetert de gebruikerservaring, vooral wanneer automatisch draaien is ingeschakeld. Tegelijkertijd, resulteert het in langzamere begintijd en hogere netwerkconsumptie, zodat zou het met zorg moeten worden gebruikt. Wanneer vooraf geladen frames met hoge resolutie wordt gebruikt, bevinden de vooraf geladen frames zich altijd in de oorspronkelijke resolutie waarin de component voor het eerst werd geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
