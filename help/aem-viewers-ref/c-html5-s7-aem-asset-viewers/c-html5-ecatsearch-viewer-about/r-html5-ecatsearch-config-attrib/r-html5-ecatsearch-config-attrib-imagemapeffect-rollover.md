---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan wanneer het deelvenster Info moet worden weergegeven. </p> <p>Indien ingesteld op <span class="codeph"> 1</span>, wordt het deelvenster Info weergegeven wanneer de muis het gebied van de afbeeldingskaart binnenkomt (voor het geval de afbeelding met hyperlinks niet leeg is), <span class="codeph"> rollover_key</span> kenmerk). </p> <p>Indien ingesteld op <span class="codeph"> 0</span>, wordt het deelvenster Info geactiveerd wanneer de afbeeldingskaart is geselecteerd (als de afbeeldingskaart een niet-lege afbeelding bevat <span class="codeph"> rollover_key</span> en leeg <span class="codeph"> href</span> kenmerken). </p> <p> Wordt genegeerd op aanraakapparaten, zoals desktopsystemen met aanraakbediening, en wordt automatisch ingesteld op <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-ccfedc2da28f412a86d03f390db92b4b}

Optioneel.

## Standaard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Voorbeeld {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
