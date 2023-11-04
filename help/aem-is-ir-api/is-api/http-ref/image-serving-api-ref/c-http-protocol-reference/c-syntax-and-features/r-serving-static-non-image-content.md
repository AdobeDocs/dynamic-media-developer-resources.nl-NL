---
description: Statische (niet-afbeeldings) inhoud bedienen
solution: Experience Manager
title: Statische (niet-afbeeldings) inhoud bedienen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Statische (niet-afbeeldings) inhoud bedienen{#serving-static-non-image-content}

Beeldserver biedt een mechanisme voor het beheren van inhoud die geen afbeelding is, in catalogi en het bedienen via een aparte `context /is/content`. Het mechanisme staat voor het vormen van TTL voor elk punt afzonderlijk toe.

## Basissyntaxis {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> verzoek </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> catalogus </span>/ <span class="varname"> item </span>][? <span class="varname"> modifiers </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> poort </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogus </span> </span> </p> </td> 
  <td class="stentry"> <p>Catalogus-id. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item </span> </span> </p> </td> 
  <td class="stentry"> <p>Item-id voor statische inhoud. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifiers </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Een van de ondersteunde opdrachtnamen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Opdrachtwaarde. </p> </td> 
 </tr> 
</table>

## Overzicht van opdrachten {#section-61657a0141914053ab12038ad7e91500}

Beeldserver ondersteunt de volgende opdrachten bij /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Inhoudstype, filter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, en <span class="codeph"> req=exists </span> alleen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cachegeheugen </a> </td> 
  <td class="stentry"> <p>Hiermee wordt caching op de client uitgeschakeld. </p> </td> 
 </tr> 
</table>

## Statische inhoudscatalogi {#section-b2b8f4860fe84e528493ed704c7c5141}

Catalogi met statische inhoud zijn vergelijkbaar met catalogi met afbeeldingen, maar ondersteunen minder gegevensvelden:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Kenmerk/gegevens</b> </th> 
   <th class="entry"> <b> Notities</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::Id </span> </p> </td> 
   <td> <p> De id van de catalogusrecord voor dit statische inhouditem </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::pad </span> </p> </td> 
   <td> <p> Het bestandspad voor dit inhoudsitem </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::Verlopen </span> </p> </td> 
   <td> <p> De TTL voor dit inhoudstitem; attribute::Expiration wordt gebruikt als niet gespecificeerd of als leeg </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::TimeStamp </span> </p> </td> 
   <td> <p> Tijdstempel voor bestandswijziging; vereist wanneer validatie op basis van catalogus is ingeschakeld met kenmerk::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogus::UserData </span> </p> </td> 
   <td> <p> Optionele metagegevens gekoppeld aan dit item met statische inhoud; beschikbaar voor de client met req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> Optioneel gegevenstype; kan worden gebruikt om aanvragen voor statische inhoud te filteren met de opdracht type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Statische inhoud filteren {#section-896c37cf68bc446eb0766fb378898262}

Dit mechanisme kan ervoor zorgen dat klanten alleen inhoud ontvangen die geschikt is voor hun behoeften. Ervan uitgaande dat de statische inhoud is gecodeerd met de juiste code `catalog::UserType`waarden, kan de client de `type=` aan het verzoek. De beeldenserver vergelijkt de waarde die met `type=` aan de waarde van `catalog::UserType` en retourneert bij een onjuiste overeenkomst een fout in plaats van mogelijk onjuiste inhoud.

## Zie ook {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referentie afbeeldingscatalogus](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
