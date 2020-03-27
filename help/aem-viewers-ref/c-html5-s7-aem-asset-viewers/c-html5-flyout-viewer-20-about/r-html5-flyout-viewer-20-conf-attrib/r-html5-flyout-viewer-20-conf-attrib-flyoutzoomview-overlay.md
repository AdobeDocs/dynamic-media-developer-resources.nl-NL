---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de vormgeving van de hooglichten van de hoofdweergave wanneer de flyout actief is. Wanneer ingesteld op <span class="codeph"> 0</span>, wordt het gebied dat momenteel zichtbaar is in het vervolgvenster gemarkeerd met stijlen die worden geboden door CSS-klassennamen <span class="codeph"> .s7highlight</span> of <span class="codeph"> .s7cursor</span> (afhankelijk van de waarde van de optie voor de <span class="codeph"> markeringsmodus</span> ). Wanneer ingesteld op <span class="codeph"> 1</span> wordt de modus Omgekeerd geactiveerd waarbij het momenteel weergegeven gebied volledig transparant is (voor het geval de <span class="codeph"> markeringsmodus</span> is ingesteld op <span class="codeph"> markeren</span>) of is opgemaakt met de CSS-klassenaam <span class="codeph"> .s7cursor</span> (voor het geval de markeringsmodus <span class="codeph"></span> <span class="codeph"></span><span class="codeph"></span> is ingesteld op de  cursor), maar het omliggende gebied wordt gevuld met behulp van de .s7overlayCSS-klassenaam. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
