---
description: Genormaliseerde grootte. Wordt gebruikt om afbeeldingsgrootten of rechthoekgrootten op te geven, genormaliseerd ten opzichte van de grootte van laag 0 of een andere afbeelding.
seo-description: Genormaliseerde grootte. Wordt gebruikt om afbeeldingsgrootten of rechthoekgrootten op te geven, genormaliseerd ten opzichte van de grootte van laag 0 of een andere afbeelding.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Genormaliseerde grootte. Wordt gebruikt om afbeeldingsgrootten of rechthoekgrootten op te geven, genormaliseerd ten opzichte van de grootte van laag 0 of een andere afbeelding.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>genormaliseerde breedte en hoogte ten opzichte van een andere afbeelding (echt, echt, groter dan 0) </p></td> 
 </tr> 
</table>

Zowel *nx* als *ny* moeten groter zijn dan 0. 0,0 kan erop wijzen dat een specifieke standaardgrootte moet worden gebruikt. 1,1 geeft een grootte aan die gelijk is aan de referentieafbeelding.
