---
description: De volgende documenteigenschappen worden ondersteund in tekstvakken.
solution: Experience Manager
title: Documenteigenschappen (tekstvak)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Documenteigenschappen (tekstvak){#document-text-box-properties}

De volgende documenteigenschappen worden ondersteund in tekstvakken.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Opdracht</b> </th> 
   <th class="entry"> <b>Beschrijving</b> </th> 
   <th class="entry"> <b>Notities</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Lettertypetabel. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Tekenset voor lettertype <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGB-kleurentabel. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK-kleurentabel. </p> </td> 
   <td> <p>Dynamic Media-extensie. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Kleurentabel voor kleuren die dienen als afbeelding. </p> </td> 
   <td> <p>Dynamic Media-extensie; <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Kleurcomponent rood. </p> </td> 
   <td> <p>Mag alleen worden weergegeven in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>Groene kleurcomponent. </p> </td> 
   <td> <p>Mag alleen worden weergegeven in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>Blauwe kleurcomponent. </p> </td> 
   <td> <p>Mag alleen worden weergegeven in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyaan <span class="varname"> N </span> </span> </td> 
   <td> <p>Cyaan kleurcomponent. </p> </td> 
   <td> <p>Dynamic Media-extensie; mag alleen worden weergegeven in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Magenta kleurcomponent. </p> </td> 
   <td> <p>Dynamic Media-extensie; mag alleen worden weergegeven in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span> </span> </td> 
   <td> <p>Gele kleurcomponent. </p> </td> 
   <td> <p>Dynamic Media-extensie; mag alleen worden weergegeven in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>Zwarte kleurcomponent. </p> </td> 
   <td> <p>Dynamic Media-extensie; mag alleen worden weergegeven in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Linkermarge. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Rechtermarge. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Bovenmarge. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Ondermarge. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertal t </span> </td> 
   <td> <p>Tekst boven uitlijnen in tekstvak. </p> </td> 
   <td> <p>Standaard </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertal b </span> </td> 
   <td> <p>Tekst onder uitlijnen in tekstvak. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertal c </span> </td> 
   <td> <p>Tekst centreren in het tekstvak. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Tekststroomrichting. </p> </td> 
   <td> <p>taalspecifieke tekstdoorloop; <span class="codeph"> textPs= </span> alleen 0 (standaard) links-rechts, boven-onder (Europees) 1 boven-onder, rechts-links (Far Eastern) </p> </td> 
  </tr> 
 </tbody> 
</table>
