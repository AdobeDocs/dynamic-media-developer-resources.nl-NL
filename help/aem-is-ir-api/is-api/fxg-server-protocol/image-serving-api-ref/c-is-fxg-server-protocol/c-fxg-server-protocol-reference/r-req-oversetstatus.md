---
description: Type aanvraag. Hier geeft u het type aanvraag op.
seo-description: Type aanvraag. Hier geeft u het type aanvraag op.
seo-title: req
solution: Experience Manager
title: req
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# req{#req}

Type aanvraag. Hier geeft u het type aanvraag op.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Waarde </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validate</span> </p> </td> 
   <td colname="col2"> <p> Retourneert eventuele fouten met het renderen van de fxg met de opgegeven url-modifiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inhoud</span> </p> </td> 
   <td colname="col2"> <p> Retourneer de xml-lijst met alle elementen met een <span class="codeph"> s7:element</span>-kenmerkwaarde en een lijst met alle pagina's in het fxg-document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Keert de lijst van XML terug waarvan <span class="codeph"> &lt;RichText/&gt;</span> elementen overlopende zijn. </p> <p>Retourneert een XML-lijst met <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementen die overlopen voor verwerking op de client. Alleen <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementen die overlopen worden geretourneerd. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> element is een vereist  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> kenmerk bij gebruik van  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Elke overlopende <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementen zonder een <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span> wordt niet vermeld. Elk <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> element in de lijst heeft <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>, en het bounding vakje van het overlopende tekstkader. Het <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> attribuut geeft de tekstindex in het artikel aan tot welke tekst in het kader kon passen. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatus is alleen van toepassing op  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen in de gevraagde FXG. Er worden geen <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-elementen van ingesloten FXG's vermeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,tekst|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>unieke aanvraag-id reqId </p> <p>Retourneert één eigenschap met de naam catalogRecord.exists. De eigenschapswaarde wordt ingesteld op "1" als het opgegeven catalogusitem voorkomt in de afbeelding of de standaardcatalogus. Als dit niet het geval is, wordt het item ingesteld op "0". req=exists verzoeken tegen de /is/content context zullen op de aanwezigheid of de afwezigheid van een gespecificeerd verslag in de statische inhoudscatalogus wijzen. </p> </td> 
  </tr> 
 </tbody> 
</table>

