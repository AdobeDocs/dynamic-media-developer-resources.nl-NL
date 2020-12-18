---
description: Versie afbeelding/metagegevens. Wanneer het werken met inhoud die regelmatig verandert, kunnen de servers in caching netwerken zoals Akamai, browser caches, en collectieve de servergeheime voorgeheugens van de volmachtsserver van het Beeld antwoorden opslaan die verouderd kunnen zijn voor periodes.
seo-description: Versie afbeelding/metagegevens. Wanneer het werken met inhoud die regelmatig verandert, kunnen de servers in caching netwerken zoals Akamai, browser caches, en collectieve de servergeheime voorgeheugens van de volmachtsserver van het Beeld antwoorden opslaan die verouderd kunnen zijn voor periodes.
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# id{#id}

Versie afbeelding/metagegevens. Wanneer het werken met inhoud die regelmatig verandert, kunnen de servers in caching netwerken zoals Akamai, browser caches, en collectieve de servergeheime voorgeheugens van de volmachtsserver van het Beeld antwoorden opslaan die verouderd kunnen zijn voor periodes.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versietekenreeks. </p> </td> 
 </tr> 
</table>

De Server van het beeld omvat een versieringsmechanisme dat kan helpen de kans verminderen dat een verouderd geheim voorgeheugeningang door een toepassing wordt gebruikt. Dit mechanisme omvat het gebruik van `req=props` om versie-id-tekenreeksen te verkrijgen voor afbeeldingsgegevens en metagegevens (zoals afbeeldingskaart of zoomdoelgegevens). De versie-id-tekenreeks wordt vervolgens met de opdracht `id=` toegevoegd aan cacheable Image Serving-aanvragen.

Wanneer een bronafbeelding of metagegevens worden gewijzigd, verandert ook de bijbehorende versie-id-waarde. Als u een up-to-date versie-id-waarde opneemt met de opdracht `id=`, bent u ervan verzekerd dat oude cachemarkeringen niet langer worden geopend.

In de volgende tabel worden de tekenreeks met de versie-id weergegeven die voor elk type `req=` moet worden gebruikt:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> versie-id van req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> map </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> masker </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> streefdoelen </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> gebruikersgegevens </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` typen die niet hierboven zijn vermeld, hebben een korte TTL (  `attribute::NonImgExpiration`) of de reacties zijn helemaal niet in de cache te plaatsen; het heeft geen enkel voordeel  `id=` bij dergelijke verzoeken te worden betrokken .

## Eigenschappen {#section-62e973d0d5884abebbb0679f9278ae2c}

Request-kenmerk. Optioneel. Altijd genegeerd door de server.

## Standaard {#section-96136720c82842c89505347ec39e6024}

Geen.

## Voorbeeld {#section-a5fb871e0ec8485c91c4fca78895d17f}

Zie de beschrijving van [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) bijvoorbeeld gebruik.

## Zie ook {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [kenmerk::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
