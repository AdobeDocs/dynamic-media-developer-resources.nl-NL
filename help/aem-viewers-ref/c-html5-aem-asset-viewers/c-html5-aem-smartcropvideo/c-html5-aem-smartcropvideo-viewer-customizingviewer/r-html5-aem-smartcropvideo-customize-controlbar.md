---
title: Besturingsbalk
description: De besturingsbalk is het rechthoekige gebied dat alle UI-besturingselementen bevat die beschikbaar zijn voor de viewer voor SmartCrop Video, zoals de knop Afspelen/Pauzeren en de volumeregelaars.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 8ea06e0a-705d-436a-9393-75a36381cba6
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Besturingsbalk{#control-bar}

De besturingsbalk is het rechthoekige gebied dat alle UI-besturingselementen bevat die beschikbaar zijn voor de viewer voor SmartCrop Video, zoals de knop Afspelen/Pauzeren en de volumeregelaars.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De besturingsbalk heeft altijd de volledige beschikbare viewerbreedte nodig. Het is mogelijk de kleur, hoogte en verticale positie van de component te wijzigen met CSS ten opzichte van de viewercontainer voor SmartCrop Video.

De volgende CSS klassenselecteur controleert de verschijning van de controlebar:

```
.s7smartcropvideoviewer .s7controlbar
```

## CSS-eigenschappen van de besturingsbalk {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de onderrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de besturingsbalk. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

Een viewer voor SmartCrop-video instellen met een grijze besturingsbalk die 30 pixels hoog is en boven aan de viewercontainer voor SmartCrop-video wordt weergegeven.

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
