---
description: De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.
seo-description: De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.
seo-title: Video360-speler
solution: Experience Manager
title: Video360-speler
topic: Dynamic media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video360-speler{#video-player}

De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Als de afmetingen van de video die wordt afgespeeld niet overeenkomen met de afmetingen van de videospeler, wordt de video-inhoud gecentreerd in het rechthoekige weergavegebied van de videospeler.

De volgende CSS-klassenkiezer bepaalt de weergave van de videospeler:

```
.s7video360viewer .s7video360player
```

**CSS-eigenschappen van de videospeler**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt het foutbericht lokaliseren dat wordt weergegeven wanneer het systeem de video niet kan afspelen.

Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Voorbeeld - Een videoviewer instellen met een grootte van 512 x 288 pixels voor de videospeler.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

De vormgeving van de bufferanimatie wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7video360player .s7waiticon
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
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

