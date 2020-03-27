---
description: Het deelvenster Oproepen naar actie wordt weergegeven wanneer de video wordt beëindigd en alle interactieve stalen worden weergegeven die aan de specifieke video zijn gekoppeld.
seo-description: Het deelvenster Oproepen naar actie wordt weergegeven wanneer de video wordt beëindigd en alle interactieve stalen worden weergegeven die aan de specifieke video zijn gekoppeld.
seo-title: Oproep tot actie
solution: Experience Manager
title: Oproep tot actie
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Oproep tot actie{#call-to-action}

Het deelvenster Oproepen naar actie wordt weergegeven wanneer de video wordt beëindigd en alle interactieve stalen worden weergegeven die aan de specifieke video zijn gekoppeld.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Het deelvenster bestaat uit een koptekstgebied met de titel van de video, een knop voor het opnieuw afspelen in de rechterbovenhoek en de interactieve stalen die daadwerkelijk als een schuifbaar raster worden weergegeven. U kunt het paneel onbruikbaar maken gebruikend het [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) configuratiekenmerk.

Het aanroepen van het deelvenster Handelingen neemt altijd het volledige beschikbare viewergebied.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Met de volgende CSS-klassenkiezer bepaalt u de weergave van de achtergrondkleur in het aanroepen van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction
```

## CSS-eigenschappen van de achtergrondkleur van de aanroep van het deelvenster Handelingen {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van de aanroep van het deelvenster Handelingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example}

Een aanroep van een handelingspaneel met donkergrijze achtergrond instellen:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Met de volgende CSS-klassenkiezer bepaalt u de weergave van de koptekst in het aanroepen van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## CSS-eigenschappen van de aanroep naar de koptekst van het deelvenster Handelingen {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de koptekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de koptekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Onderrand van de koptekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-1}

Een koptekst instellen die 70 pixels hoog is, met een donkergrijze achtergrond en een iets lichtere grijze rand van twee pixels langs de onderkant:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

De volgende CSS-klassenkiezer bepaalt de weergave van de koptekst in de aanroep van het handelingspaneel:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## CSS-eigenschappen van de kopteksttitel in het actiepaneel:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p> Tekstkleur in de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte </span> </p> </td> 
   <td colname="col2"> <p>Lijnhoogte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>De uitlijning van tekst in de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-links </span> </p> </td> 
   <td colname="col2"> <p>Opvulling links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvulling rechts </span> </p> </td> 
   <td colname="col2"> <p> Opvulling rechts om ruimte toe te staan voor de knop Opnieuw afspelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-2}

U stelt als volgt een titel van een video in met een regelhoogte van 70 pixels, een tekengrootte van 25 pixels, een witte kleur en een links uitgelijnde tekst:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

De volgende CSS-klassenkiezer bepaalt de vormgeving van de sluitknop in de aanroep van het handelingspaneel:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## CSS-eigenschappen van de knop close in de aanroep van het deelvenster Handelingen: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenkant van de koptekst, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Positie rechts van de koptekst, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Afbeelding weergegeven voor een bepaalde knopstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Plaats binnen de illustratie-sprite als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

## Voorbeeld {#example-3}

Een afspeelknop van 28 x 28 pixels instellen; geplaatst op 20 pixels van de bovenkant en vanaf de rechterrand van de koptekst; geeft een andere afbeelding weer voor elk van de vier verschillende knoptoestanden; neemt het kunstwerk van SPRITE van de component beeld:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

Met de volgende CSS-klassenkiezer bepaalt u de weergave van het miniatuurraster in de aanroep van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## CSS-eigenschappen van de weergave van het miniatuurraster in het aanroepen van het deelvenster Handelingen:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van het gebied met miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-4}

Een miniatuurgebied met een donkergrijze achtergrond instellen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Met de volgende CSS-klassenkiezer bepaalt u de vormgeving van de blokcel in de aanroep van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## CSS-eigenschappen van de minicel in de aanroep van het deelvenster Handelingen: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Grootte van de horizontale en verticale marge rond elke miniatuur. </p> <p>De werkelijke horizontale miniatuurafstand is gelijk aan de som van de linker- en rechtermarge die is ingesteld voor de miniatuur <span class="codeph"> .s7 </span>. Dezelfde regel geldt ook, maar voor verticale afstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-5}

Zo stelt u de horizontale afstand in van 24 pixels en de verticale afstand van 18 pixels:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

De volgende CSS-klassenkiezer bepaalt de weergave van de miniatuur in het aanroepen van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## CSS-eigenschappen van de miniatuur in de aanroep van het deelvenster Handelingen: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand van de miniatuur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De miniatuur ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. komt met name overeen met `state="selected"` de miniatuur van de momenteel geselecteerde afbeelding; komt overeen `state="default"` met de overige miniaturen; wordt `state="over"` gebruikt bij de muisaanwijzer.

## Voorbeeld {#example-6}

Miniaturen van 94 x 100 pixels instellen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

De volgende CSS-klassenkiezer bepaalt de vormgeving van het miniatuurlabel in het aanroepen van het handelingenvenster:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## CSS-eigenschappen van het label van de miniatuur in de oproep naar het deelvenster Handelingen: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p> Tekstkleur van label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale uitlijning van label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-7}

Als u labels wilt instellen die een witte kleur gebruiken, moet u 15 pixels gecentreerd zijn en een Arial-lettertype gebruiken:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Als er meer miniaturen zijn dan verticaal in de weergave passen, wordt aan de rechterkant een verticale schuifbalk weergegeven. Standaard wordt met het aanroepen van het deelvenster Handelingen een kleine verticale balk zonder blokje en schuifknoppen weergegeven. Het is echter mogelijk de balk aan te passen door de CSS van de viewer te wijzigen.

De volgende CSS-klassenkiezer bepaalt de vormgeving van het gebied van de schuifbalk in het aanroepen van het deelvenster Handelingen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## CSS-eigenschappen van het gebied van de schuifbalk in het aanroepen van het deelvenster Handelingen: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breedte van schuifbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Verticale verschuiving van de schuifbalk ten opzichte van de bovenkant van het gebied met miniaturen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Verticale verschuiving van de schuifbalk ten opzichte van de onderkant van het gebied met miniaturen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> De horizontale verschuiving van de schuifbalk ten opzichte van de rechterrand van het gebied met miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-8}

Als u een schuifbalk wilt instellen die 22 pixels breed is en geen marge heeft vanaf de bovenkant, de rechterkant of de onderkant van het miniatuurgebied:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

Het schuifbalkvak is het gebied tussen de bovenste en onderste schuifbalkknoppen. De component stelt automatisch de positie en de hoogte van het spoor in.

De volgende CSS-klassenkiezer bepaalt de weergave van het schuifbalkvak in het aanroepen van het handelingspaneel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## CSS-eigenschappen van de schuifbalk {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van schuifbalk in track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van de trackbalk. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#example-9}

U stelt als volgt een schuifbalktrack in die 22 pixels breed is en een grijze kleur heeft:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Het schuifbalkblokje beweegt verticaal binnen het gebied van het schuifvak. De verticale positie ervan wordt volledig bepaald door de componentlogica; de hoogte van het blokje verandert echter niet dynamisch, afhankelijk van de hoeveelheid inhoud.

De volgende CSS-klassenkiezer bepaalt de vormgeving van de duimhoogte en andere aspecten:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## CSS-eigenschappen van de hoogte van het blokje in het aanroepen van het deelvenster Handelingen: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen boven </span> </p> </td> 
   <td colname="col2"> <p>Verticale opvulling tussen de bovenkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-onder </span> </p> </td> 
   <td colname="col2"> <p>Verticale opvulling tussen de onderkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Straal van de rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Kleur van duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> Afbeelding die wordt weergegeven voor een bepaalde blokje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De duim steunt de `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op de volgende verschillende duimstaten toe te passen: `"up"`, `"down"`, `"over"`en `"disabled"`.

## Voorbeeld {#example-10}

Als u een schuifbalkblokje van 6 x 167 pixels wilt instellen, hebt u drie afgeronde hoeken van pixels en een grijze kleur:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

Met de volgende CSS-klassenkiezer bepaalt u de vormgeving van de bovenste en onderste schuifknoppen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Het is niet mogelijk om schuifknoppen te positioneren met de CSS-eigenschappen top, left, bottom of right. de viewerlogica plaatst ze automatisch. Het actiepaneel in de interactieve videoviewer gebruikt deze knoppen in de schuifbalk niet en hun grootte wordt daarom ingesteld op 0 pixels in de standaard-CSS.

## CSS-eigenschappen van de schuifknoppen boven en onder in het actiepaneel:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breedte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Afbeelding weergegeven voor een bepaalde knopstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoppen ondersteunen de `state` kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op de volgende verschillende blokstatussen: `"up"`, `"down"`, `"over"`en `"disabled"`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Voorbeeld {#example-11}

Schakel schuifknoppen uit door de grootte in te stellen op 0 en deze te verbergen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

