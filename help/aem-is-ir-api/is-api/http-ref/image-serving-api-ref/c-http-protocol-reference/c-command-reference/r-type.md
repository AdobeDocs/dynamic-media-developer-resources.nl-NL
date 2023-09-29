---
title: type
description: Statisch inhoudstype, filter. Geeft een filtertekenreeks op voor statische inhoud die wordt geleverd via /is/content.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# type{#type}

Statisch inhoudstype, filter. Geeft een filtertekenreeks op voor statische inhoud die wordt geleverd via /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Filtertekenreeks typen. </p></td> 
 </tr> 
</table>

De serververgelijkingen `val` met de waarde van `catalog::Type` van het gevraagde statische inhoudsitem. Het item wordt geretourneerd aan de client als de waarden overeenkomen (hoofdlettergevoelig). Als dit niet het geval is, wordt een fout geretourneerd.

## Eigenschappen {#section-529b088434a44a9f86a64ef548d2925b}

Alleen ondersteund voor aanvragen voor statische inhoud (niet-afbeeldingsbestanden) via. Genegeerd als `catalog::Type` is leeg of niet gedefinieerd.

## Standaard {#section-e9e8f51d0a01452183ccb510efd87d46}

Er wordt geen overeenkomend type toegepast als `type=` is niet opgegeven of is leeg.

## Zie ook {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Statische (niet-afbeeldings) inhoud renderen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalogus::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
