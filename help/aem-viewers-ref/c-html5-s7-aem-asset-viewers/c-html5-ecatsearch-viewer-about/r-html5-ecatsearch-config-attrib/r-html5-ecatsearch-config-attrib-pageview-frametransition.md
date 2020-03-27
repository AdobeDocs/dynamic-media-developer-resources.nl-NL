---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duur`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dia|draaien|auto</span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type effect op dat wordt toegepast op de framewijziging. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> dia</span> activeert een overgang waar het oude kader uit mening glijdt en het nieuwe kader binnen aan mening glijdt. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> draai</span> maakt het mogelijk om een pagina om te draaien wanneer een gebruiker een van de vier spreadhoeken kan slepen en een interactieve pagina omdraait. </p> <p>Wanneer <span class="codeph"> draai</span> wordt gebruikt, wordt de vormgeving van de component gecontroleerd met de <span class="codeph"> pageturnstyle</span> modifier en wordt de CSS-klasse <span class="codeph"> .s7pagedivider</span> genegeerd. </p> <p>Opmerking:  <p><span class="codeph"> draai</span> animatie wordt niet ondersteund op Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> stelt de omwentelingsframeovergang in op desktopsystemen en de diaovergang op aanraakapparaten. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de duur in seconden van een overgangseffect voor een <span class="codeph"> dia</span> of <span class="codeph"> draai</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optioneel.

## Standaard {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Voorbeeld {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
