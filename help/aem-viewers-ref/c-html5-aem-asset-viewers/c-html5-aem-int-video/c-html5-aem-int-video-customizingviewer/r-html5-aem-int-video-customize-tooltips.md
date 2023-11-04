---
title: Knopinfo
description: Op desktopsystemen hebben bepaalde gebruikersinterface-elementen, zoals knoppen, knopinfo die wordt weergegeven wanneer de muisaanwijzer wordt bewogen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 430809d8-3d51-49b7-b6bf-c3c3c77501ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Knopinfo{#tooltips}

Op desktopsystemen hebben bepaalde gebruikersinterface-elementen, zoals knoppen, knopinfo die wordt weergegeven wanneer de muisaanwijzer wordt bewogen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van knopinfo wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7tooltip
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Straal achtergrondrand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondrandkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Naam tekstlettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte tekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Als knopinfo-stijlen worden aangepast vanuit de ingesloten webpagina, moeten alle eigenschappen de eigenschap `!IMPORTANT` regel. Deze notitie is niet nodig als knopinfo wordt aangepast in het CSS-bestand van de viewer.

## Voorbeeld {#section-59e009fd05b14019936aba04d7ca779d}

U stelt knopinfo in met een grijze rand met een straal van drie pixels voor hoeken, een zwarte achtergrond en witte tekst in Arial®, 11 pixels:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
