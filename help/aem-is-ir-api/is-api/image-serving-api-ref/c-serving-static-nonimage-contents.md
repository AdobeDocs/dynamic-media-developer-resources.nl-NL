---
description: Met Afbeeldingsserver kunt u niet-afbeeldingsinhoud in catalogi beheren en deze via een aparte /is/content-context bedienen.
seo-description: Met Afbeeldingsserver kunt u niet-afbeeldingsinhoud in catalogi beheren en deze via een aparte /is/content-context bedienen.
seo-title: Statische (niet-afbeeldings) inhoud bedienen
solution: Experience Manager
title: Statische (niet-afbeeldings) inhoud bedienen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# Statische (niet-grafische) inhoud{#serving-static-non-image-contents} leveren

Met Afbeeldingsserver kunt u niet-afbeeldingsinhoud in catalogi beheren en deze via een aparte /is/content-context bedienen.

Dit vermogen staat voor het vormen van TTL voor elk punt afzonderlijk toe.

Beeldserver ondersteunt de volgende opdrachten op [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type  </a> </p> </td> 
  <td class="stentry"> <p>Filter Inhoudstype. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>, and  <span class="codeph"> req=exists  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cachegeheugen  </a> </p> </td> 
  <td class="stentry"> <p>Hiermee wordt caching op de client uitgeschakeld. </p> </td> 
 </tr> 
</table>

## Basissyntaxis {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> verzoek  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/ <span class="varname"> item  </span>][? <span class="varname"> modifiers  </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> poort  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogus  </span> </span> </p> </td> 
  <td class="stentry"> <p>Catalogus-id. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>Item-id voor statische inhoud. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifiers  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opdracht  </span>*[&amp;  <span class="varname"> opdracht  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>Een van de ondersteunde opdrachtnamen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Opdrachtwaarde. </p> </td> 
 </tr> 
</table>

## Statische inhoudcatalogi {#section-91014f17f0d543d7aaf24539b2d7d4b9}

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
   <td colname="col1"> <p> <span class="codeph"> catalogus::Id  </span> </p> </td> 
   <td colname="col2"> <p>De id van de catalogusrecord voor dit statische inhoudsitem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::pad  </span> </p> </td> 
   <td colname="col2"> <p>Het bestandspad voor dit inhoudsitem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::Verlopen  </span> </p> </td> 
   <td colname="col2"> <p>De TTL voor dit inhoudsitem; <span class="codeph"> kenmerk::Vervaldatum </span> wordt gebruikt als deze niet is opgegeven of als deze leeg is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Tijdstempel voor bestandswijziging; vereist als validatie op basis van een catalogus is ingeschakeld met <span class="codeph">-kenmerk::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogus::UserData  </span> </p> </td> 
   <td colname="col2"> <p>Optionele metagegevens die zijn gekoppeld aan dit statische inhoudsitem; beschikbaar voor de client met <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType  </span> </p> </td> 
   <td colname="col2"> <p>Optioneel gegevenstype; U kunt verzoeken om statische inhoud filteren met de opdracht <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Statische inhoud filteren {#section-4c41bf41ff994910840c1352683d1f37}

Dit mechanisme kan ervoor zorgen dat klanten alleen inhoud ontvangen die geschikt is voor hun behoeften. Ervan uitgaande dat de statische inhoud is gelabeld met de juiste `catalog::UserType`-waarden, kan de client de opdracht `type=` aan de aanvraag toevoegen. Bij Afbeeldingsservice wordt de waarde die met de opdracht `type=` is opgegeven, vergeleken met de waarde `catalog::UserType` en wordt bij een onjuiste overeenkomst een fout geretourneerd in plaats van mogelijk onjuiste inhoud.

## Bestanden voor videobijschriften {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

U kunt videotitelbestanden (WebVTT), CSS of een willekeurig tekstbestand in JSONP-indeling inkapselen. De JSON-respons wordt hieronder beschreven.

* Voor WebVTT-bestanden is het mime-type van de reactie tekst/javascript. JSON wordt niet geretourneerd; in plaats daarvan wordt Javascript geretourneerd die een methode met JSON aanroept. Zowel identiteitskaart als manager zijn facultatief.
* Voor CSS-bestanden is het mime-type van de reactie text/javascript. Zowel identiteitskaart als manager zijn facultatief.
* UTF-8-codering wordt standaard toegepast om ervoor te zorgen dat deze correct wordt gedecodeerd. De standaardgroottelimiet is 2 MB.

U kunt ook tracks gebruiken voor andere soorten metagegevens met tijdnotatie. De brongegevens voor elk spoorelement zijn een tekstdossier dat uit een lijst van getimed cues wordt samengesteld. Cuse kan gegevens opnemen in indelingen zoals JSON of CSV.

Zie [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) voor meer informatie over het formaat JSONP.

Zie [www.json.org](http://www.json.org) voor meer informatie over de JSON-indeling.

## Zie ook {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Referentie  [afbeeldingscatalogus](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
