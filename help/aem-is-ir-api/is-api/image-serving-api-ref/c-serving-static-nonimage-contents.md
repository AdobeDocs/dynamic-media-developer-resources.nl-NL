---
title: Statische (niet-afbeeldings) inhoud bedienen
description: Met Afbeeldingsserver kunt u niet-afbeeldingsinhoud in catalogi beheren en deze inhoud bedienen via een aparte /is/content-context.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Statische (niet-afbeeldings) inhoud bedienen{#serving-static-non-image-contents}

Met Afbeeldingsserver kunt u niet-afbeeldingsinhoud in catalogi beheren en deze inhoud bedienen via een aparte /is/content-context.

Dit vermogen staat voor het vormen van TTL voor elk punt afzonderlijk toe.

Image Serving ondersteunt de volgende opdrachten bij [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Inhoudstype, filter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, en <span class="codeph"> req=exists </span> alleen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cachegeheugen </a> </p> </td> 
  <td class="stentry"> <p>Hiermee wordt caching op de client uitgeschakeld. </p> </td> 
 </tr> 
</table>

## Basissyntaxis {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> verzoek </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> modifiers </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> poort </span>] </span> </p> </td> 
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

## Statische inhoudscatalogi {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Catalogi met statische inhoud zijn vergelijkbaar met catalogi met afbeeldingen, maar ondersteunen minder gegevensvelden:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Kenmerk/gegevens </p> </th> 
   <th colname="col2" class="entry"> <p>Notities </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::Id </span> </p> </td> 
   <td colname="col2"> <p>De id van de catalogusrecord voor dit statische inhoudsitem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::pad </span> </p> </td> 
   <td colname="col2"> <p>Het bestandspad voor dit inhoudsitem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::Verlopen </span> </p> </td> 
   <td colname="col2"> <p>De TTL voor dit inhoudsitem; <span class="codeph"> kenmerk::Expiration </span> wordt gebruikt als niet gespecificeerd of als leeg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Tijdstempel voor bestandswijziging; is vereist als validatie op basis van catalogus is ingeschakeld met <span class="codeph"> kenmerk:CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::UserData </span> </p> </td> 
   <td colname="col2"> <p>Optionele metagegevens gekoppeld aan dit statische inhouditem; beschikbaar voor de client met <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Optioneel gegevenstype; kan worden gebruikt om aanvragen voor statische inhoud te filteren met de <span class="codeph"> type=, opdracht </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Statische inhoud filteren {#section-4c41bf41ff994910840c1352683d1f37}

Dit mechanisme kan ervoor zorgen dat klanten alleen inhoud ontvangen die geschikt is voor hun behoeften. Ervan uitgaande dat de statische inhoud is gecodeerd met de juiste code `catalog::UserType` waarden, kan de client de `type=` aan het verzoek. De beeldenserver vergelijkt de waarde die met `type=` aan de waarde van `catalog::UserType` en retourneert een fout in plaats van mogelijk onjuiste inhoud als er een probleem is.

## Bestanden van videobijschriften {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

U kunt videotitelbestanden (WebVTT), CSS of een willekeurig tekstbestand in JSONP-indeling inkapselen. De JSON-respons wordt hieronder beschreven.

* Voor WebVTT-bestanden is het mime-type van de reactie tekst/javascript. JSON wordt niet geretourneerd. In plaats daarvan wordt JavaScript geretourneerd dat een methode met JSON aanroept. Zowel identiteitskaart als manager zijn facultatief.
* Voor CSS-bestanden is het mime-type van de reactie text/javascript. Zowel identiteitskaart als manager zijn facultatief.
* UTF-8-codering wordt standaard toegepast om ervoor te zorgen dat deze correct wordt gedecodeerd. De standaardformaatlimiet is 2 MB.

U kunt ook tracks gebruiken voor andere soorten metagegevens met tijdnotatie. De brongegevens voor elk spoorelement zijn een tekstdossier dat uit een lijst van getimed cues wordt samengesteld. Cuse kan gegevens opnemen in indelingen zoals JSON of CSV.

Zie [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) voor meer informatie over het formaat JSONP.

Zie [www.json.org](https://www.json.org/json-en.html) voor meer informatie over de JSON-indeling.

## Zie ook {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referentie afbeeldingscatalogus](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
