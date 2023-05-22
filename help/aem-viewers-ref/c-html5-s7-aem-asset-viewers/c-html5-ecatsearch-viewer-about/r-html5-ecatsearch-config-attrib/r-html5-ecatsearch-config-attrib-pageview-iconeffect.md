---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`aantal`*][, *`vervagen`*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u het <span class="codeph"> iconeffect</span> om boven op de afbeelding weer te geven wanneer de afbeelding opnieuw is ingesteld en er een actie voor interactie met de afbeelding wordt voorgesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat de <span class="codeph"> iconeffect</span> verschijnt en verschijnt opnieuw. Een waarde van <span class="codeph"> -1</span> Hiermee wordt aangegeven dat het pictogram altijd voor onbepaalde tijd opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> vervagen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de duur van de animatie voor tonen of verbergen in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee stelt u het aantal seconden in dat de <span class="codeph"> iconeffect</span> blijft volledig zichtbaar voordat deze automatisch wordt verborgen. De tijd nadat de animatie voor infaden is voltooid, maar voordat de animatie voor uitfaden wordt gestart. Een instelling van <span class="codeph"> 0</span> Hiermee schakelt u het gedrag voor automatisch verbergen uit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Optioneel.

## Standaard {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Voorbeeld {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
