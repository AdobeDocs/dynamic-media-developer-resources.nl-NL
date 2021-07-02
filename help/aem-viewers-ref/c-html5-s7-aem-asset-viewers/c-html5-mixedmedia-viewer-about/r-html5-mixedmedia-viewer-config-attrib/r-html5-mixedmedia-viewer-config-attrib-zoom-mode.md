---
description: Hiermee stelt u het type zoominteractie in.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# zoomMode{#zoommode}

Hiermee stelt u het type zoominteractie in.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continue|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Met continue  </span> vergroting kunt u in de hoofdweergave geleidelijk inzoomen terwijl u klikt, dubbeltikt of een knijpbeweging maakt. U moet expliciet uitzoomen of de zoomstatus opnieuw instellen om terug te keren naar de oorspronkelijke weergave. </p> <p> <span class="codeph"> inline  </span> maakt direct zoomen mogelijk, waarbij de ingezoomde afbeelding direct verschijnt als u de hoofdweergave op het bureaublad plaatst, of om een aanraakapparaat aan te raken en vast te houden. de oorspronkelijke staat van de afbeelding wordt automatisch hersteld wanneer u de muis uit de weergave verplaatst of uw vinger loslaat. In <span class="codeph"> inline </span>-modus worden geneste afbeeldingssets samengevoegd en weergegeven als afzonderlijke miniaturen. <span class="codeph"> auto  </span> activeert inlinemodus op desktop en continumodus op aanraakapparaten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
