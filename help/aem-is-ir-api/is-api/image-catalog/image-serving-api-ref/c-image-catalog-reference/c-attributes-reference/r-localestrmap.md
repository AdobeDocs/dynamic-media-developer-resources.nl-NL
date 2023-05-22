---
description: Tekenreeksvertaalkaart. Verwijst naar een locId die aan om het even welk aantal internalLocId kan worden in kaart gebracht.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

Tekenreeksvertaalkaart. Verwijst naar een locId die aan om het even welk aantal internalLocId kan worden in kaart gebracht.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> landinstelling </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> landinstelling </span> </p> </td> 
  <td class="stentry"> <p>Landinstelling (niet hoofdlettergevoelig). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>Interne landinstellings-id. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` verwijst naar een `locId` die kunnen worden toegewezen aan een willekeurig aantal `internalLocId`.

Een leeg *`locale`* waarde komt overeen met leeg en onbekend `locale=` tekenreeksen. Hiermee kunt u een standaardregel voor onbekende landinstellingen definiëren.

Leeg *`locId`* waarden zijn toegestaan en selecteer de *`defaultString`* (de *`defaultString`* heeft geen landinstellings-id). *`locId`* waarden worden doorzocht in de opgegeven volgorde. De eerste overeenkomst wordt geretourneerd.

Wanneer Tekenreeksomzetting is ingeschakeld, wordt deze toegepast op tekstreeksen in de volgende afbeeldingscatalogusvelden:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Catalogusveld</b> </td> 
   <td> <b>Tekenreekselement in veld</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::ImageSet </span> </p> </td> 
   <td> <p>Een subelement dat een vertaalbare tekenreeks bevat (gescheiden door een combinatie van scheidingstekens ',' ';' ':' en/of het begin/einde van het veld). </p> <p>A <span class="codeph"> 0xrrggbb </span> kleurwaarde aan het begin van een lokaliseerbaar veld wordt niet gelokaliseerd en ongewijzigd doorgegeven. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::Kaart </span> </p> </td> 
   <td> <p>Een enkele of dubbele kenmerkwaarde, met uitzondering van de waarden van de <span class="codeph"> coördins= </span> en <span class="codeph"> shape= </span> kenmerken. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::doelen </span> </p> </td> 
   <td> <p>De waarde van <span class="filepath"> doel.*.label </span> en <span class="filepath"> doel.*.userdata </span> eigenschap. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::UserData </span> </p> </td> 
   <td> <p>De waarde van een eigenschap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8505a8525f6948ada3979f68c4081044}

Een of meer items, gescheiden met |, waarbij elk item uit twee of meer door komma&#39;s gescheiden tekenreekswaarden bestaat.

## Zie ook {#section-0c0516e4f83d42d38247308cab9b6708}

Ondersteuning voor lokalisatie, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [kenmerk:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogus::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogus::Kaart](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalogus::doelen](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogus::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
