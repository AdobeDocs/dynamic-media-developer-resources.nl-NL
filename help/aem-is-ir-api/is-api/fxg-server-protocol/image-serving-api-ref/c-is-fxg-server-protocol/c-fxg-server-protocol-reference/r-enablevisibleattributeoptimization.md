---
description: Hiermee wordt de optimalisatie van FXG ingeschakeld.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Hiermee wordt de optimalisatie van FXG ingeschakeld.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Verwijdert de elementen waarvan de zichtbaarheid is ingesteld op false in FXG terwijl deze FXG wordt doorgegeven, waardoor de verwerkingstijd van FXG afneemt. Hoewel alleen die elementen met zichtbaarheid als false worden verwijderd die geen invloed hebben op andere elementen in FXG. Als er bijvoorbeeld tekst is ingeschakeld `Path` en zichtbaarheid van `Path` is ingesteld op false, wordt deze niet verwijderd uit FXG, zelfs niet als deze optie is ingeschakeld, omdat tekst op dit pad moet worden getekend.

De standaardwaarde is 1.
