---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks Beeldbewerking die op alle miniaturen wordt toegepast. Indien opgegeven in de URL, alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> moet HTTP-gecodeerd zijn als <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>, respectievelijk. </p> </td> 
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
