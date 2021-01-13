---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 2%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks Beeldbewerking die op alle miniaturen wordt toegepast. Indien opgegeven in de URL moeten alle exemplaren van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als <span class="codeph"> %26</span> respectievelijk <span class="codeph"> %3D</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-df5a0604766b4ac2b9a6742b377e427c}

Optioneel.

## Standaard {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Geen.

## Voorbeeld {#section-813de2905d6c44c0991cfe0931581462}

Wanneer opgegeven in de URL van de viewer.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Indien opgegeven in de configuratiegegevens.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
