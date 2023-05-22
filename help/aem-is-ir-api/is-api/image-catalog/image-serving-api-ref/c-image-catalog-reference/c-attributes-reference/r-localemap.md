---
description: ID-vertaalkaart. Geeft de regels aan die worden gebruikt voor het omzetten van generieke afbeeldings-id's in landspecifieke id's.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# LocaleMap{#localemap}

ID-vertaalkaart. Geeft de regels aan die worden gebruikt voor het omzetten van generieke afbeeldings-id&#39;s in landspecifieke id&#39;s.

`*`item`*&#42;['|' *`item`*]`

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

`LocaleMap` verwijst naar een `locId` die kunnen worden toegewezen aan een willekeurig aantal `locSuffix`.

Leeg *`locSuffix`* waarden zijn toegestaan. *`locSuffix`* waarden moeten worden gesorteerd in de volgorde waarin ze moeten worden doorzocht. De eerste overeenkomst wordt geretourneerd.

Beeldserver zoekt de *`locId`* waarden voor een niet-hoofdlettergevoelig overeenkomend met de `locale=` in de aanvraag opgegeven waarde. Als er een overeenkomst wordt gevonden, wordt de eerste koppeling *`locSuffix`* wordt toegevoegd aan de oorspronkelijke catalogus-id. Als dit catalogusitem bestaat, wordt het gebruikt, anders de volgende *`locSuffix`* waarde wordt geprobeerd. Indien geen van de *`locSuffix`* De waarden komen overeen met een item in een catalogus, de afbeeldingsserver retourneert een fout of een standaardafbeelding.

Een leeg *`locId`* waarde komt overeen met leeg en onbekend `locale=` tekenreeksen. Hiermee kunt u een standaardregel voor onbekende landinstellingen definiëren.

Als id-omzetting is ingeschakeld, wordt deze toegepast op alle id&#39;s die verwijzen naar de afbeeldingscatalogus en de items in de catalogus met statische inhoud.

## Eigenschappen {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Een of meer items, gescheiden met |, waarbij elk item uit twee of meer door komma&#39;s gescheiden tekenreekswaarden bestaat. *`locId`* en `locale=` worden vergeleken. Niet hoofdlettergevoelig.

## Zie ook {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Ondersteuning voor lokalisatie, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [kenmerk:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
