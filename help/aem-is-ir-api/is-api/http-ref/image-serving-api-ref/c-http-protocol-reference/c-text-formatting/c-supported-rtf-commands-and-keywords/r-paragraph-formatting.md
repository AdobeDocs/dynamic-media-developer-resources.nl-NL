---
description: De volgende opdrachten voor alineaopmaak worden ondersteund.
seo-description: De volgende opdrachten voor alineaopmaak worden ondersteund.
seo-title: Alinea-opmaak
solution: Experience Manager
title: Alinea-opmaak
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td> <p>Standaard; alleen <span class="codeph"> textPs= </span> ; genegeerd als <span class="codeph"> \qj niet actief </span>is. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Lijn de laatste regel van een uitgevulde alinea rechts uit. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj </span> niet actief is. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>De laatste regel van een uitgevulde alinea centreren. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj niet actief </span>is. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>De laatste regel van een uitgevulde alinea uitrekken (uitrekken). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> alleen; genegeerd als <span class="codeph"> \qj niet actief </span>is. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span></span> </td> 
   <td> <p>Eerste regel inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span></span> </td> 
   <td> <p>Links inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span></span> </td> 
   <td> <p>Rechts inspringen. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span></span> </td> 
   <td> <p>Ruimte tussen regels. </p> </td> 
   <td> <p>0 (standaard) voor automatische regelafstand; positieve waarden om alleen waarde te gebruiken als deze groter is dan de standaardregelafstand; negatieve waarde om spatiëring te forceren. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span></span> </td> 
   <td> <p>Regelafstand meerdere markeringen. </p> </td> 
   <td> <p>Stel de waarde in op 0 (standaard) als <span class="codeph"> \sl </span> zich in twips bevindt, op 1 als <span class="codeph"> \sl </span> zich in veelvouden van de standaardafstand bevindt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span></span> </td> 
   <td> <p>Extra ruimte voor alinea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>past <span class="codeph"> \sb </span> toe op de eerste alinea in het tekstvak, <span class="codeph"> textPs= </span> niet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span></span> </td> 
   <td> <p>Extra ruimte na alinea. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> past <span class="codeph"> \sa </span> toe op de laatste alinea in het tekstvak, <span class="codeph"> textPs= </span> niet. </p> </td> 
  </tr> 
 </tbody> 
</table>

