---
description: Het veranderbare volumeregelaar verschijnt aanvankelijk als knoop die een gebruiker het geluid van de videospeler laat dempen of dempen.
seo-description: Het veranderbare volumeregelaar verschijnt aanvankelijk als knoop die een gebruiker het geluid van de videospeler laat dempen of dempen.
seo-title: Meerbaar volume
solution: Experience Manager
title: Meerbaar volume
topic: Dynamic media
uuid: d7eafff8-dd98-42e2-9d45-e291fe372d8c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---


# Mutable volume{#mutable-volume}

Het veranderbare volumeregelaar verschijnt aanvankelijk als knoop die een gebruiker het geluid van de videospeler laat dempen of dempen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wanneer een gebruiker de muis over de knop beweegt, wordt een schuifregelaar weergegeven waarmee de gebruiker het volume kan instellen. De veranderbare volumeregeling kan door CSS worden gerangschikt, worden geschilderd, en, met betrekking tot de controlebar worden geplaatst die het bevat.

De vormgeving van het veranderbare volumegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7mutablevolume
```

**CSS-eigenschappen van het veranderbare volume**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de rechterrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de veranderbare volumeregeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de veranderbare volumeregeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> De kleur van de veranderbare volumeregeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

De vormgeving van de knop dempen/dempen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

U kunt de achtergrondafbeelding voor elke knopstatus bepalen. De grootte van de knop wordt overgenomen van de grootte van de volumeregeling.

**CSS-eigenschappen van de knopafbeelding**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt zowel `state` als `selected` attribuutselecteurs, die kunnen worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen. Met name `selected='true'` komt overeen met de status &quot;muted&quot; en `selected='false'` komt overeen met de status &quot;unmuted&quot;.

Het verticale gebied van de volumebalk wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-eigenschappen van het verticale gebied van de volumebalk**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> De achtergrondkleur van het verticale volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> De breedte van het verticale volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> De hoogte van het verticale volume. </p> </td> 
  </tr> 
 </tbody> 
</table>

De track binnen verticale volumeregeling wordt bestuurd met de volgende CSS-klassenkiezers:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-eigenschappen van het verticale volumeregelaar**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> De achtergrondkleur van het verticale volumeregelaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de verticale volumeregeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de verticale volumeregeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

De verticale volumeknop wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-eigenschappen van de verticale volumeregelaar**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> Verticale volumeregelaar illustraties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de verticale volumeregelaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de verticale volumeregelaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Horizontale positie van de knop voor verticale volumeregeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie.

## Voorbeelden {#section-e8caea0a303c425a8a637c2a47c06355}

U stelt een dempknop in van 32 x 32 pixels en 6 pixels van de bovenkant naar 38 pixels van de rechterrand van de besturingsbalk. Geef een andere afbeelding weer voor elk van de vier verschillende knopstatussen, al dan niet geselecteerd.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Hieronder ziet u hoe u de volumeschuifregelaar binnen het veranderbare volumeregelaar kunt opmaken.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Hieronder ziet u hoe u de videospeler kunt aanpassen, zodat geluid tijdens het afspelen wordt uitgeschakeld. Voeg de volgende code toe aan de insluitcode van de viewer:

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

In het bovenstaande codevoorbeeld wordt het volumeniveau ingesteld op `0` in de component `mutableVolume`. Vervolgens wordt dezelfde component gedeactiveerd, zodat deze niet door de eindgebruiker kan worden gebruikt.
