---
title: coordN
description: Genormaliseerde coördinaten. Wordt gebruikt om relatieve posities binnen een afbeelding op te geven, zoals afbeeldingsverschuivingen of uitsnijdparameters, die genormaliseerd zijn voor de grootte van de afbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
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

Vaak is de referentiestand het midden van de afbeelding. In dit geval: `0,0` komt overeen met het middelpunt van de afbeelding; `-0.5,-0.5` in de linkerbovenhoek, en `0.5,0.5` in de rechterbenedenhoek.

Deze wordt ook gebruikt om de afbeeldingsgrootte of de rechthoekgrootte op te geven ten opzichte van de grootte van laag 0. In dat geval moet de waarde groter zijn dan 0. 0 kan aangeven dat een specifieke standaardwaarde moet worden gebruikt. Een waarde van `1,1` geeft een grootte aan die gelijk is aan die van laag 0.
