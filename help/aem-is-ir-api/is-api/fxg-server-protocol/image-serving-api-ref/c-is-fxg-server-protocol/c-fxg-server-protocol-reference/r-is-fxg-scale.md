---
description: Afbeelding schalen. Hiermee schaalt u een afbeelding met factor ten opzichte van de afbeelding met volledige resolutie.
seo-description: Afbeelding schalen. Hiermee schaalt u een afbeelding met factor ten opzichte van de afbeelding met volledige resolutie.
seo-title: schalen
solution: Experience Manager
title: schalen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---


# scale{#scale}

Afbeelding schalen. Hiermee schaalt u een afbeelding met factor ten opzichte van de afbeelding met volledige resolutie.

`scale= *`factor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> factor</span></span> </p> </td> 
  <td class="stentry"> <p>Schaalfactor (reëel, &gt;0). </p></td> 
 </tr> 
</table>

## Standaard {#section-e9e53959b35844579f0f1d7721b71f8e}

Als deze optie niet is opgegeven, wordt de afbeelding gebruikt zonder schalen.

## Voorbeeld {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
