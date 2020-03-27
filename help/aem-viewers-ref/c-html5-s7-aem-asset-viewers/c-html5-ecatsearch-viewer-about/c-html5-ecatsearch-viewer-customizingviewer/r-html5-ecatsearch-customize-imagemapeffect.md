---
description: Afhankelijk van de waarde van de wijzeparameter, toont de kijker de pictogrammen van de beeldkaart over de belangrijkste mening op plaatsen waar de kaarten oorspronkelijk in het Publiceren Scene7 Systeem worden ontworpen of geeft nauwkeurige gebieden terug die de vorm van originele beeldkaarten aanpassen.
seo-description: Afhankelijk van de waarde van de wijzeparameter, toont de kijker de pictogrammen van de beeldkaart over de belangrijkste mening op plaatsen waar de kaarten oorspronkelijk in het Publiceren Scene7 Systeem worden ontworpen of geeft nauwkeurige gebieden terug die de vorm van originele beeldkaarten aanpassen.
seo-title: Afbeeldingskaart, effect
solution: Experience Manager
title: Afbeeldingskaart, effect
topic: Dynamic media
uuid: 8bafaec3-500c-4a1f-b511-bff125daab7f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Afbeeldingskaart, effect{#image-map-effect}

Afhankelijk van de waarde van de wijzeparameter, toont de kijker de pictogrammen van de beeldkaart over de belangrijkste mening op plaatsen waar de kaarten oorspronkelijk in het Publiceren Scene7 Systeem worden ontworpen of geeft nauwkeurige gebieden terug die de vorm van originele beeldkaarten aanpassen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het afbeeldingskaartpictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>De `s7mapoverlay` CSS-klasse die in het verleden is gebruikt om afbeeldingskaartpictogrammen op te maken, is nu afgekeurd. in `s7icon` plaats daarvan gebruiken.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Pictogramafbeeldingskaart, illustraties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van afbeeldingskaart in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte afbeeldingskaart in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het pictogram Afbeeldingskaart ondersteunt de `state` kenmerkkiezer, die u kunt gebruiken om verschillende skins toe te passen op de pictogramstatussen `default` en `active`.

Voorbeeld: stel een pictogram voor een afbeelding met hyperlinks van 28 x 28 pixels in en geef een andere afbeelding weer voor elk van de twee verschillende pictogramstaten.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Zie ook Ondersteuning voor [afbeeldingen met hyperlinks](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

De vormgeving van het gebied met afbeeldingskaart wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p> Vulkleur van gebied Afbeeldingskaart. </p> <p>Opgegeven in de indeling #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Vulkleur van gebied Afbeeldingskaart. </p> <p>Opgegeven in de indeling #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Randstijl van afbeeldingskaart. </p> <p>Opgegeven als <span class="codeph"><span class="varname"> effen </span> kleur <span class="varname"> </span> , waarbij de </span><span class="codeph"> <span class="varname"> </span> </span> <span class="codeph"> <span class="varname"> </span> </span> breedte wordt uitgedrukt in pixels en  kleur wordt ingesteld als #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een transparant gebied voor een afbeeldingskaart in met een zwarte pixelrand: `1`

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

