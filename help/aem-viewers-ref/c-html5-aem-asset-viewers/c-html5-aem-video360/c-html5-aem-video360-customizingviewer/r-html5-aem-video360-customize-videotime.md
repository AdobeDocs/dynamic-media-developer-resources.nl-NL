---
title: Videotijd
description: De videotijd is de numerieke weergave waarin de huidige tijd en duur van de video die momenteel wordt afgespeeld, worden weergegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Videotijd{#video-time}

De videotijd is de numerieke weergave waarin de huidige tijd en duur van de video die momenteel wordt afgespeeld, worden weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De lettertypefamilie, tekengrootte en lettertypekleur van de videotijd behoren tot de eigenschappen die CSS kan besturen. Het kan ook, met betrekking tot de controlebar worden geplaatst die het bevat, door CSS.

De weergave van de videotijd wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7videotime
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

**Voorbeeld** - Stel de videotijd in op lichtgrijs (hexadecimaal) `#BBBBBB`), met een grootte van 12 pixels, op 15 pixels afstand van de bovenkant van de besturingsbalk en op 80 pixels afstand van de boven- en rechterrand van de besturingsbalk.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
