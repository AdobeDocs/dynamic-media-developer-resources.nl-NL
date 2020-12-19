---
description: Pas de helderheid aan. Hiermee verkleint of vermeerdert u de helderheid van de afbeelding.
seo-description: Pas de helderheid aan. Hiermee verkleint of vermeerdert u de helderheid van de afbeelding.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# op_brightness{#op-brightness}

Pas de helderheid aan. Hiermee verkleint of vermeerdert u de helderheid van de afbeelding.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Helderheidsaanpassing (-100..+100 int). </p></td> 
 </tr> 
</table>

## Eigenschappen {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Laag, opdracht. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen. CMYK-afbeeldingen of -lagen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Standaard {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, voor geen enkele wijziging van de helderheid.

## Voorbeeld {#section-c25f952f1b77409abb9ccf885862d75c}

Maak de achtergrond van een afbeelding iets donkerder om de voorgrondinhoud te benadrukken:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
