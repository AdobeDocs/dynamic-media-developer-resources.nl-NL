---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de vormgeving van de hooglichten van de hoofdweergave wanneer de vervolgkeuzelijst actief is. Wanneer ingesteld op <span class="codeph"> 0</span>, wordt het gebied dat momenteel zichtbaar is in het vervolgvenster gemarkeerd met stijlen die worden verschaft door <span class="codeph"> .s7highlight</span> of door <span class="codeph"> .s7cursor</span> Namen van CSS-klassen (afhankelijk van de waarde van <span class="codeph"> markeringsmodus</span> modifier). Wanneer ingesteld op <span class="codeph"> 1</span> wordt de modus "Omgekeerd" geactiveerd waarbij het momenteel weergegeven gebied volledig transparant is (voor het geval <span class="codeph"> markeringsmodus</span> is ingesteld op <span class="codeph"> highlight</span>) of gestileerd met <span class="codeph"> .s7cursor</span> CSS-klassenaam (in het geval <span class="codeph"> markeringsmodus</span> is ingesteld op <span class="codeph"> cursor</span>), maar het omliggende gebied wordt gevuld met stijlen die worden geleverd door <span class="codeph"> .s7overlay</span> CSS-klassenaam. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
