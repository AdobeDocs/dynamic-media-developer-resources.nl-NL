---
title: richting
description: Hiermee bepaalt u hoe pagina's worden weergegeven in de hoofdweergave en in de miniaturen. Hiermee bepaalt u ook hoe de gebruiker communiceert met de gebruikersinterface van de viewer om te schakelen tussen catalogusframes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# richting{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u hoe pagina's worden weergegeven in de hoofdweergave en in de miniaturen. Hiermee bepaalt u ook hoe de gebruiker communiceert met de gebruikersinterface van de viewer om te schakelen tussen catalogusframes. </p> <p>Wanneer <span class="codeph"> left </span> wordt gebruikt, wordt een uitlijning naar rechts ingesteld voor de eerste pagina en een uitlijning naar links voor de laatste pagina. Subafbeeldingen van afzonderlijke pagina's worden in de volgorde van links naar rechts geplaatst. De hoofdweergave wordt ook ingesteld om diaanimatie van rechts naar links te gebruiken om de catalogus te vervroegen (voor het geval dat <span class="codeph"> PageView.frametransition </span> is ingesteld op dia). Tot slot worden miniaturen ingesteld voor een opvulvolgorde van links naar rechts. </p> <p>En wanneer <span class="codeph"> right </span> wordt gebruikt, wordt de linkeruitlijning voor de eerste pagina ingesteld en de rechteruitlijning voor de laatste pagina. Subafbeeldingen van afzonderlijke pagina's worden met elkaar verbonden voor de rendervolgorde van rechts naar links. De hoofdweergave wordt ook ingesteld om diaanimatie van links naar rechts te gebruiken om de catalogus te vervroegen (voor het geval dat <span class="codeph"> PageView.frametransition </span> is ingesteld op dia). Tot slot wordt de volgorde van de miniaturen omgekeerd, zodat de weergave van de miniaturen van rechts naar links en van boven naar beneden wordt gevuld. </p> <p>Wanneer <span class="codeph"> auto </span> is ingesteld, wordt de viewer toegepast <span class="codeph"> right </span> modus wanneer landinstelling is ingesteld op <span class="codeph"> ja; </span>anders gebruikt het <span class="codeph"> left </span> in. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optioneel.

## Standaard {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Voorbeeld {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
