---
title: req
description: Type aanvraag. Hier geeft u het type aanvraag op.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
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
   <td colname="col2"> <p> XML-lijst met alle elementen retourneren met een <span class="codeph"> s7:element</span> kenmerkwaarde en een lijst van alle pagina's in het fxg-document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Retourneert een XML-lijst waarvan <span class="codeph"> &lt;richtext /&gt;</span> elementen lopen over. </p> <p>Hiermee wordt een xml-lijst van <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen die overlopen voor verwerking op de client. Alleen <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen die overlopen, worden geretourneerd. De <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span> is vereist <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> kenmerk bij gebruik <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Willekeurig overlopend <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen zonder <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span> is niet vermeld. Elk <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> het element in de lijst bevat de <span class="+ topic/ph pr-d/codeph codeph"> s7:element</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>en het selectiekader van het overlopende tekstkader. De <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> kenmerk geeft de tekstindex aan in het artikel tot welke tekst in het kader kon passen. De <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> alleen van toepassing op <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen in de gevraagde FXG. De lijst bevat geen <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementen van ingesloten FXG's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,tekst|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>unieke aanvraag-id reqId </p> <p>Er wordt één eigenschap met de naam catalogRecord.exists geretourneerd. De eigenschapswaarde wordt ingesteld op "1" als het opgegeven catalogusitem voorkomt in de afbeelding of de standaardcatalogus. Als dit niet het geval is, wordt het item ingesteld op "0". req=exists verzoeken tegen de /is/content context wijst op de aanwezigheid of de afwezigheid van een gespecificeerd verslag in de statische inhoudscatalogus. </p> </td> 
  </tr> 
 </tbody> 
</table>
