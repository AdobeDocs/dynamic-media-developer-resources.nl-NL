---
description: De videoscrubber is de horizontale schuifregelaar waarmee een gebruiker dynamisch naar een willekeurige tijdpositie in de video kan zoeken die momenteel wordt afgespeeld.
seo-description: De videoscrubber is de horizontale schuifregelaar waarmee een gebruiker dynamisch naar een willekeurige tijdpositie in de video kan zoeken die momenteel wordt afgespeeld.
seo-title: Videoscrubber
solution: Experience Manager
title: Videoscrubber
topic: Dynamic media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---


# Video scrubber{#video-scrubber}

De videoscrubber is de horizontale schuifregelaar waarmee een gebruiker dynamisch naar een willekeurige tijdpositie in de video kan zoeken die momenteel wordt afgespeeld.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De scrubber &#39;knob&#39; beweegt zich ook terwijl de video speelt om op de huidige tijdpositie van de video tijdens playback te wijzen. De videoscrubber neemt altijd de volledige breedte van de controlebar. Het is mogelijk om de videoscrubber van een skin te voorzien. de hoogte en de verticale positie van het object wijzigen met CSS.

De algemene weergave van de videoscrubber wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-eigenschappen van de videoscrubber**

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
   <td colname="col2"> <p>Hoogte van de videoscrubber. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De kleur van de videoscrubber. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassekiezers volgen de indicatoren voor achtergrond, afspelen en laden:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**CSS-eigenschappen van de track**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de desbetreffende track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De kleur van de bijbehorende track. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassenkiezer bestuurt de knop:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-eigenschappen van de knop**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Verticale knopverschuiving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Illustraties uitnemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende CSS-klassenkiezer bestuurt de zeepbel waarin de tijd wordt afgespeeld:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**CSS-eigenschappen van de afgespeelde bel**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> De lettertypefamilie die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p> De tekengrootte die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p> De lettertypekleur die voor de tijdweergavetekst moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling van ballongebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Bubble artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>De uitlijning van tekst met het bellengebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knopinfo voor het gereedschap Video scrubber kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie.

**Voorbeeld**  - Een videoviewer instellen met een videoscrubber met aangepaste trackkleuren die 10 pixels hoog zijn en die 10 pixels en 35 pixels van de boven- en linkerrand van de besturingsbalk zijn geplaatst.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Wanneer videochaptering met de parameter `navigation` wordt toegelaten, worden de hoofdstukplaatsen getoond als tellers bovenop het video scrubberspoor.

De markering van het videohoofdstuk wordt beheerd door de volgende CSS-klassenkiezer:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**CSS-eigenschappen van de markering van het videohoofdstuk**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte markeerteken van videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte markeerteken videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Illustraties markeren voor videohoofdstukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt zowel de `state` attributenselecteur, die u kunt gebruiken om verschillende huiden op verschillende knoopstaten toe te passen. Met name `selected='default'` komt overeen met de standaardmarkeringsstatus van het videohoofdstuk en `selected='over'` wordt gebruikt wanneer de markering van het videohoofdstuk wordt geactiveerd door een muis boven of aanraakbeweging.

**Voorbeeld**  - Een hoofdstukmarkering voor video instellen van 5 x 8 pixels en een andere illustratie voor de status &quot;default&quot; en &quot;over&quot; gebruiken.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

De zeepbel van het videohoofdstuk wordt geplaatst bovenop de videokaartmarkering en toont de titel, begintijd, en beschrijving voor een bepaald hoofdstuk. U kunt de maximale breedte en verticale verschuiving ten opzichte van de videoscrubbertrack instellen. De rest wordt automatisch door de component berekend.

De ballon van het videohoofdstuk wordt gecontroleerd door de volgende CSS klassenselecteur:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**CSS-eigenschappen van de ballon van het videohoofdstuk**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max. breedte  </span> </p> </td> 
   <td colname="col2"> <p>Maximale breedte van de ballon van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Verticale verschuiving van de videoscrubbertrack. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Een ballon van een videohoofdstuk instellen die 235 pixels breed is en 8 pixels omhoog vanaf de onderkant van de videoscrubbertrack loopt.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

De hoofdstukballon van de video bestaat uit een facultatieve kopbal en inhoud. De kopbal heeft de facultatieve hoofdstukbegintijd en hoofdstuktitel.

De header wordt bestuurd door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**CSS-eigenschappen van de koptekst van de bubble van het videohoofdstuk**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de ballonkoptekst van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Binnenopvulling voor koptekst van videopunten met koptekst voor hoofdstukken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van bubbelkoptekst van videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte  </span> </p> </td> 
   <td colname="col2"> <p>De regelhoogte van de ballontekst van het videohoofdstuk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Een bubbelkoptekst van een videohoofdstuk instellen van 22 pixels hoog, een regelhoogte van 22 pixels, een horizontale marge van 12 pixels en een grijze achtergrond.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

De begintijd van het videohoofdstuk wordt bepaald door de volgende CSS-klassenkiezer:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**CSS-eigenschappen van de begintijd van het videohoofdstuk**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvulling rechts  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling tussen de begintijd en de titel van het hoofdstuk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Als u de begintijd van het hoofdstuk wilt instellen met grijs 10 pixels, laat u het Verdana-lettertype en hebt u een opvulling van 10 pixels rechts.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

De titel van het videohoofdstuk wordt bestuurd door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**CSS-eigenschappen van de titel van het videohoofdstuk**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur van titel van videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Fontdikte van titel van videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Fontgrootte van titel van videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie titel van videohoofdstuk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - U stelt een titel van een videohoofdstuk in met een wit, vet en 10-pixel Verdana-lettertype.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

De beschrijving van het videohoofdstuk wordt beheerd door de volgende CSS-klassenkiezer:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**CSS-eigenschappen van de beschrijving van het videohoofdstuk**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur van de beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Fontdikte van de beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Fontgrootte van de beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Fontfamilie van de beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte  </span> </p> </td> 
   <td colname="col2"> <p>Lijnhoogte van de beschrijving van het videohoofdstuk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Omschrijving binnenopvulling van het videohoofdstuk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Als u een beschrijving van een videohoofdstuk wilt instellen met een donkergrijs, 11-pixel Verdana-lettertype, met een lichtgrijze achtergrond; 5 pixels, lijnhoogte, 12 pixels, horizontale opvulling, 12 pixels opvulling boven en 9 pixels opvulling onder.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

De vastzetconnector onder aan de hoofdstukballon wordt bestuurd door de volgende CSS-klassenkiezer:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**CSS-eigenschappen van de wig-connector**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p>Kleur van wedge-connector. </p> <p>Gedefinieerd als <span class="codeph"> &lt;color&gt; transparant </span>, zodat alleen de kleur van de bovenrand wordt gedefinieerd en de resterende randen transparant blijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width  </span> </p> </td> 
   <td colname="col2"> <p> Breedte randaansluiting. </p> <p>Gedefinieerd als <span class="codeph"> &lt;width&gt; 0 </span>, zodat dezelfde breedte alleen voor de boven- en horizontale randen wordt gedefinieerd en de breedte van de onderrand <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee definieert u alleen een negatieve ondermarge. Deze moet dezelfde waarde hebben als <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**  - Voor het instellen van een grijze, zes-pixelvastzetconnector:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

