---
title: zoomMode
description: Hiermee stelt u het type zoominteractie in.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# zoomMode{#zoommode}

Hiermee stelt u het type zoominteractie in.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continue|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continu </span> Hiermee schakelt u klassiek zoomen in, waarbij de afbeelding geleidelijk wordt ingezoomd terwijl u in de hoofdweergave klikt, dubbeltikt of een knijpbeweging maakt. Als u de oorspronkelijke weergave wilt herstellen, zoomt u uit of stelt u de zoomstatus opnieuw in. De klasse </p> <p> <span class="codeph"> inline </span> Hiermee kunt u direct zoomen, waarbij de ingezoomde afbeelding direct wordt weergegeven wanneer u de hoofdweergave op het bureaublad plaatst, of op een aanraakapparaat tikken en ingedrukt houden. De oorspronkelijke staat van de afbeelding wordt automatisch hersteld wanneer u de muis uit de weergave verplaatst of uw vinger loslaat. In <span class="codeph"> inline </span> geneste afbeeldingssets worden samengevoegd en weergegeven als afzonderlijke miniaturen. De klasse <span class="codeph"> auto </span> Hiermee activeert u de inlinemodus op het bureaublad en de continue modus op aanraakapparaten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
