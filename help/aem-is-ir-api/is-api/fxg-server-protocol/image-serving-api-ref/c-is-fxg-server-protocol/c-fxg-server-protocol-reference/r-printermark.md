---
description: Drukkermarkeringen weergeven. Hiermee geeft u op hoe de drukkermarkeringen moeten worden weergegeven.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 6%

---


# printerMark{#printermark}

Drukkermarkeringen weergeven. Hiermee geeft u op hoe de drukkermarkeringen moeten worden weergegeven.

` printerMark= *`verkleinde `*, *`markeringsaflooptekens `*, *`markeringsmarkering `*, *`voor `*, *`streepjesinformatie `*, *``*, *`voor `*, *`streepjesregistratie;stijllijnwegingslaagingesloten`*`

De verschillende markeringen kunnen worden uit- of ingeschakeld. U kunt ook de stijl van de drukkermarkeringen bepalen.

De volgende waarden zijn geldig:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>snijtekens= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>aflooptekens= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registratietekens= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>kleurenbalken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>paginagegevens= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standaard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Standaard is </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>lijndikte= </p></td> 
  <td class="stentry"> <p>Elke waarde in het bereik 0,125 - 2,0, beide waarden inbegrepen. </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>laag insluiten= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>De standaardwaarde is 1. </p></td> 
 </tr> 
</table>

## Voorbeeld {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
