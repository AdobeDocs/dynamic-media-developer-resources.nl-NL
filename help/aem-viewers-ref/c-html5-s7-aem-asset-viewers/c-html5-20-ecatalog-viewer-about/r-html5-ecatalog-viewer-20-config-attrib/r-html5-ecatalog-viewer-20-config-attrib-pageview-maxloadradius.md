---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`voorlader`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> voorlader</span></span> </p> </td> 
   <td colname="col2"> <p>Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span> de component laadt alle catalogusframes vooraf wanneer deze niet actief zijn. </p> <p> Wanneer ingesteld op <span class="codeph"> 0</span> de component laadt alleen het frame dat momenteel zichtbaar, vorig en volgend frame is. </p> <p>Set <span class="codeph"><span class="varname"> voorlader</span></span> om te bepalen hoeveel onzichtbare kaders rond het momenteel getoonde kader in een nutteloze staat worden vooraf geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-4b7952997f9240e581d21bcdb173f9af}

Optioneel.

## Standaard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Voorbeeld {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
