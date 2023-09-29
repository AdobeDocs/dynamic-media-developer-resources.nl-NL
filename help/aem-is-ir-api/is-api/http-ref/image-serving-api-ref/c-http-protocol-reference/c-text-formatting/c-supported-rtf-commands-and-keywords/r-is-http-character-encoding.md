---
title: Tekencodering
description: Gebruik de volgende opdrachten voor het coderen van tekens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
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
   <td> <p><span class="varname"> HH</span> moet een hexadecimale waarde van 2 cijfers zijn. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Eén Unicode-teken. </p> </td> 
   <td> <p><span class="varname"> N</span> is een 2-byte geheel getal met teken en een Unicode-waarde groter dan 32767 moet daarom worden uitgedrukt als een negatief getal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode-tekengrootte. </p> </td> 
   <td> <p>Aantal bytes dat overeenkomt met een bepaald Unicode-teken. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Tekens uit het gebied met de lage ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Tekens uit het gebied met hoge ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Hierna volgen double-bytetekens. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
