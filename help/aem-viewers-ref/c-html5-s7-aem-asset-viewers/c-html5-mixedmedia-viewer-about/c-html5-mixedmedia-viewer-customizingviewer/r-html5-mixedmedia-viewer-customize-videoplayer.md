---
description: De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.
seo-description: De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.
seo-title: Videospeler
solution: Experience Manager
title: Videospeler
topic: Dynamic media
uuid: d7431a7b-6078-45d6-a364-434b3b44ecf4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Videospeler{#video-player}

De videospeler is het rechthoekige gebied waar de video-inhoud wordt weergegeven in de viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Als de afmetingen van de video die wordt afgespeeld niet overeenkomen met de afmetingen van de videospeler, wordt de video-inhoud gecentreerd in het rechthoekige weergavegebied van de videospeler.

De volgende CSS-klassenkiezer bepaalt de weergave van de videospeler:

```
.s7mixedmediaviewer .s7videoplayer
```

**CSS-eigenschappen van de videospeler**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> De achtergrondkleur van de videospeler. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het foutbericht dat wordt weergegeven als het systeem de video niet kan afspelen, kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

Voorbeeld - De videospeler transparant maken:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Bijschriften worden in de interne container in de videospeler geplaatst. De positie van die container wordt gecontroleerd door gesteunde WebVTT plaatsende exploitanten. De bijschrifttekst zelf bevindt zich in die container. de stijl ervan wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**CSS-eigenschappen van bijschriften**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrond van bijschrifttekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Kleur van bijschrifttekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - Een bijschrifttekst instellen op 14-pixel lichtgrijs Arial op een halftransparante zwarte achtergrond:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

De vormgeving van de bufferanimatie wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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

Voorbeeld - Als u een bufferanimatie wilt instellen op 101 pixels breed en 29 pixels hoog:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

