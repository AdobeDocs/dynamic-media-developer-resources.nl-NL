---
description: Eigenschappen van responsgegevens. Evalueert het huidige verzoek alsof het een beeldverzoek (req=img) was, maar in plaats van het beeld terug te keren, keert de server geselecteerde eigenschappen van het antwoordbeeld terug.
seo-description: Eigenschappen van responsgegevens. Evalueert het huidige verzoek alsof het een beeldverzoek (req=img) was, maar in plaats van het beeld terug te keren, keert de server geselecteerde eigenschappen van het antwoordbeeld terug.
seo-title: props
solution: Experience Manager
title: props
topic: Scene7 Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# props{#props}

Eigenschappen van responsgegevens. Evalueert het huidige verzoek alsof het een beeldverzoek (req=img) was, maar in plaats van het beeld terug te keren, keert de server geselecteerde eigenschappen van het antwoordbeeld terug.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p> </td> 
 </tr> 
</table>

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

Zie [Eigenschappen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) voor een beschrijving van de antwoordsyntaxis en het antwoord MIME type. De reactie van HTTP is cacheable met TTL die op `attribute::NonImgExpiration` wordt gebaseerd.

De volgende eigenschappen worden geretourneerd voor aanvragen van /is/image:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschap</b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Beschrijving</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> Achtergrondkleur (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Hoogte van afbeelding in pixels beantwoorden </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> True if the ICC profile is embedded in the response image. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Naam/beschrijving van het profiel dat aan de antwoordafbeelding is gekoppeld. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Reaginggrootte in pixels, exclusief de HTTP-header. 0 als de gegevens van het antwoordbeeld niet eerder door de server in het voorgeheugen onder zijn gebracht. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 als de antwoordafbeelding een alfakanaal bevat, anders 0. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Type reactieafbeelding kan <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> of <span class="codeph"> BW </span> (voor grijswaardenafbeeldingen) zijn. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 als in de reactieafbeelding paden zijn ingesloten, 0 in andere gevallen. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> echt </p> </td> 
   <td> <p> Afdrukresolutie (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG-kwaliteit. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> MIME-type voor de antwoordafbeelding. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Breedte van afbeelding beantwoorden in pixels. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 als in de reactieafbeelding xmp-gegevens worden ingesloten, anders 0. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Id van afbeeldingsversie. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Versie-id metagegevens. (Zie <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende eigenschappen worden geretourneerd voor `/is/content`-aanvragen:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Eigenschap</b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Beschrijving</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> pad  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Gedeeltelijk opgelost bestandspad. (Zie <span class="codeph"> statisch::Pad </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Bestandsgrootte van object in bytes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> vervaldatum  </span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration  </span> of de standaardtijd om te leven </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Wijzigingsdatum/-tijd (vanaf <span class="codeph"> statisch::TimeStamp </span> of het objectbestand) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

