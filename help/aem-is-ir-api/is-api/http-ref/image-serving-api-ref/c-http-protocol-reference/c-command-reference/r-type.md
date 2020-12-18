---
description: Statisch inhoudstype, filter. Geeft een filtertekenreeks op voor statische inhoud die wordt geleverd via /is/content.
seo-description: Statisch inhoudstype, filter. Geeft een filtertekenreeks op voor statische inhoud die wordt geleverd via /is/content.
seo-title: type
solution: Experience Manager
title: type
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '123'
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

De server zal val met de waarde van `catalog::Type` van het gevraagde statische inhoudspunt vergelijken. Het item wordt geretourneerd aan de client als de waarden overeenkomen (hoofdlettergevoelig). Als dit niet het geval is, wordt een fout geretourneerd.

## Eigenschappen {#section-529b088434a44a9f86a64ef548d2925b}

Alleen ondersteund voor aanvragen voor statische inhoud (niet-afbeeldingsbestanden) via. Wordt genegeerd als `catalog::Type` leeg is of niet is gedefinieerd.

## Standaard {#section-e9e8f51d0a01452183ccb510efd87d46}

Er wordt geen overeenkomend type toegepast als `type=` niet is opgegeven of leeg is.

## Zie ook {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Statische inhoud](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da) (niet-afbeeldingsbestanden) wordt geleverd,  [catalogus::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
