---
description: Doelgegevens zoomen. Geen of meer zoomeigenschappen, die samen met de zoomviewerclient kunnen worden gebruikt.
solution: Experience Manager
title: Doelen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Doelen{#targets}

Doelgegevens zoomen. Geen of meer zoomeigenschappen, die samen met de zoomviewerclient kunnen worden gebruikt.

De server retourneert de inhoud van dit veld als reactie op `req=targets`, na het vervangen van &#39; `??`&#39; recordterminatortokens.

Er kunnen maximaal vier eigenschappen aan elk zoomdoel worden gekoppeld:

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`links,boven,breedte,hoogte`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoomdoelnummer (int); Zoomdoelen moeten opeenvolgend worden genummerd, te beginnen met 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Optioneel frame-/paginanummer voor het opgeven van een specifiek frame of specifieke pagina van een spin- of brochure-set. is standaard ingesteld op 0 indien niet gespecificeerd voor gebruik door de kijker van de spin- en brochure; genegeerd door de zoomviewer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> links, boven </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelverschuiving van de linkerbovenhoek van de afbeelding naar de linkerbovenhoek van de zoomdoelrechthoek (int, int); moet 0 of groter zijn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> breedte, hoogte </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelgrootte van de zoomdoelrechthoek (int, int); moet groter zijn dan 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Waarde tekstgegevens; kan worden gebruikt als een tekstlabel voor een zoomdoelkoppeling. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Waarde tekstgegevens; kan worden gebruikt om doel-specifieke informatie tot de cliënt, zoals een waarde SKU of heet-verbinding URL over te gaan. </p> </td> 
 </tr> 
</table>

Doel. *`num`*.rect is vereist voor elk gezoemdoel en moet een rechthoek volledig binnen het beeld specificeren. Alle andere eigenschappen zijn optioneel.

*`label`* en *`userData`* deel te nemen aan lokalisatie van tekstreeksen. Zie [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

Voor toepassingen waarbij de viewerclients voor spin- en brochure worden gebruikt, moeten de zoomdoelen worden gedefinieerd in dezelfde catalogusrecord die de afbeeldingsset definieert. Alle zoomdoeldefinities in de catalogusrecords van de leden van de afbeeldingsset worden door de viewer genegeerd.

De Dynamic Media-viewers verwachten zoomdoelen in de coördinaten van de afbeelding met volledige resolutie die al zijn aangepast met de opdrachten van `catalog::Modifier`.

## Eigenschappen {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Eigenschapsgegevens](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) waarde.

## Standaard {#section-feab29f6575e482391086a57f547543c}

Geen.

## Zie ook {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogus::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalogus::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
