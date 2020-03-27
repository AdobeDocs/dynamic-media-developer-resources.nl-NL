---
description: Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.
seo-description: Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# coordN{#coordn}

Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> alles</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> alles</span></span> </p></td> 
  <td class="stentry"> <p>coördinaatverschuiving genormaliseerd op afbeeldingsgrootte (reëel, reëel) </p></td> 
 </tr> 
</table>

Positieve waarden worden naar rechts onder verplaatst.

In veel gevallen vormt het midden van de afbeelding de positie van de verwijzing. In dit geval komt 0,0 overeen met het midden van de afbeelding, -0,5,-0,5 met de linkerbovenhoek en 0,5,0,5 met de rechterbenedenhoek.

Wordt ook gebruikt om afbeeldingsgrootten of rechthoekgrootte op te geven ten opzichte van de grootte van laag 0. In dat geval moeten de waarden groter zijn dan 0. 0 kan aangeven dat een specifieke standaardwaarde moet worden gebruikt. 1,1 geeft een grootte aan die gelijk is aan die van laag 0.
