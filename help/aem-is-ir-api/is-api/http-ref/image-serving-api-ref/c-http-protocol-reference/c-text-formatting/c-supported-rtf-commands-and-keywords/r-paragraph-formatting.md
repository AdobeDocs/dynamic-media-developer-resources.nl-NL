---
description: De volgende opdrachten voor alineaopmaak worden ondersteund.
solution: Experience Manager
title: Alinea-opmaak
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Alinea-opmaak{#paragraph-formatting}

De volgende opdrachten voor alineaopmaak worden ondersteund.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Opdracht </p> </th> 
   <th class="entry"> <p>Beschrijving </p> </th> 
   <th class="entry"> <p>Notities </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Standaardalineaopmaak herstellen </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Tekst links uitlijnen. </p> </td> 
   <td> <p>Standaard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Tekst rechts uitlijnen. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Tekst horizontaal centreren. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Tekst horizontaal uitvullen. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Lijn de laatste regel van een alinea links uit. </p> </td> 
   <td> <p>Standaard; <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj </span>is niet actief. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Lijn de laatste regel van een uitgevulde alinea rechts uit. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj </span> is niet actief. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>De laatste regel van een uitgevulde alinea centreren. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj </span>is niet actief. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>De laatste regel van een uitgevulde alinea uitrekken (uitrekken). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj </span>is niet actief. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Eerste regel inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Links inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Rechts inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Ruimte tussen regels. </p> </td> 
   <td> <p>0 (standaard) voor automatische regelafstand; positieve waarden om alleen waarde te gebruiken als deze groter is dan de standaardregelafstand; negatieve waarde om spatiëring te forceren. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Regelafstand meerdere markeringen. </p> </td> 
   <td> <p>Instellen op 0 (standaard) als <span class="codeph"> \sl </span> is in twips, naar 1 if <span class="codeph"> \sl </span> is in veelvouden van de standaardspatiëring. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Extra ruimte voor alinea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>is <span class="codeph"> \sb </span> de eerste alinea van het tekstvak, <span class="codeph"> textPs= </span> niet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Extra ruimte na alinea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> is <span class="codeph"> \sa </span> op de laatste alinea van het tekstvak, <span class="codeph"> textPs= </span> niet. </p> </td> 
  </tr> 
 </tbody> 
</table>
