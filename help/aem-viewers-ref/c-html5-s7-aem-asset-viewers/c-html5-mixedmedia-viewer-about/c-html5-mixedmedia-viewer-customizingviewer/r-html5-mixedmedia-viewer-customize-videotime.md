---
title: Videotijd
description: De videotijd is de numerieke weergave waarin de huidige tijd en duur van de video die momenteel wordt afgespeeld, worden weergegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Videotijd{#video-time}

De videotijd is de numerieke weergave waarin de huidige tijd en duur van de video die momenteel wordt afgespeeld, worden weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De lettertypefamilie, tekengrootte en lettertypekleur van de videotijd behoren tot de eigenschappen die CSS kan besturen. Het kan ook, met betrekking tot de controlebar worden geplaatst die het bevat, door CSS.

De weergave van de videotijd wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7videotime
```

## CSS-eigenschappen van videotijd {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de rechterrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van het besturingselement voor videotijd. Deze eigenschap is vereist voor de juiste werking van Internet Explorer 8 of hoger. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>De lettertypefamilie die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>De tekengrootte die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>De lettertypekleur die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

De videotijd instellen op lichtgrijs (hexadecimaal) `#BBBBBB`), met een grootte van 12 pixels, geplaatst op 15 pixels van de bovenkant van de besturingsbalk en 80 pixels van de rechterranden van de besturingsbalk.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
