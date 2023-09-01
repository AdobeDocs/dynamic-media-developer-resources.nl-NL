---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`voorlader`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> voorlader</span></span> </p> </td> 
   <td colname="col2"> <p>Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span> de component laadt alle catalogusframes vooraf wanneer deze niet actief zijn. </p> <p> Wanneer ingesteld op <span class="codeph"> 0</span> de component laadt alleen het frame dat zichtbaar is, het vorige frame en het volgende frame. </p> <p>Set <span class="codeph"><span class="varname"> voorlader</span></span> om te bepalen hoeveel onzichtbare kaders rond het momenteel getoonde kader in een nutteloze staat worden vooraf geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-4b7952997f9240e581d21bcdb173f9af}

Optioneel.

## Standaard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Voorbeeld {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
