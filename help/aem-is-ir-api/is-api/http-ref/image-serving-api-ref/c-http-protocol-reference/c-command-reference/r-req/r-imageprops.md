---
description: Eigenschappen van bronafbeelding. Hiermee worden de geselecteerde eigenschappen geretourneerd van het afbeeldingsbestand of het catalogusitem dat is opgegeven in het URL-pad.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
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

De HTTP-respons is cacheable met de TTL op basis van `attribute::NonImgExpiration`.

Andere opdrachten in de tekenreeks request worden genegeerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> catalogus::Anker</span> of het standaardankerpunt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogus::Verlopen</span> of de standaardtijd om te leven </p> </td> 
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
   <td> <p> <span class="codeph"> catalogus::Modifier</span> of leeg als er geen catalogusitem is </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> afbeelding. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Lijst met door komma's gescheiden namen van alle Photoshop-paden die aan deze afbeelding zijn gekoppeld </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Afbeeldingstype, kan 'CMYK', 'RGB' of 'BW' zijn (voor grijswaardenafbeeldingen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> kenmerk::PostModifier</span> of leeg als er geen catalogusitem is </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> standaardafdrukresolutie in pixels/inch </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalogus:Resolutie</span> of de standaardobjectresolutie </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Wijzigingsdatum/-tijd (van <span class="codeph"> catalogus::TimeStamp</span> of het afbeeldingsbestand) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> <span class="codeph"> catalogus::ThumbRes</span> of de standaardminiatuurresolutie </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalogus::ThumbType</span> of het standaardminiatuurtype </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Breedte van afbeelding met volledige resolutie in pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Catalogus-id waaraan de <span class="varname"> object</span> opgegeven in het pad wordt opgelost (zie <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Vertaling object-id</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
