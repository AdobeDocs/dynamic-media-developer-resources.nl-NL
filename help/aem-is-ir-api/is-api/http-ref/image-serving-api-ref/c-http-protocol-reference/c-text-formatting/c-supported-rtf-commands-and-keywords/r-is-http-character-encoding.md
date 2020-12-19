---
description: Gebruik de volgende opdrachten voor het coderen van tekens.
seo-description: Gebruik de volgende opdrachten voor het coderen van tekens.
seo-title: Tekencodering
solution: Experience Manager
title: Tekencodering
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Tekencodering{#character-encoding}

Gebruik de volgende opdrachten voor het coderen van tekens.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Opdracht </th> 
   <th class="entry"> Beschrijving </th> 
   <th class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Enkel 8-bits teken. </p> </td> 
   <td> <p><span class="varname"> HH </span> moet een hexadecimale waarde van 2 cijfers zijn. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Eén Unicode-teken. </p> </td> 
   <td> <p><span class="varname"> </span> Nis een 2-byte geheel getal met teken en daarom moet een Unicode-waarde groter dan 32767 worden uitgedrukt als een negatief getal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode-tekengrootte. </p> </td> 
   <td> <p>Aantal bytes dat overeenkomt met opgegeven Unicode-teken. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Er volgen tekens uit het gebied met de lage ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>Er volgen tekens uit het gebied met hoge ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Hierna volgen double-bytetekens. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

