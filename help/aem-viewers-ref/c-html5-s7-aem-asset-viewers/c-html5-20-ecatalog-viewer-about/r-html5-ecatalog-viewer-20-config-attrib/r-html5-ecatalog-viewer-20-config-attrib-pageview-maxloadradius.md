---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`voorlader`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span>, laadt de component alle catalogusframes wanneer deze niet worden gebruikt. </p> <p> Wanneer ingesteld op <span class="codeph"> 0</span> laadt de component alleen het frame dat momenteel zichtbaar is, het vorige en volgende frame. </p> <p>Stel <span class="codeph"><span class="varname"> voorlader</span></span> in om te bepalen hoeveel onzichtbare frames rondom het momenteel weergegeven frame bij inactiviteit worden voorgeladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-4b7952997f9240e581d21bcdb173f9af}

Optioneel.

## Standaard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Voorbeeld {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
