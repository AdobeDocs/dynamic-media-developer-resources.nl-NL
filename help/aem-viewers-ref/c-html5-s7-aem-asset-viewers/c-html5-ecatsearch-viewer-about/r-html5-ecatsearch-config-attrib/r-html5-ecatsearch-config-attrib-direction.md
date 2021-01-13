---
description: richting
solution: Experience Manager
title: richting
topic: Dynamic media
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u hoe pagina's worden weergegeven in de hoofdweergave en in de miniaturen. Hiermee bepaalt u ook hoe de gebruiker communiceert met de gebruikersinterface van de viewer om te schakelen tussen catalogusframes. </p> <p>Als <span class="codeph"> links </span> wordt gebruikt, wordt een uitlijning naar rechts ingesteld voor de eerste pagina en de uitlijning naar links voor de laatste pagina. Subafbeeldingen van afzonderlijke pagina's worden met elkaar verbonden voor de rendervolgorde van links naar rechts. De hoofdweergave wordt ook ingesteld om diaanimatie van rechts naar links te gebruiken om de catalogus te vervroegen (voor het geval <span class="codeph"> PageView.frametransition </span> is ingesteld op dia). Tot slot worden miniaturen ingesteld voor een opvulvolgorde van links naar rechts. </p> <p>Als <span class="codeph"> rechts </span> wordt gebruikt, wordt de linkeruitlijning voor de eerste pagina en de rechteruitlijning voor de laatste pagina ingesteld. Subafbeeldingen van afzonderlijke pagina's worden met elkaar verbonden voor de rendervolgorde van rechts naar links. De hoofdweergave wordt ook ingesteld om diaanimatie van links naar rechts te gebruiken om de catalogus te vervroegen (voor het geval <span class="codeph"> PageView.frametransition </span> is ingesteld op dia). Tot slot wordt de volgorde van de miniaturen omgekeerd, zodat de weergave van de miniaturen van rechts naar links en van boven naar beneden wordt gevuld. </p> <p>Wanneer <span class="codeph"> auto </span> wordt geplaatst, past de kijker <span class="codeph"> juiste </span> wijze toe wanneer scène aan <span class="codeph"> ja wordt geplaatst; </span>anders wordt <span class="codeph"> linker </span> modus gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optioneel.

## Standaard {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Voorbeeld {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
