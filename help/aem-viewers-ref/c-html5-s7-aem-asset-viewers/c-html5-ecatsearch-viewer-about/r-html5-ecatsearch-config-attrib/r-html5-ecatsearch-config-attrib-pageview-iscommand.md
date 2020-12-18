---
description: 'null'
seo-description: 'null'
seo-title: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic media
uuid: 32bfd041-e44c-4a78-a923-896a85d8f75f
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '59'
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
