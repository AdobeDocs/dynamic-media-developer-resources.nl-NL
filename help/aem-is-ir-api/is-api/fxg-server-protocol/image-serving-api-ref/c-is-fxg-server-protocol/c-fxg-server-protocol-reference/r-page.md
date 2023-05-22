---
description: Pagina ophalen. Hiermee wordt een specifieke pagina in een FXG-bestand van meerdere pagina's opgehaald.
solution: Experience Manager
title: page
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# page{#page}

Pagina ophalen. Hiermee wordt een specifieke pagina in een FXG-bestand van meerdere pagina&#39;s opgehaald.

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Paginanummer (eerste pagina is 1). </p></td> 
 </tr> 
</table>

## Standaard {#section-3fd7fcc525b947c7a95457e50414ac9e}

Indien `page` wordt niet opgegeven, wordt de eerste pagina geretourneerd voor rasteruitvoer en alle pagina&#39;s voor PDF-uitvoer.
