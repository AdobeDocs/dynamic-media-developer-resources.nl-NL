---
description: De eigenschappen en syntaxis van afbeeldingscatalogi worden in deze sectie beschreven.
solution: Experience Manager
title: Afbeeldingscatalogi
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Afbeeldingscatalogi{#image-catalogs}

De eigenschappen en syntaxis van afbeeldingscatalogi worden in deze sectie beschreven.

Afbeeldingscatalogi bieden de volgende functies:

* Een blijvende koppeling van afbeeldingen met bepaalde metagegevens en wijzigingopdrachten toestaan.

   Er wordt verwezen naar items in afbeeldingscatalogi met een snelkoppelingnotatie `*`rootId/objId`*`, waarbij `*`rootId`*` de afbeeldingscatalogus en `*`objId`*` geeft een gegevensrecord in de catalogus aan.
* Verstrek gebreken voor bepaalde verzoekattributen, zoals de kwaliteit van de JPEG of of een watermerk moet worden toegepast.
* Lettertypen, ICC-profielen, macrodefinities en aanvraagsjablonen beheren

Zelfs als er geen specifieke afbeeldingscatalogi zijn gedefinieerd, zijn alle functies van afbeeldingscatalogi beschikbaar via de standaardcatalogus ( [!DNL default.ini]).

Indien `*`rootId`*` in het URL-pad van de aanvraag komt overeen `attribute::RootId` van een specifieke afbeeldingscatalogus wordt die catalogus de hoofdcatalogus voor deze aanvraag. De hoofdcatalogus bevat de standaardkenmerken en -instellingen voor de gehele aanvraag. Als er geen overeenkomende catalogus wordt gevonden, wordt in plaats daarvan de standaardcatalogus gebruikt.

Een catalogus die is geïdentificeerd in een `src=` of `mask=` biedt de volgende cataloguskenmerken en -gegevens aan de huidige laag:

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
   <td> <p> standaard voor <span class="codeph"> catalogus::Verlopen</span> of verlopen van de huidige laag als er geen catalogusrecord is betrokken </p> </td> 
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
   <td> <p> standaard voor <span class="codeph"> catalogus:Resolutie</span> alleen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Anker</span> </p> </td> 
   <td> <p> standaard voor de <span class="codeph"> anchor=</span> waarde van de huidige laag </p> </td> 
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
   <td> <p> voorvoegselopdrachten voor de huidige laag (elke opdracht in <span class="codeph"> catalogus::Modifier</span> kan worden overschreven door dezelfde opdracht in de URL, als deze voor dezelfde laag is opgegeven) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::pad</span> </p> </td> 
   <td> <p> het bronafbeeldingsbestand voor de huidige laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::PostModifier</span> </p> </td> 
   <td> <p> postfix-opdrachten voor de huidige laag (vergelijkbaar met <span class="codeph"> catalogus::Modifier</span>, maar opdrachten in <span class="codeph"> catalogus::PostModifier</span> dezelfde opdrachten overschrijven die in de URL of in <span class="codeph"> catalogus::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus:Resolutie</span> </p> </td> 
   <td> <p> de objectresolutie van de huidige laag </p> </td> 
  </tr> 
 </tbody> 
</table>

Binnen dezelfde laag, `src=` en `mask=` moet verwijzen naar dezelfde (eventuele) afbeeldingscatalogus.

Een catalogus die is geïdentificeerd in een `icc=` wordt alleen gebruikt om een item uit de ICC-profieltabel van de catalogus op te zoeken. Er zijn geen andere cataloguskenmerken of -gegevens bij betrokken.

Indien: `*`rootId`*` wordt omgezet in een catalogus, en `*`objId`*` komt overeen met een `catalog::Id` in deze catalogus, dan `*`rootId/objId`*` wordt in feite vervangen door de volgende vermelding in de catalogus:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Zie ook {#section-00e4f6b39cd14244bcce537a3f831259}

[Referentie afbeeldingscatalogus](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
