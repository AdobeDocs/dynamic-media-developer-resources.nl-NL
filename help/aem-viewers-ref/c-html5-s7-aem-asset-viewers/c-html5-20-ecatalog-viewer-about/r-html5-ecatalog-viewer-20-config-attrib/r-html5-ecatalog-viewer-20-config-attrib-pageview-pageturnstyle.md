---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

Hiermee wordt de vormgeving van de component bepaald wanneer een `PageView.frametransition` is ingesteld op `turn` of aan `auto` op desktopsystemen.

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
   <td colname="col2"> <p> De markering (ofwel <span class="codeph"> 0</span> of <span class="codeph"> 1</span>). Hiermee wordt de rand rondom de pagina in- en uitgeschakeld. </p> </td> 
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
