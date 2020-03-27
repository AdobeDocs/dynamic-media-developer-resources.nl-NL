---
description: 'null'
seo-description: 'null'
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 3192d810-fb30-44ae-9939-98e890c76e5c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`

Hiermee bepaalt u de vormgeving van de component wanneer een element `PageView.frametransition` is ingesteld op `turn` of is ingesteld op `auto` desktopsystemen.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> De breedte in pixels van de scheidingsschaduw van de pagina die de linker- en rechterpagina in de spread scheidt. Het bepaalt ook de breedte van de lopende schaduw die naast de het draaien pagina wordt getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> De schaduwkleur in RRGGBB-indeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>De schaduwdekking in het bereik van <span class="codeph"> 0</span> tot en met <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> De markering ( <span class="codeph"> 0</span> of <span class="codeph"> 1</span>) waarmee de rand om de pagina voor uitzetten wordt in- en uitgeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> De randkleur in RRGGBB-indeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> De kleur van de effen vulling van het componentgebied dat wordt gebruikt tijdens een animatie bij omslaan van pagina, in RRGGBB-indeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-54c634116cfe4f17813318e07539264c}

Optioneel.

## Standaard {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Voorbeelden {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
