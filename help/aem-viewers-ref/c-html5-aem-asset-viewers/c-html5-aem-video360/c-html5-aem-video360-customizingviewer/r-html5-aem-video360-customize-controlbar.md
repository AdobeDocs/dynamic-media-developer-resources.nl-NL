---
description: De besturingsbalk is het rechthoekige gebied dat alle besturingselementen voor de gebruikersinterface bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort.
seo-description: De besturingsbalk is het rechthoekige gebied dat alle besturingselementen voor de gebruikersinterface bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort.
seo-title: Besturingsbalk
solution: Experience Manager
title: Besturingsbalk
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Control bar{#control-bar}

De besturingsbalk is het rechthoekige gebied dat alle besturingselementen voor de gebruikersinterface bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De besturingsbalk heeft altijd de volledige beschikbare viewerbreedte nodig. Het is mogelijk de kleur, hoogte en verticale positie ervan te wijzigen met CSS ten opzichte van de container van de videoviewer.

De volgende CSS klassenselecteur controleert de verschijning van de controlebar:

```
.s7video360viewer .s7controlbar
```

## CSS-eigenschappen van de besturingsbalk {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de onderrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de besturingsbalk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Een videoviewer instellen met een grijze besturingsbalk van 30 pixels hoog en bevindt zich boven aan de container van de videoviewer.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

