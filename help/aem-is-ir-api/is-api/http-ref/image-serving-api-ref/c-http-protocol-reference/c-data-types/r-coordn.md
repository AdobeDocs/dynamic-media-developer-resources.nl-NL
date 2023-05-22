---
description: Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# coordN{#coordn}

Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> nihil</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> nihil</span></span> </p></td> 
  <td class="stentry"> <p>coördinaatverschuiving genormaliseerd op afbeeldingsgrootte (reëel, reëel) </p></td> 
 </tr> 
</table>

Positieve waarden worden naar rechts onder verplaatst.

In veel gevallen vormt het midden van de afbeelding de positie van de verwijzing. In dit geval komt 0,0 overeen met het midden van de afbeelding, -0,5,-0,5 met de linkerbovenhoek en 0,5,0,5 met de rechterbenedenhoek.

Wordt ook gebruikt om afbeeldingsgrootten of rechthoekgrootte op te geven ten opzichte van de grootte van laag 0. In dat geval moeten de waarden groter zijn dan 0. 0 kan aangeven dat een specifieke standaardwaarde moet worden gebruikt. 1,1 geeft een grootte aan die gelijk is aan die van laag 0.
