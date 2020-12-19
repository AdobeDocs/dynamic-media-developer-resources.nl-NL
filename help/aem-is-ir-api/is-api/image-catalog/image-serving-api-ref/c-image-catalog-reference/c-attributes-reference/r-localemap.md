---
description: ID-vertaalkaart. Geeft de regels aan die worden gebruikt voor het omzetten van generieke afbeeldings-id's in landspecifieke id's.
seo-description: ID-vertaalkaart. Geeft de regels aan die worden gebruikt voor het omzetten van generieke afbeeldings-id's in landspecifieke id's.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# LocaleMap{#localemap}

ID-vertaalkaart. Geeft de regels aan die worden gebruikt voor het omzetten van generieke afbeeldings-id&#39;s in landspecifieke id&#39;s.

` *``*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> item</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Landinstellings-id (niet hoofdlettergevoelig). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Achtervoegsel landinstelling. </p></td> 
 </tr> 
</table>

`LocaleMap` verwijst naar een  `locId` item dat aan een willekeurig aantal items kan worden toegewezen  `locSuffix`.

Lege *`locSuffix`*-waarden zijn toegestaan. *`locSuffix`* waarden moeten worden gesorteerd in de volgorde waarin ze moeten worden doorzocht. De eerste overeenkomst wordt geretourneerd.

Met Beeldserver worden de *`locId`*-waarden doorzocht op een niet-hoofdlettergevoelige overeenkomst met de waarde `locale=` die in de aanvraag is opgegeven. Als een overeenkomst wordt gevonden, wordt de eerste gekoppelde *`locSuffix`*-waarde toegevoegd aan de oorspronkelijke catalogus-id. Als deze catalogusvermelding bestaat, wordt deze gebruikt. Als dit niet het geval is, wordt de volgende *`locSuffix`*-waarde geprobeerd. Als geen van de *`locSuffix`* waarden een catalogusingang aanpast, keert de Serving van het Beeld een fout of een standaardbeeld terug.

Een lege *`locId`* waarde past lege en onbekende `locale=` koorden aan. Hiermee kunt u een standaardregel voor onbekende landinstellingen definiëren.

Als id-omzetting is ingeschakeld, wordt deze toegepast op alle id&#39;s die verwijzen naar de afbeeldingscatalogus en de items in de catalogus met statische inhoud.

## Eigenschappen {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Een of meer items, gescheiden met |, waarbij elk item uit twee of meer door komma&#39;s gescheiden tekenreekswaarden bestaat. *`locId`* en  `locale=` worden vergeleken. Niet hoofdlettergevoelig.

## Zie ook {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Localization Support, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
