---
title: Videoscrubber
description: De videoscrubber is de horizontale schuifregelaar waarmee een gebruiker dynamisch naar een willekeurige tijdpositie in de video kan zoeken die momenteel wordt afgespeeld.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9f7e3fec-8303-4114-86b2-fb75d041701d
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Videoscrubber{#video-scrubber}

De videoscrubber is de horizontale schuifregelaar waarmee een gebruiker dynamisch naar een willekeurige tijdpositie in de video kan zoeken die momenteel wordt afgespeeld.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De scrubber &#39;knob&#39; beweegt zich ook terwijl de video speelt om op de huidige tijdpositie van de video tijdens playback te wijzen. De videoscrubber neemt altijd de volledige breedte van de controlebar. Het is mogelijk de skin van de videoscrubber te wijzigen, de hoogte en de verticale positie te wijzigen met CSS.

De algemene weergave van de videoscrubber wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7smartcropvideoviewer .s7videoscrubber 
.s7smartcropvideoviewer .s7videoscrubber .s7videotime 
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**CSS-eigenschappen van de videoscrubber**

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
   <td colname="col2"> <p>Hoogte van de videoscrubber. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De kleur van de videoscrubber. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassekiezers volgen de indicatoren voor achtergrond, afspelen en laden:

```
.s7smartcropvideoviewer .s7videoscrubber .s7track 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed
```

**CSS-eigenschappen van de track**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de desbetreffende track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De kleur van de bijbehorende track. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassenkiezer bestuurt de knop:

```
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**CSS-eigenschappen van de knop**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Verticale knopverschuiving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Illustraties uitnemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassenkiezer bestuurt de zeepbel waarin de tijd wordt afgespeeld:

```
.s7smartcropvideoviewer .s7videoscrubber .s7videotime
```

**CSS-eigenschappen van de afgespeelde bel**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> De lettertypefamilie die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p> De tekengrootte die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p> De lettertypekleur die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Bubble artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>De uitlijning van tekst met het bellengebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knopinfo voor het gereedschap Video scrubber kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie .

**Voorbeeld** - Een videoviewer instellen met een videoscrubber met aangepaste trackkleuren van tien pixels hoog. En tenslotte, laat het 10 pixel en 35 pixel van de bovenkant en linkerranden van de controlebar worden geplaatst.

```
.s7smartcropvideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
