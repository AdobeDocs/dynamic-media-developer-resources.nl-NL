---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Hiermee configureert u de toewijzing van één klik of tik voor zoomacties. Instellen op <span class="codeph"> none </span> Hiermee schakelt u zoomen met één klik of tikken uit. Indien ingesteld op <span class="codeph"> zoomen </span> als u op de afbeelding klikt, wordt in één zoomstap ingezoomd; Met CTRL en klikken zoomt u één zoomstap uit. Instellen op <span class="codeph"> reset </span> zorgt ervoor dat een enkele klik op de afbeelding het zoomniveau terugzet naar het oorspronkelijke zoomniveau. Voor <span class="codeph"> zoomReset </span>wordt opnieuw ingesteld als de huidige zoomfactor op of boven de opgegeven limiet ligt. Zoom wordt anders toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-edcfcd6c0bd24ac093442c56450b3c97}

Optioneel.

## Standaard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` op desktopcomputers; `none` op aanraakapparaten.

## Voorbeeld {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
