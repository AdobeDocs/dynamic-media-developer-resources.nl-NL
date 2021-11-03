---
description: De videospeler voor slimme uitsnijdingen is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.
solution: Experience Manager
title: Videospeler
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Videospeler{#video-player}

De videospeler voor slimme uitsnijdingen is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Als de afmetingen van de video die wordt afgespeeld niet overeenkomen met de afmetingen van de videospeler voor SmartCrop, wordt de video-inhoud gecentreerd binnen het weergavegebied van de videospeler voor SmartCrop.

De volgende CSS-klassenkiezer bepaalt de weergave van de slimme-uitsnijdvideospeler:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**CSS-eigenschappen van de slimme-uitsnijdvideospeler**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het foutbericht dat wordt weergegeven als het systeem de video niet kan afspelen, kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie .

Voorbeeld - Een viewer voor slimme-uitsnijdvideo instellen met een grootte van 512 x 288 pixels voor de slimme-uitsnijdvideospeler.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Gesloten bijschriften worden in een interne container in de slimme-uitsnijdvideospeler geplaatst. De positie van die container wordt gecontroleerd door gesteunde WebVTT plaatsende exploitanten. De bijschrifttekst zelf bevindt zich in die container en de stijl ervan wordt bestuurd met de volgende CSS-klassenkiezer:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**CSS-eigenschappen van closed captioning**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrond van tekstbijschrift met gesloten bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur van bijschrift sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Dikte lettertype van gesloten bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p> Tekengrootte van gesloten bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertype voor gesloten bijschrift. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - Een gesloten bijschrifttekst instellen op 14 pixels, lichtgrijs, Arial, op een halftransparante zwarte achtergrond:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

De vormgeving van de bufferanimatie wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**CSS-eigenschappen van wachtpictogram**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breedte van animatiepictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Hoogte van animatiepictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Linkermarge van animatiepictogram, normaal gesproken min de helft van de breedte van het pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Bovenmarge van animatiepictogram, normaal gesproken min de helft van de hoogte van het pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> Illustraties uitnemen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een bufferanimatie wilt instellen op 101 pixels breed en 29 pixels hoog:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
