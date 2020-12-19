---
description: Gebruik de volgende opdrachten voor geavanceerde tekstopmaak.
seo-description: Gebruik de volgende opdrachten voor geavanceerde tekstopmaak.
seo-title: Geavanceerde tekstopmaak
solution: Experience Manager
title: Geavanceerde tekstopmaak
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Geavanceerde tekstopmaak{#advanced-text-formatting}

Gebruik de volgende opdrachten voor geavanceerde tekstopmaak.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Opdracht </th> 
   <th class="entry"> Beschrijving </th> 
   <th class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Subscript zonder wijziging van tekengrootte. </p> </td> 
   <td> <p>positie in halve punten; de standaardwaarde is 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Superscript zonder wijziging van tekengrootte. </p> </td> 
   <td> <p>positie in halve punten; de standaardwaarde is 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>In-/uitschakelen bij opgegeven tekengrootte. </p> </td> 
   <td> <p>Tekengrootte in halve punten, waarboven tekenspatiëring moet worden toegepast; 0 om tekenspatiëring uit te schakelen; De standaardwaarde is 1 voor tekenspatiëring van alle tekengrootten op een half punt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptische  </span> </td> 
   <td> <p>Selecteer optische tekenspatiëring. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetrisch  </span> </td> 
   <td> <p>Selecteer metrische spatiëring. </p> </td> 
   <td> <p>Standaard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \uitvouwen  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tekenspatiëring wijzigen. </p> </td> 
   <td> <p>positieve of negatieve kwartpunten; de standaardwaarde is 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tekenspatiëring wijzigen. </p> </td> 
   <td> <p>Positieve of negatieve twips. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Horizontale tekenschaling. </p> </td> 
   <td> <p>positief of negatief percentage; de standaardwaarde is 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Verticale tekenschaling. </p> </td> 
   <td> <p>positief of negatief percentage; de standaardwaarde is 100; Scene7-extensie. </p> <p> <span class="codeph"> \charscaley schaalt  </span> ook de regelafstand bij toepassing met  <span class="codeph"> text=  </span>. <span class="codeph"> textPs= behoudt  </span> altijd de regelafstand, ongeacht de mate van verticale tekenschaling. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Selecteer tekenstroom van links naar rechts. </p> </td> 
   <td> <p>Standaard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Selecteer tekenstroom van rechts naar links. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Enable copy-fitting and set maximum allowed font size. </p> </td> 
   <td> <p>Tekengrootte in halve punten; <span class="codeph"> textPs= alleen </span>; Scene7-extensie. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximale aantal regels voor passend maken van kopieën (zachte beperkingen). </p> </td> 
   <td> <p>0 voor geen regelbeperking; <span class="codeph"> textPs= alleen </span>; Scene7-extensie. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximale aantal regels voor passend maken van tekst (afkappen). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Scene7-extensie. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tekenrichting. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; genegeerd voor niet-Romeinse lettertypen; genegeerd als  <span class="codeph"> \stextflow1 niet  </span> van kracht is. </p> <p>0 verticaal (standaard). </p> <p>1 gedraaid 90 graden rechtsom. </p> </td> 
  </tr> 
 </tbody> 
</table>

