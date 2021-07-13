---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`]

Hiermee bepaalt u de vormgeving van de component wanneer een [!DNL `PageView.frametransition`] op [!DNL `turn`] of [!DNL `auto`] op desktopsystemen is ingesteld.

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
   <td colname="col2"> <p>De schaduwdekking in het bereik van <span class="codeph"> 0</span> tot <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> De vlag (of <span class="codeph"> 0</span> of <span class="codeph"> 1</span>) die de grens rond de het draaien pagina in en uit draait. </p> </td> 
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

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Voorbeelden {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
