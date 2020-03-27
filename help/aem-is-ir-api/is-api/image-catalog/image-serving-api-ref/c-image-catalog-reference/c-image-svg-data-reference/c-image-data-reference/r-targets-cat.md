---
description: Doelgegevens zoomen. Geen of meer zoomeigenschappen, die samen met de zoomviewerclient kunnen worden gebruikt.
seo-description: Doelgegevens zoomen. Geen of meer zoomeigenschappen, die samen met de zoomviewerclient kunnen worden gebruikt.
seo-title: Doelen
solution: Experience Manager
title: Doelen
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Doelen{#targets}

Doelgegevens zoomen. Geen of meer zoomeigenschappen, die samen met de zoomviewerclient kunnen worden gebruikt.

De server retourneert de inhoud van dit veld als reactie op `req=targets`, na het vervangen van &#39; `??`&#39;-recordterminatortokens.

Er kunnen maximaal vier eigenschappen aan elk zoomdoel worden gekoppeld:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span></span> </p> </td> 
  <td class="stentry"> <p>Zoomdoelnummer (int); Zoomdoelen moeten opeenvolgend worden genummerd, te beginnen met 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span></span> </p> </td> 
  <td class="stentry"> <p>Optioneel frame-/paginanummer voor het opgeven van een specifiek frame of specifieke pagina van een spin- of brochure-set. is standaard ingesteld op 0 indien niet gespecificeerd voor gebruik door de kijker van de spin- en brochure; genegeerd door de zoomviewer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> links, boven </span></span> </p> </td> 
  <td class="stentry"> <p>Pixelverschuiving van de linkerbovenhoek van de afbeelding naar de linkerbovenhoek van de zoomdoelrechthoek (int, int); moet 0 of groter zijn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> breedte, hoogte </span></span> </p> </td> 
  <td class="stentry"> <p>Pixelgrootte van de zoomdoelrechthoek (int, int); moet groter zijn dan 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span></span> </p> </td> 
  <td class="stentry"> <p>Waarde tekstgegevens; kan worden gebruikt als een tekstlabel voor een zoomdoelkoppeling. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> gebruikersgegevens </span></span> </p> </td> 
  <td class="stentry"> <p>Waarde tekstgegevens; kan worden gebruikt om doel-specifieke informatie tot de cliënt, zoals een waarde SKU of heet-verbinding URL over te gaan. </p> </td> 
 </tr> 
</table>

Doel. *`num`*.rect is vereist voor elk gezoemdoel en moet een rechthoek volledig binnen het beeld specificeren. Alle andere eigenschappen zijn optioneel.

*`label`* en deel *`userData`* aan de lokalisatie van teksttekenreeksen. Zie Tekstreeks lokaliseren [in de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) HTTP-protocolreferentie ** voor meer informatie.

Voor toepassingen waarbij de viewerclients voor spin- en brochure worden gebruikt, moeten de zoomdoelen worden gedefinieerd in dezelfde catalogusrecord die de afbeeldingsset definieert. Alle zoomdoeldefinities in de catalogusrecords van de leden van de afbeeldingsset worden door de viewer genegeerd.

De kijkers Scene7 verwachten gezoemdoelstellingen in de coördinaten van het volledig-resolutiebeeld dat reeds door de bevelen van `catalog::Modifier`. wordt aangepast.

## Eigenschappen {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Waarde van eigenschappengegevens](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) .

## Standaard {#section-feab29f6575e482391086a57f547543c}

Geen.

## Zie ook {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
