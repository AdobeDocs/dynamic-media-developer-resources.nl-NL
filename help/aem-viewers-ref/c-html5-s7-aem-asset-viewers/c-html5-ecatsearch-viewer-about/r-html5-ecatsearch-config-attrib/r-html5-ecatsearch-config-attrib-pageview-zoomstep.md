---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic Media
uuid: 27eb2a48-008b-455e-9a03-41bb4030271b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> stap</span></span> </p> </td> 
   <td colname="col2"> <p> Vormt het aantal acties voor inzoomen en uitzoomen die nodig zijn om de resolutie met een factor twee te verhogen of te verlagen. De resolutie voor elke zoomactie wordt 2^1 per stap gewijzigd. Stel in op <span class="codeph"> 0</span> om te zoomen naar volledige resolutie met één zoomactie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limiet</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de maximale zoomresolutie in ten opzichte van de afbeelding met volledige resolutie. De standaardwaarde is <span class="codeph"> 1.0</span>, die het zoomen voorbij volledige resolutie niet toestaat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-636d35a4791447039f1902973f568320}

Optioneel.

## Standaard {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Voorbeeld {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
