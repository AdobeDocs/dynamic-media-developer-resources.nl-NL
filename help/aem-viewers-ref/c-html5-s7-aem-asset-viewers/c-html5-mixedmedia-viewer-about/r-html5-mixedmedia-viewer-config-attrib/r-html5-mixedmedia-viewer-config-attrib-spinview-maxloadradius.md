---
description: Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.
seo-description: Geeft het maximale aantal frames aan dat in elke richting vooraf wordt geladen wanneer de SpinView inactief is.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col2"> <p> Hiermee bepaalt u de kwaliteit van vooraf geladen frames. </p> <p>Wanneer de waarde is ingesteld op <span class="codeph"> 1</span> , worden de frames in hoge kwaliteit geladen, overeenkomstig de grootte van de component. </p> <p>Wanneer u deze optie instelt op <span class="codeph"> 0</span> , wordt alleen de voorvertoningstegel met lage resolutie geladen. </p> <p>Het vooraf laden in hoge resolutie verbetert de gebruikerservaring, vooral wanneer automatisch draaien is ingeschakeld. Tegelijkertijd, resulteert het in langzamere begintijd en hogere netwerkconsumptie, zodat zou het met zorg moeten worden gebruikt. Wanneer vooraf geladen frames met hoge resolutie wordt gebruikt, bevinden de vooraf geladen frames zich altijd in de oorspronkelijke resolutie waarin de component voor het eerst werd geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
