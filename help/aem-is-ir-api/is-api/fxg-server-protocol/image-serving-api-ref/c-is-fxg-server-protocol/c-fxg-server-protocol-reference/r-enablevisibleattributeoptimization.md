---
description: Hiermee wordt de optimalisatie van FXG ingeschakeld.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Hiermee wordt de optimalisatie van FXG ingeschakeld.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Verwijdert de elementen waarvan de zichtbaarheid is ingesteld op false in FXG terwijl deze FXG wordt doorgegeven, waardoor de verwerkingstijd van FXG afneemt. Hoewel alleen die elementen met zichtbaarheid als false worden verwijderd die geen invloed hebben op andere elementen in FXG. Als er bijvoorbeeld tekst staat op `Path` en de zichtbaarheid van `Path` is ingesteld op false, wordt deze niet verwijderd uit FXG, zelfs niet als deze optie is ingeschakeld, omdat tekst op dit pad moet worden getekend.

De standaardwaarde is 1.
