---
description: De besturingsbalk is het rechthoekige gebied dat alle UI-besturingselementen bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort, en bevindt zich achter deze besturingselementen.
seo-description: De besturingsbalk is het rechthoekige gebied dat alle UI-besturingselementen bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort, en bevindt zich achter deze besturingselementen.
seo-title: Besturingsbalk
solution: Experience Manager
title: Besturingsbalk
topic: Dynamic media
uuid: 5686b670-3c8c-4bef-b428-dc468f6ca05d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Besturingsbalk{#control-bar}

De besturingsbalk is het rechthoekige gebied dat alle UI-besturingselementen bevat die beschikbaar zijn voor de videoviewer, zoals de knop Afspelen/Pauzeren, volumeregelingen enzovoort, en bevindt zich achter deze besturingselementen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De besturingsbalk heeft altijd de volledige beschikbare viewerbreedte nodig. Het is mogelijk de kleur, hoogte en verticale positie ervan te wijzigen met CSS ten opzichte van de container van de videoviewer.

De volgende CSS klassenselecteur controleert de verschijning van de controlebar:

```
.s7videoviewer .s7controlbar
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

Een videoviewer instellen met een grijze besturingsbalk van 30 pixels hoog en bevindt zich boven aan de container van de videoviewer.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

