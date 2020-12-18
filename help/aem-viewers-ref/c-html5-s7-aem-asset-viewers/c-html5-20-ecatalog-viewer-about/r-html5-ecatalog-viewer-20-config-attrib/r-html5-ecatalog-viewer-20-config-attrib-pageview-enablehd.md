---
description: 'null'
seo-description: 'null'
seo-title: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
topic: Dynamic media
uuid: dcfb202d-6ed8-4cb9-9254-b8dcfe99cd00
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`getal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Optimalisatie in-, beperken of uitschakelen voor apparaten waarbij <span class="codeph"> devicePixelRatio</span> groter is dan <span class="codeph"> 1</span>, dat wil zeggen apparaten met een hoge dichtheid, zoals iPhone4 en soortgelijke apparaten. Als actief dan beperkt de component de grootte van het de beeldverzoek van IS alsof het apparaat slechts een pixelverhouding van <span class="codeph"> 1 </span> had en die manier de bandbreedte vermindert. </p> <p>Zie onderstaande voorbeeld </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> getal</span></span> </p> </td> 
   <td colname="col2"> <p> Als u de limietinstelling gebruikt, schakelt de component hoge pixeldichtheid alleen in tot de opgegeven limiet. </p> <p>Zie het onderstaande voorbeeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-38b878e38caa439bb462d4fa637afdaa}

Optioneel.

## Standaard {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## Voorbeeld {#section-09433488774245d985acef6c0341ece0}

De volgende resultaten worden verwacht wanneer u dit configuratiekenmerk in de viewer gebruikt en de viewergrootte 1000 x 1000 is:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Als de setvariabele gelijk is aan </p> </th> 
   <th colname="col2" class="entry"> <p>Resultaat </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> altijd</span> </p> </td> 
   <td colname="col2"> <p>Er wordt altijd rekening gehouden met de pixeldichtheid van het scherm/apparaat. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Als de pixeldichtheid van het scherm 1 is, is de gevraagde afbeelding 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Als de pixeldichtheid van het scherm 1,5 is, is de gevraagde afbeelding 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Als de pixeldichtheid van het scherm 2 is, is de gevraagde afbeelding 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nooit</span> </p> </td> 
   <td colname="col2"> <p>Deze gebruikt altijd een pixeldichtheid van 1 en negeert de HD-mogelijkheden van het apparaat. De gevraagde afbeelding is daarom altijd 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limiet&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Een pixeldichtheid van het apparaat wordt alleen opgevraagd en weergegeven als de resulterende afbeelding onder de opgegeven limiet ligt. </p> <p>Het limietnummer wordt toegepast op de breedte of de hoogte. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Als het maximale getal 1600 is en de pixeldichtheid 1,5 is, wordt de afbeelding van 1500 x 1500 weergegeven. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Als het maximumaantal 1600 is en de pixeldichtheid 2 is, wordt de afbeelding van 1000 x 1000 weergegeven omdat de afbeelding van 2000 x 2000 de limiet overschrijdt. </p> </li> 
     </ul> </p> <p><b>Beste praktijken</b>: Het limietnummer moet worden gebruikt in combinatie met de bedrijfsinstelling voor afbeeldingen van maximale grootte. Stel het limietnummer daarom in op het maximale afbeeldingsformaat van het bedrijf. </p> </td> 
  </tr> 
 </tbody> 
</table>

