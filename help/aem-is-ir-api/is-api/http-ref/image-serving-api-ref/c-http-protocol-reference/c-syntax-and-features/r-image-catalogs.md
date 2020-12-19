---
description: De eigenschappen en syntaxis van afbeeldingscatalogi worden in deze sectie beschreven.
seo-description: De eigenschappen en syntaxis van afbeeldingscatalogi worden in deze sectie beschreven.
seo-title: Afbeeldingscatalogi
solution: Experience Manager
title: Afbeeldingscatalogi
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# Afbeeldingscatalogi{#image-catalogs}

De eigenschappen en syntaxis van afbeeldingscatalogi worden in deze sectie beschreven.

Afbeeldingscatalogi bieden de volgende functies:

* Een blijvende koppeling van afbeeldingen met bepaalde metagegevens en wijzigingopdrachten toestaan.

   Er wordt verwezen naar items in afbeeldingcatalogi met een sneltoetsnotatie ` *`rootId/objId`*`, waarbij ` *`rootId`*` de afbeeldingscatalogus identificeert en ` *`objId`*` een gegevensrecord in de catalogus identificeert.
* Geef standaardwaarden op voor bepaalde aanvraagkenmerken, zoals de JPEG-kwaliteit of het feit of een watermerk moet worden toegepast.
* Lettertypen, ICC-profielen, macrodefinities en aanvraagsjablonen beheren

Zelfs als er geen specifieke afbeeldingscatalogi zijn gedefinieerd, zijn alle functies van afbeeldingscatalogi beschikbaar via de standaardcatalogus ( [!DNL default.ini]).

Als ` *`rootId`*` in de weg van URL van het verzoek `attribute::RootId` van een specifieke beeldcatalogus aanpast, zal die catalogus de belangrijkste catalogus voor dit verzoek worden. De hoofdcatalogus bevat de standaardkenmerken en -instellingen voor de gehele aanvraag. Als er geen overeenkomende catalogus wordt gevonden, wordt in plaats daarvan de standaardcatalogus gebruikt.

Een catalogus die is geïdentificeerd in de opdracht `src=` of `mask=` biedt de volgende cataloguskenmerken en -gegevens aan de huidige laag:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Kenmerk/gegevens</b> </th> 
   <th class="entry"> <b> Notities</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::DefaultExt</span> </p> </td> 
   <td> <p> de standaardextensie voor alle paden voor afbeeldingsbestanden in de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::Expiration</span> </p> </td> 
   <td> <p> standaard voor <span class="codeph">-catalogus::Verlopen</span> of verlopen van de huidige laag als er geen catalogusrecord is betrokken </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::Icc*</span> </p> </td> 
   <td> <p> het werkende ICC kleurenprofiel, geef intentie, en zwarte puntcompensatiemarkering voor het verzoek en/of de huidige laag terug </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk::RootPath</span> </p> </td> 
   <td> <p> wordt gebruikt voor alle bronbestandspaden van de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> kenmerk:Resolution</span> </p> </td> 
   <td> <p> standaard voor <span class="codeph">-catalogus::Resolutie</span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Anker</span> </p> </td> 
   <td> <p> standaardwaarde voor het <span class="codeph"> anker=</span> waarde van de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Verlopen</span> </p> </td> 
   <td> <p> de kleinste vervalwaarde van alle lagen wordt gebruikt als tijd-aan-levende waarde van het antwoordbeeld </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::IccProfile</span> </p> </td> 
   <td> <p> het kleurprofiel van de bronafbeelding voor de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Kaart</span> </p> </td> 
   <td> <p> de afbeeldingskaartgegevens voor de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::MaskPath</span> </p> </td> 
   <td> <p> standaard voor <span class="codeph"> mask=</span> voor de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Modifier</span> </p> </td> 
   <td> <p> voorvoegselopdrachten voor de huidige laag (elke opdracht in de catalogus <span class="codeph">::Modifier</span> kan worden overschreven door dezelfde opdracht in de URL, indien deze voor dezelfde laag is opgegeven) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::pad</span> </p> </td> 
   <td> <p> het bronafbeeldingsbestand voor de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::PostModifier</span> </p> </td> 
   <td> <p> postfix-opdrachten voor de huidige laag (vergelijkbaar met de catalogus <span class="codeph">::Modifier</span>, maar opdrachten in de catalogus <span class="codeph">::PostModifier</span> overschrijven dezelfde opdrachten die in de URL of in de catalogus <span class="codeph"> zijn opgegeven::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus:Resolutie</span> </p> </td> 
   <td> <p> de objectresolutie van de huidige laag </p> </td> 
  </tr> 
 </tbody> 
</table>

Binnen dezelfde laag moeten `src=` en `mask=` naar dezelfde (eventuele) afbeeldingscatalogus verwijzen.

Een catalogus die wordt geïdentificeerd in een `icc=` bevel wordt slechts gebruikt om een ingang van de ICC profiellijst van de catalogus op te zoeken. Er zijn geen andere cataloguskenmerken of -gegevens bij betrokken.

Als ` *`rootId`*` wordt omgezet in een catalogus, en ` *`objId`*` wordt aangepast met een `catalog::Id` in deze catalogus, dan wordt ` *`rootId/objId`*` effectief vervangen door de catalogusvermelding als volgt:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Zie ook {#section-00e4f6b39cd14244bcce537a3f831259}

[Referentie](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) afbeeldingscatalogus,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
