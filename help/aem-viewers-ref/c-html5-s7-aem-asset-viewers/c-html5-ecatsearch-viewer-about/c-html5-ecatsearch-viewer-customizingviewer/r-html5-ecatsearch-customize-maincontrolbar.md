---
title: Hoofdbesturingsbalk
description: De hoofdbesturingsbalk is het rechthoekige gebied op desktopsystemen en tablets dat alle besturingselementen voor de gebruikersinterface bevat (behalve knoppen voor grote pagina) die beschikbaar zijn voor de eCatalog Search-viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Hoofdbesturingsbalk{#main-control-bar}

De hoofdbesturingsbalk is het rechthoekige gebied op desktopsystemen en tablets dat alle besturingselementen voor de gebruikersinterface bevat (behalve knoppen voor grote pagina) die beschikbaar zijn voor de eCatalog Search-viewer.

Op mobiele telefoons blijven de knoppen Miniaturen, Inhoudsopgave, Downloaden, Afdrukken, Favorieten, Delen via sociale media, Volledig scherm en Sluiten behouden. De knoppen Eerste pagina en Laatste pagina en Pagina-indicator worden echter verwijderd van de hoofdbesturingsbalk en in plaats daarvan toegevoegd aan de secundaire besturingsbalk. Standaard wordt de hoofdbesturingsbalk boven in het viewergebied weergegeven op desktopsystemen en mobiele telefoons en op tablets naar de onderkant van het viewergebied verplaatst. De viewerbreedte neemt altijd de volledige beschikbare viewerbreedte in beslag. Het is mogelijk de kleur, hoogte en verticale positie in de CSS te wijzigen ten opzichte van de viewercontainer.

De vormgeving van de hoofdbesturingsbalk wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Positie boven aan de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Positie onder aan de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de hoofdbesturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van de hoofdbesturingsbalk. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - om een grijze hoofdbesturingsbalk in te stellen die 36 pixels hoog is en boven aan de viewercontainer wordt geplaatst.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

De hoofdbesturingsbalk ondersteunt een optionele schuiffunctie. Deze wordt geactiveerd als de viewerbreedte te klein is en er onvoldoende ruimte is voor alle knoppen die zijn ingesteld op de besturingsbalk. In dit geval wordt een pijlknop met twee statussen weergegeven aan de rechterkant van de besturingsbalk. Wanneer u op deze knop klikt of erop tikt, worden alle besturingsbalkelementen naar links of naar rechts geschoven, afhankelijk van de status van de schuifknop. Het belangrijkste gebruiksgeval voor deze functie is mobiele apparaten met kleine schermen met een staande oriëntatie.

De scrolleigenschap wordt toegelaten voor de belangrijkste controlebar, en is gehandicapt voor de secundaire controlebar. De functie wordt in- en uitgeschakeld met de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> positie </span> </p> </td> 
   <td colname="col2"> <p>Wanneer ingesteld op <span class="codeph"> static </span> de schuiffunctie is uitgeschakeld. </p> <p>Deze eigenschap instellen op <span class="codeph"> absoluut </span> om de schuiffunctie in te schakelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

De rolknoop wordt toegevoegd aan een speciaal containerelement dat de knoop behoorlijk plaatst. Hiermee kunt u het gebied rondom de knop anders opmaken dan de rest van de besturingsbalk als de hoogte van de schuifknop kleiner is dan de hoogte van de besturingsbalk.

De vormgeving van deze schuifknopcontainer wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normaal gesproken moet deze gelijk zijn aan of groter zijn dan de breedte van de schuifknop zelf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur container. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt de schuifknop zelf groter of kleiner maken met behulp van CSS.

De vormgeving van deze knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
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
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` en `selected` kenmerkkiezers, die kunnen worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden. Met name: `state="selected"` komt overeen met de oorspronkelijke toestand van de schuifknop wanneer u naar links door de inhoud van de schuifbalk kunt schuiven. De `state="default"` komt overeen met de status wanneer de inhoud helemaal naar links wordt geschoven en de schuifknop stelt voor de inhoud naar de begintoestand te retourneren.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

**Voorbeeld** - De schuiffunctie in de hoofdbesturingsbalk voor mobiele telefoons inschakelen. Stel een schuifknop in van 64 x 64 pixels waarmee een andere afbeelding wordt weergegeven voor elk van de vier verschillende knopstatussen, al dan niet geselecteerd:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
