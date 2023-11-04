---
title: regel
description: Regel-element aanvragen. Een of meer regels zijn optioneel in het dialoogvenster <ruleset> element.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# regel{#rule}

Regel-element aanvragen. Een of meer regels zijn optioneel in het dialoogvenster `<ruleset>` element.

## Attributen {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Optioneel. De standaardwaarde is &quot;break&quot;.

`Replace = "first" | "all"`: Optioneel. De standaardwaarde is &quot;first&quot;.

`RequestType` = *&quot;`types`&quot;*: Optioneel. Geeft aan op welke invoercontext de regel van toepassing is. *`types`* is een lijst met komma&#39;s als scheidingsteken. Deze lijst kan een of meer tokens bevatten die in de volgende tabel worden vermeld. Indien `RequestType` niet wordt gespecificeerd, is de regel op verzoeken van toepassing die op alle gesteunde contexten worden ontvangen.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>token</b> </p> </th> 
   <th class="entry"> <p><b>Context</b> </p> </th> 
   <th class="entry"> <p><b>Beschrijving</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> is</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Toegepast op verzoeken om beeldbewerking </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Toegepast op aanvragen voor het renderen van afbeeldingen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> static</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Toegepast op aanvragen voor statische inhoud </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Optioneel. Wordt gebruikt om de `<rule>` -element in foutopsporingslogboeken en foutberichten.

`  *`Kenmerk`* ="value"`: Optioneel. `<rule>` elementen kunnen elk van de volgende kenmerken definiëren in elke combinatie. Als deze optie is opgegeven en de regel correct wordt toegepast, worden de overeenkomende cataloguskenmerken voor deze aanvraag genegeerd. Standaard is `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Kenmerk </span> </b> </th> 
   <th class="entry"> <p>Overeenkomende afbeeldingscataloguskenmerken </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> kenmerk:DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Verlopen</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> kenmerk::Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> kenmerk::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> kenmerk::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> kenmerk::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> kenmerk:RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> kenmerk:SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> kenmerk::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Raadpleeg de beschrijving van het overeenkomstige kenmerk voor de afbeeldingscatalogus voor meer informatie.

De kenmerken Expiration overschrijven alleen de standaardkenmerkwaarden. De overschrijving wordt genegeerd als een specifieke `catalog::Expiration` waarde is van toepassing op de aanvraag.

## Gegevens {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Optioneel </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>Optioneel </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>Optioneel </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>Optioneel </p></td> 
 </tr> 
</table>

## Notities {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Als beide `<expression>` en `<substitution>` worden opgegeven en vastgelegde subtekenreeksen niet worden gebruikt, wordt de eerste overeenkomende subtekenreeks vervangen door `<substitution>`.

Indien `<expression>` niet is opgegeven, overeenkomende paden en `<substitution>` wordt toegevoegd aan het einde van het pad.

Indien `<substitution>` niet is opgegeven, er vindt geen pad- of querytransformatie plaats, maar opgegeven cataloguskenmerken worden overschreven. Indien `<substitution>` is leeg, wordt de overeenkomende subtekenreeks verwijderd.

De `<addressfilter>` wordt toegepast slechts wanneer een gelijke voorkomt, en vóór vraagregels worden toegepast.
