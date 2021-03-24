---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---


# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks voor Beeldbewerking die wordt toegepast op de pagina-afbeelding. Indien opgegeven in de URL moeten alle exemplaren van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als <span class="codeph"> %26</span> respectievelijk <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
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
