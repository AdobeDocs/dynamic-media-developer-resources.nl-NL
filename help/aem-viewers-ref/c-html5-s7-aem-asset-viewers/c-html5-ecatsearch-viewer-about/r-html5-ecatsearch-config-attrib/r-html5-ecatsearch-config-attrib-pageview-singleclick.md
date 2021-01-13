---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van één klik of tik voor zoomacties. Als u instelt op <span class="codeph"> Geen </span>, wordt zoomen met één klik/tikken uitgeschakeld. Indien ingesteld op <span class="codeph"> zoomen </span> klikken op de afbeelding, zoomt u in één zoomstap. Met CTRL en klikken zoomt u één zoomstap uit. Als u <span class="codeph"> reset </span> instelt, wordt met één klik op de afbeelding de zoomwaarde opnieuw ingesteld op het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span> wordt opnieuw ingesteld als de huidige zoomfactor op of buiten de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-edcfcd6c0bd24ac093442c56450b3c97}

Optioneel.

## Standaard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] op desktopcomputers;  [!DNL `none`] op aanraakapparaten.

## Voorbeeld {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]