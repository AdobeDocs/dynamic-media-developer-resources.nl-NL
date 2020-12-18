---
description: JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.
seo-description: JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# qlt{#qlt}

JPEG-kwaliteit. Hiermee geeft u JPEG-coderingskenmerken op om het compressieniveau te bepalen. Dit varieert op zijn beurt de bestandsgrootte (de hoeveelheid antwoordgegevens) en indirect de visuele kwaliteit van de resulterende afbeelding.

` qlt= *``*[, *`kwalitatief chroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kwaliteit  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-coderingskwaliteit (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>downsampling van JPEG-chromaticiteit (0=normaal, 1=uitgeschakeld); optioneel, standaard is 0. </p> </td> 
 </tr> 
</table>

Wordt alleen gebruikt als `fmt=jpg`. Anders genegeerd

Bij hogere waarden voor kwaliteit neemt de bestandsgrootte en de kwaliteit toe, bij lagere waarden neemt de bestandsgrootte af en neemt de waargenomen afbeeldingskwaliteit af. Met waarden boven 90 worden vaak afbeeldingen gegenereerd die niet van de ongecomprimeerde afbeelding zijn te onderscheiden.

Stel de markering `chroma` in om de downsampling van RGB-chromaticiteit in JPEG-coders uit te schakelen. Hierdoor kan de waargenomen scherpte van de randen in een afbeelding toenemen wanneer de rand wordt gedefinieerd door een wijziging in kleurtoon in plaats van helderheid. Als u deze markering instelt, kan de bestandsgrootte enigszins toenemen. Experimenteer met deze instelling als de tekst iets vaag lijkt.

`chroma` wordt genegeerd als het uitvoerpixeltype CMYK of grijs is.

## Voorbeeld {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
