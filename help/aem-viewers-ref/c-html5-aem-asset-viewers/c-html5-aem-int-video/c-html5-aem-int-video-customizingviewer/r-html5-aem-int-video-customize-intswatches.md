---
description: Het interactieve deelvenster Stalen wordt naast de video-inhoud weergegeven als interactieve gegevens in configuratie zijn doorgegeven aan de viewer. Het bestaat uit een banner bovenaan die tekst zoals "Klik om te bekijken", een kolom van één of meerdere interactieve monsters en twee rolknopen (beschikbaar slechts op Desktopsystemen) teruggeeft.
seo-description: Het interactieve deelvenster Stalen wordt naast de video-inhoud weergegeven als interactieve gegevens in configuratie zijn doorgegeven aan de viewer. Het bestaat uit een banner bovenaan die tekst zoals "Klik om te bekijken", een kolom van één of meerdere interactieve monsters en twee rolknopen (beschikbaar slechts op Desktopsystemen) teruggeeft.
seo-title: Interactieve stalen
solution: Experience Manager
title: Interactieve stalen
topic: Dynamic media
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---


# Interactieve stalen{#interactive-swatches}

Het interactieve deelvenster Stalen wordt naast de video-inhoud weergegeven als interactieve gegevens in configuratie zijn doorgegeven aan de viewer. Het bestaat uit een banner bovenaan die tekst zoals &quot;Klik om te bekijken&quot;, een kolom van één of meerdere interactieve monsters en twee rolknopen (beschikbaar slechts op Desktopsystemen) teruggeeft.

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Op desktopsystemen en op aanraakapparaten worden interactieve stalen in liggende richting verticaal rechts van de video-inhoud gerenderd. Op aanraakapparaten met een staande oriëntatie worden deze onder aan de viewer weergegeven als een horizontale rij stalen.

De volgende CSS-klassenkiezer bepaalt de locatie en richting van het interactieve deelvenster Stalen:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS-eigenschappen van de interactieve stalen {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van het interactieve deelvenster Stalen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van het interactieve deelvenster Stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Bovenste positie van het interactieve deelvenster Stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>De onderste positie van het interactieve deelvenster Stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Linkerpositie van het interactieve deelvenster Stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>De rechterpositie van het interactieve deelvenster Stalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

De locatie en richting van het interactieve deelvenster Stalen tijdens runtime worden als volgt gedefinieerd door een combinatie van de bovenstaande CSS-eigenschappen:

* Als u interactieve stalen horizontaal wilt renderen onder aan de viewer, stelt u de hoogte in op een absolute pixelwaarde. van links naar beneden naar 0 px; breedte, rechts en van boven naar automatisch.
* Als u interactieve stalen verticaal wilt renderen rechts van de video-inhoud, stelt u de breedte in op een absolute pixel. rechts en boven naar 0 px; hoogte, links en onder naar automatisch.

U kunt CSS-markeringen in combinatie met deze stijl gebruiken om het interactieve deelvenster Stalen op een aangepaste manier te plaatsen.

## Voorbeeld {#example}

Een interactief deelvenster Stalen instellen om de weergave horizontaal onder aan de viewer op aanraakapparaten te vergroten in de stand Liggend en in alle andere gevallen verticaal rechts van de video-inhoud weer te geven:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De grootte en positie van de banner worden beheerd door de interactieve staalcomponent op basis van andere stijlen die met CSS zijn toegepast en kunnen niet expliciet worden ingesteld.

De volgende CSS-klassenkiezer bepaalt de vormgeving van het bannerpaneel:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## CSS-eigenschappen van het paneel banner {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van het bannerpaneel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur in het bannerpaneel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand rond het bannerpaneel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>De tekendikte die voor de tekst in het bannerpaneel moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>De tekengrootte die voor de tekst in het bannerpaneel moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>De lettertypefamilie die voor de tekst in het bannerpaneel moet worden gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>De lettertypeuitlijning die moet worden gebruikt voor de tekst in het bannerpaneel. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knopinfo voor de banner kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

Als u een banner wilt instellen met een donkergrijze achtergrond, lichtere grijze rand van twee pixels en de witte tekst horizontaal gecentreerd:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

De volgende CSS-klassenkiezer bepaalt de weergave van de stalen:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## CSS-eigenschappen van het staalgebied {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van het gebied Stalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-9cadd62a09fd44a280f55ff42437e416}

Stalen instellen met donkergrijze achtergrond:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

De volgende CSS-klassenkiezer bepaalt de afstand tussen staalminiaturen:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS-eigenschappen van de tussenruimte tussen miniaturen van stalen {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de horizontale en verticale marge rond elke miniatuur. De werkelijke miniatuurspatiëring is gelijk aan de som van de linker- en rechtermarge die is ingesteld voor <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-39fb270b7e494a9d99e6e8f6890ec53c}

De verticale afstand instellen op 10 pixels:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

De volgende CSS-klassenkiezer bepaalt de weergave van afzonderlijke miniaturen:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS-eigenschappen van de weergave van afzonderlijke miniaturen {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand van de miniatuur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatuur ondersteunt de kenmerkenkiezer `state`, die u kunt gebruiken om verschillende skins toe te passen op verschillende miniatuurtoestanden. Met name `state="selected"` komt overeen met de miniatuur van de geselecteerde afbeelding; `state="default"` komt overeen met de overige miniaturen; `state="over"` wordt gebruikt bij de muisaanwijzer.

## Voorbeeld {#section-69fec189ffaa440b97b6b846c320b75b}

Miniaturen van 100 x 75 pixels instellen:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

De volgende CSS-klassenkiezer bepaalt de vormgeving van het miniatuurlabel:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS-eigenschappen van de weergave van het miniatuurlabel {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand Label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Horizontale tekstuitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-eb141eb6c1154183baa69796edb90536}

Als u labels wilt instellen voor links uitgelijnd, wit en 12 pixels in het Helvetica-lettertype en een onderrand:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Met de volgende CSS-klassenkiezer bepaalt u de vormgeving van de schuifknoppen Omhoog en Omlaag:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Het is niet mogelijk om de rolknopen te plaatsen gebruikend CSS `top`, `left`, `bottom`, en `right` eigenschappen; in plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

## CSS-eigenschappen van de weergave van de schuifknoppen Omhoog en Omlaag {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>De positie binnen de sprite van de illustratie, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die u kunt gebruiken om verschillende huiden op de knoopstaten toe te passen: &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; en &quot; `disabled`&quot;.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

## Voorbeeld {#section-e6ce4fa084b84288bc7583342b2c510c}

Als u een schuifknop van 60 x 36 pixels wilt instellen, hebt u voor elke staat een andere illustratie en haalt u die illustratie uit de sprite-afbeelding van de component:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

