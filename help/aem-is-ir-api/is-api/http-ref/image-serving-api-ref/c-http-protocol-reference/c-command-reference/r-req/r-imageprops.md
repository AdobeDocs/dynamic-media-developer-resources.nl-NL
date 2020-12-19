---
description: Eigenschappen van bronafbeelding. Hiermee worden de geselecteerde eigenschappen geretourneerd van het afbeeldingsbestand of het catalogusitem dat is opgegeven in het URL-pad.
seo-description: Eigenschappen van bronafbeelding. Hiermee worden de geselecteerde eigenschappen geretourneerd van het afbeeldingsbestand of het catalogusitem dat is opgegeven in het URL-pad.
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# imageprops{#imageprops}

Eigenschappen van bronafbeelding. Hiermee worden de geselecteerde eigenschappen geretourneerd van het afbeeldingsbestand of het catalogusitem dat is opgegeven in het URL-pad.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

De reactie van HTTP is cacheable met TTL die op `attribute::NonImgExpiration` wordt gebaseerd.

Andere opdrachten in de tekenreeks request worden genegeerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

De volgende eigenschappen worden geretourneerd:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschap</b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Beschrijving</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> Anker of standaardankerpunt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> Verlopen of de standaardtijd om te leven </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Hoogte van afbeelding met volledige resolutie in pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Naam/beschrijving van het profiel dat aan deze afbeelding is gekoppeld </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> afbeelding. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 als het gekoppelde profiel is ingesloten in de afbeelding </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 als de afbeelding Photoshop-padgegevens bevat </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> afbeelding. embeddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 als de afbeelding XMP gegevens bevat </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 voor geen masker, 1 voor vooraf vermenigvuldigde alfa, 2 voor niet-vooraf vermenigvuldigde alfa en 3 voor een afzonderlijke maskerafbeelding </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> Wijzigen of leeg als geen catalogusitem is </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> afbeelding. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Lijst met door komma's gescheiden namen van alle Photoshop-paden die aan deze afbeelding zijn gekoppeld </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Afbeeldingstype, mogelijk 'CMYK', 'RGB' of 'BW' (voor grijswaardenafbeeldingen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> kenmerk::</span> PostModifier of leeg als er geen item uit de catalogus is </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> standaardafdrukresolutie in pixels/inch </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> Resolutie of de resolutie van het standaardobject </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Wijzigingsdatum/-tijd (uit catalogus <span class="codeph">::TimeStamp</span> of het afbeeldingsbestand) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> ThumbResor de standaardminiatuurresolutie </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalogus::</span> ThumbType of het standaardminiatuurtype </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Breedte van afbeelding met volledige resolutie in pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Catalogus-id waarnaar het object <span class="varname"></span> dat in het pad is opgegeven, wordt omgezet (zie <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Vertaling object-id</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>

