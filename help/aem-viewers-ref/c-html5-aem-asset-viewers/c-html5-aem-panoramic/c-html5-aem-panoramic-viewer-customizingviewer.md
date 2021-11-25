---
title: Panoramische viewer aanpassen
description: Alle visuele aanpassingen en de meeste gedragsaanpassingen voor de Panoramische Viewer worden uitgevoerd door een aangepaste CSS te maken.
keywords: responsief
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Video360 Viewer aanpassen{#customizing-video-viewer}

Alle visuele aanpassingen en de meeste gedragsaanpassingen worden gedaan door een aangepaste CSS te creëren.

De voorgestelde workflow is om het standaard CSS-bestand voor de juiste viewer te gebruiken, het naar een andere locatie te kopiëren, het aan te passen en de locatie van het aangepaste bestand op te geven in het `style=` gebruiken.

Standaard CSS-bestanden vindt u op de volgende locatie:

`<s7viewers_root>/html5/PanoramicViewer.css`

Aangepast CSS-bestand moet dezelfde klassedeclaraties bevatten als het standaardbestand. Als een klassendeclaratie wordt weggelaten, werkt de viewer niet correct omdat deze geen ingebouwde standaardstijlen voor gebruikersinterface-elementen biedt.

Een andere manier om aangepaste CSS-regels te bieden, is door ingesloten stijlen rechtstreeks op de webpagina of in een van gekoppelde externe CSS-regels te gebruiken.

Houd er bij het maken van aangepaste CSS rekening mee dat de viewer `.s7panoramicviewer` -klasse aan het DOM-containerelement. Als u een extern CSS-bestand gebruikt dat wordt doorgegeven met `style=` gebruiken `.s7panoramicviewer` klasse als bovenliggende klasse in afstammende kiezer voor uw CSS-regels. Als u ingesloten stijlen op de webpagina uitvoert, kwalificeert u deze kiezer als volgt aanvullend met een id van het DOM-containerelement:

`#<containerId>.s7panoramicviewer.`


## Algemene opmaakopmerkingen en advies {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alle paden naar externe elementen in CSS worden omgezet op de CSS-locatie, niet op de locatie van de HTML-pagina van de viewer. Hiermee houdt u rekening wanneer u de standaard-CSS naar een andere locatie kopieert: het kan nodig zijn om de standaardelementen ook te kopiëren of paden in de aangepaste CSS bij te werken.
* U kunt verschillende indelingen gebruiken voor kleurwaarden die worden ondersteund door CSS. Indien transparantie nodig is, `rgba(R,G,B,A)` wordt aanbevolen. Anders is transparantie niet vereist `#RRGGBB` kan worden gebruikt.

Wanneer u de gebruikersinterface van de viewer aanpast met CSS, kunt u `!IMPORTANT` regel wordt niet ondersteund voor het opmaken van viewerelementen. Met name: `!IMPORTANT` Deze regel mag niet worden gebruikt om standaardstijlen of runtimestijlen die door de viewer of Viewer SDK worden geboden, te negeren, omdat dit van invloed kan zijn op het gedrag van de juiste componenten. In plaats daarvan moeten CSS-kiezers met de juiste specificiteit worden gebruikt om CSS-eigenschappen in te stellen die in deze naslaggids worden beschreven.

## Panoramische Viewer CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Hoofdviewergebied**
Het hoofdweergavegebied is het gebied dat wordt ingenomen door de panorama-afbeelding.  Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.

De vormgeving van het weergavegebied wordt bepaald door de CSS-klassenkiezer:
`.s7panoramicviewer`

Toepasselijke CSS-eigenschappen zijn onder andere:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> de breedte van de kijker; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> de hoogte van de kijker; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: Een viewer instellen met een grootte van 1024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Panoramische weergave**
De hoofdweergave bestaat uit het panorama.

De vormgeving van de hoofdweergave wordt bepaald door de CSS-klassenkiezer:
`.s7panoramicviewer .s7panoramicview`

Toepasselijke CSS-eigenschappen zijn onder andere:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> de achtergrondkleur van de hoofdweergave; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: De hoofdweergave transparant maken:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
