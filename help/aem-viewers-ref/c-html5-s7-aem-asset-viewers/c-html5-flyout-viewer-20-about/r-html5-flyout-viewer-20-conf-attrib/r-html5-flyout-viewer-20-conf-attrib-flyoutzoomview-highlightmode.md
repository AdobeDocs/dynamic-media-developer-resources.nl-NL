---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markering|cursor </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type navigatieframe op dat u wilt gebruiken. Wanneer ingesteld op <span class="codeph"> cursor </span>gebruikt de component een referentiecursor met een vaste grootte. Het is mogelijk dat u verschillende cursorillustraties gebruikt voor desktopsystemen en aanraakapparaten. Deze mogelijkheid wordt geregeld met <span class="codeph"> .s7cursor </span> CSS-klasse en <span class="codeph"> input=mouse|touch </span> kenmerkkiezer. Op desktopsystemen wordt een ankerpunt ingesteld in het midden van het cursorgebied, terwijl op aanraakapparaten het anker zich in het onderste midden van de cursor bevindt. Wanneer ingesteld op <span class="codeph"> highlight </span>gebruikt de component een navigatieframe van variabele grootte; de grootte en vorm van het frame zijn afhankelijk van de zoomfactor en de grootte van de uitvliegweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de tijd in (in seconden) waarin de markering of de cursor moet infaden nadat deze door de gebruiker is geactiveerd. Infaden wordt alleen toegepast op aanraakapparaten. op desktopsystemen wordt deze genegeerd door de component. </p> <p>Infaden is van toepassing op de volgende UI-elementen: markeringskader, vaste cursor, bedekking (voor het geval dat <span class="codeph"> bedekking </span> parameter is ingesteld op <span class="codeph"> 1 </span>). Animaties in de Flyout-weergave beginnen pas nadat de animatie voor het vervagen van de markering/cursor is voltooid. Er is geen animatie voor uitfaden. Wanneer de gebruiker de vervolgkeuzelijst deactiveert, worden de bijbehorende UI-elementen (cursor, markering en bedekking) direct verborgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Bepaalt de positie van navigatieframes. </p> <p>Indien ingesteld op <span class="codeph"> onimage </span>kan het navigatieframe alleen worden geplaatst binnen het daadwerkelijke afbeeldingsgebied in de hoofdweergave. </p> <p>Indien ingesteld op <span class="codeph"> vrij </span> een gebruiker kan het navigatieframe overal in het logische hoofdweergavegebied verplaatsen, zelfs buiten de afbeeldingsinhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
