---
description: Gebruik de volgende opdrachten voor elementaire tekenopmaak.
seo-description: Gebruik de volgende opdrachten voor elementaire tekenopmaak.
seo-title: Basisopmaak van tekens
solution: Experience Manager
title: Basisopmaak van tekens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Standaardtekenopmaak{#basic-character-formatting}

Gebruik de volgende opdrachten voor elementaire tekenopmaak.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Opdracht </th> 
   <th class="entry"> Beschrijving </th> 
   <th class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \plain  </span> </td> 
   <td> <p>Standaardtekenopmaak herstellen </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Lettertype. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl- </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tekengrootte. </p> </td> 
   <td> <p>Halfpunten; de standaardwaarde is 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Fontkleur. </p> </td> 
   <td> <p>Op 0 gebaseerde index in kleurentabel. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b  </span> </td> 
   <td> <p>Vette stijl. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i  </span> </td> 
   <td> <p>Cursieve stijl. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>Subscript. </p> </td> 
   <td> <p>Hiermee verkleint u de tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>Superscript. </p> </td> 
   <td> <p>Hiermee verkleint u de tekengrootte. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>Onderstrepen. </p> </td> 
   <td> <p>De Beeldserver herkent ook de volgende RTF-onderstrepende opdrachten: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>Deze worden momenteel geïmplementeerd als een standaard <span class="codeph"> \ul </span> onderstrepen. Alle andere onderstrepende RTF-opdrachten worden genegeerd. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>onderstrepen uitschakelen </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>onderstrepen uitschakelen </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps  </span> </td> 
   <td> <p>hoofdletter </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>kleine letters ("kleinkapitalen") </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
 </tbody> 
</table>

