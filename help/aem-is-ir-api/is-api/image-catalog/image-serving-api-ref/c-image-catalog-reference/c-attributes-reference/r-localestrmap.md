---
description: Tekenreeksvertaalkaart. Verwijst naar een locId die aan om het even welk aantal internalLocId kan worden in kaart gebracht.
seo-description: Tekenreeksvertaalkaart. Verwijst naar een locId die aan om het even welk aantal internalLocId kan worden in kaart gebracht.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# LocaleStrMap{#localestrmap}

Tekenreeksvertaalkaart. Verwijst naar een locId die aan om het even welk aantal internalLocId kan worden in kaart gebracht.

` *``*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item  </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> landinstelling  </span> </p> </td> 
  <td class="stentry"> <p>Landinstelling (niet hoofdlettergevoelig). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>Interne landinstellings-id. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` verwijst naar een  `locId` item dat aan een willekeurig aantal items kan worden toegewezen  `internalLocId`.

Een lege *`locale`* waarde past lege en onbekende `locale=` koorden aan. Hiermee kunt u een standaardregel voor onbekende landinstellingen definiëren.

Lege *`locId`* waarden zijn toegestaan en selecteer *`defaultString`* (*`defaultString`* heeft geen landinstellings-id). *`locId`* waarden worden doorzocht in de opgegeven volgorde. De eerste overeenkomst wordt geretourneerd.

Wanneer Tekenreeksomzetting is ingeschakeld, wordt deze toegepast op tekstreeksen in de volgende afbeeldingscatalogusvelden:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Catalogusveld</b> </td> 
   <td> <b>Tekenreekselement in veld</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::ImageSet  </span> </p> </td> 
   <td> <p>Een subelement dat een vertaalbare tekenreeks bevat (gescheiden door een combinatie van scheidingstekens ',' ';' ':' en/of het begin/einde van het veld). </p> <p>Een <span class="codeph"> 0xrrggbb </span> kleurwaarde aan het begin van een lokaliseerbaar veld wordt uitgesloten van lokalisatie en wordt ongewijzigd doorgegeven. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::Kaart  </span> </p> </td> 
   <td> <p>Een enkele of dubbele kenmerkwaarde, behalve de waarden van de <span class="codeph"> coördins= </span> en <span class="codeph"> shape= </span> attributen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::doelen  </span> </p> </td> 
   <td> <p>De waarde van een <span class="filepath">-doel.*.label </span> en <span class="filepath"> doel.*.userdata </span> property. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::UserData  </span> </p> </td> 
   <td> <p>De waarde van een eigenschap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8505a8525f6948ada3979f68c4081044}

Een of meer items, gescheiden met |, waarbij elk item uit twee of meer door komma&#39;s gescheiden tekenreekswaarden bestaat.

## Zie ook {#section-0c0516e4f83d42d38247308cab9b6708}

Ondersteuning voor lokalisatie, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), &lt;a10/&lt;catalog::UserData 11/>[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
