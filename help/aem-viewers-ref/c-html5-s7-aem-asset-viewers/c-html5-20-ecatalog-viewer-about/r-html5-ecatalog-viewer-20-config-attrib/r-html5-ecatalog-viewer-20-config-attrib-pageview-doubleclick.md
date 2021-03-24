---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van dubbelklikken/tikken voor zoomacties. Als u instelt op <span class="codeph"> Geen </span>, wordt dubbelklikken/tikken uitgeschakeld. Indien ingesteld op <span class="codeph"> zoomen </span> klikken op de afbeelding, zoomt u in één zoomstap. Met CTRL en klikken zoomt u één zoomstap uit. Als u <span class="codeph"> reset </span> instelt, wordt met één klik op de afbeelding de zoomwaarde opnieuw ingesteld op het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span> wordt opnieuw ingesteld als de huidige zoomfactor op of buiten de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Optioneel.

## Standaard {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` op desktopcomputers;  `zoomReset` op aanraakapparaten.

## Voorbeeld {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
