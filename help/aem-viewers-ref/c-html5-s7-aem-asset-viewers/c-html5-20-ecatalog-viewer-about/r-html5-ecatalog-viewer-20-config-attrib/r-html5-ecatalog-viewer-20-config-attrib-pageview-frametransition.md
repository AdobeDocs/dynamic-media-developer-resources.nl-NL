---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duur`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dia|draaien|auto</span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type effect op dat wordt toegepast op de framewijziging. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Hiermee </span> deactiveert u een overgang waarin het oude frame uit beeld schuift en het nieuwe frame naar buiten schuift. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Hiermee </span> schakelt u een pagina-spiegeleffect in wanneer een gebruiker een van de vier spreadhoeken kan slepen en een interactieve pagina-omdraaiing kan uitvoeren. </p> <p>Wanneer <span class="codeph"> draai</span> wordt gebruikt, wordt de vormgeving van de component bepaald met de <span class="codeph"> pageturnstyle</span> modifier en wordt de CSS-klasse <span class="codeph"> .s7pagedivider</span> genegeerd. </p> <p>Opmerking:  <p><span class="codeph"> Omdraaianimatie wordt niet ondersteund op Motorola Xoom. </span>  </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> Hiermee </span> wordt de overgang van het draaiframe op desktopsystemen en de diaovergang op aanraakapparaten automatisch ingesteld. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p>Geeft de duur in seconden aan van een <span class="codeph"> dia</span> of <span class="codeph"> draai</span> overgangseffect. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optioneel.

## Standaard {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Voorbeeld {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
