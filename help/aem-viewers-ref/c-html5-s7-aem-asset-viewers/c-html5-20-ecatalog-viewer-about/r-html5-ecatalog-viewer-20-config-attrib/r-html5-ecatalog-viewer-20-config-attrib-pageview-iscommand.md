---
title: PageView.iscommand
description: PageView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d1b05fe7-901b-4030-9b71-e4e0e5191abf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks voor Beeldbewerking die wordt toegepast op de pagina-afbeelding. Indien opgegeven in de URL, alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> moet HTTP-gecodeerd zijn als <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>, respectievelijk. </p> <p> <p>Opmerking: Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-df5a0604766b4ac2b9a6742b377e427c}

Optioneel.

## Standaard {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Geen.

## Voorbeeld {#section-813de2905d6c44c0991cfe0931581462}

Wanneer opgegeven in de URL van de viewer.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Indien opgegeven in de configuratiegegevens.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
