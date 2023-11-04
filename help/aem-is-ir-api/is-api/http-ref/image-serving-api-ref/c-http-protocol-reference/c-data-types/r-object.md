---
description: Source Object Specifier. Afbeeldings-, SVG- en ICC-profielobjecten kunnen worden opgegeven als afbeeldingscatalogus-items of relatieve bestandspaden
solution: Experience Manager
title: object
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# object{#object}

Source Object Specifier. Afbeeldings-, SVG- en ICC-profielobjecten kunnen worden opgegeven als afbeeldingscatalogus-items of relatieve bestandspaden

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`pad`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>naam van de afbeeldingscatalogus ( <span class="codeph"> kenmerk::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID van de afbeeldings-, SVG-, sjabloon- of ICC-profielrecord in de opgegeven, hoofd- of standaardafbeeldingscatalogus </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> pad </span> </span> </p> </td> 
  <td class="stentry"> <p>pad en naam van relatieve afbeelding, masker of ICC-profielbestand </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>kan voorkomen in het hoofd-URL-pad of in een <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>, of <span class="codeph"> icc= </span> command </p> </td> 
 </tr> 
</table>

*`rootId`* geeft een afbeeldingscatalogus aan. (Zie [Afbeeldingscatalogus](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) voor meer informatie.) Indien *`rootId`* wordt opgegeven in het URL-pad, wordt die catalogus *hoofdcatalogus* voor dit verzoek. Anders wordt de standaardcatalogus gebruikt als de hoofdcatalogus. In dezelfde aanvraag kunnen meerdere verschillende afbeeldingcatalogi worden gebruikt.

De server gaat er aanvankelijk van uit dat *`rootId`* wordt weggelaten in `src=`, `mask=`, en `icc=` opdrachten en pogingen om een item in de catalogus te zoeken. In feite probeert de server de gehele server te gebruiken *`object`* tekenreeks als *`objId.`*

Als een catalogusitem wordt gevonden, wordt dit gebruikt. Als dit niet het geval is, probeert de volgende server het item *`rootId`* van een afbeeldingscatalogus. Als een catalogus wordt geïdentificeerd, wordt gezocht naar *`objId`*. Als en de ingang wordt gevonden, wordt het gebruikt.

Anders, *`object`* wordt aangenomen dat het een expliciet bestandspad betreft. In dat geval, indien `attribute::FullMatch` wordt ingesteld in de hoofdcatalogus, wordt de catalogus genegeerd voor dit object en wordt in plaats daarvan de standaardcatalogus gebruikt. Indien `attribute::FullMatch` niet is ingesteld, wordt de hoofdcatalogus gebruikt voor verdere verwerking.

Beide *`rootId`* en *`objId`* hoofdlettergevoelig zijn. *`path`* is alleen hoofdlettergevoelig op UNIX.

Indien een regelafstand `/` wordt opgegeven, wordt de standaardcatalogus doorzocht in plaats van de hoofdcatalogus. Dit is vooral handig wanneer een expliciet pad vereist `default::RootPath` in plaats van de hoofdcatalogus `attribute::RootPath`, maar kan ook worden gebruikt om toegang te krijgen tot items in de standaardcatalogus die anders zouden worden overschreven door items in de hoofdcatalogus.

Zie *Inhoud beheren* in de *Serverconfiguratiegids* voor meer informatie over hoe *`path`* wordt omgezet in een fysiek bestandspad.

>[!NOTE]
>
>Komma &#39;,&#39; tekens zijn niet toegestaan in *`object.`*

## Ondersteunde bestandsindelingen voor afbeeldingen {#section-12c85aead78e4f759856ca9ff10637d7}

Raadpleeg de beschrijving van het hulpprogramma IC (Image Converter) voor een volledige lijst met ondersteunde bestandsindelingen.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het beste als de indeling voor meerresolutie van de Dynamic Media-piramide TIFF (PTIF) wordt gebruikt. Het hulpprogramma IC wordt gebruikt om PTIF-afbeeldingen te maken in elke ondersteunde afbeeldingsindeling.

## Voorbeelden {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Een afbeelding en een ICC-profiel openen in twee verschillende afbeeldingcatalogi**

De afbeelding ophalen &#39; [!DNL myImage]&#39; in de afbeeldingscatalogus aangeduid als &#39; [!DNL myCatalog]en sluit het ICC-profiel &#39; [!DNL sRGB]&#39; in de afbeeldingscatalogus &#39; [!DNL myProfiles]&quot;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Eén afbeeldingscatalogus met lagen gebruiken

**Een eenvoudige samengestelde afbeelding maken die bestaat uit drie lagen en die allemaal zijn opgehaald uit &#39; [!DNL myCatalog]&quot;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Afbeeldingsbestanden rechtstreeks openen terwijl u nog steeds een catalogus gebruikt voor kenmerken**

Toegang [!DNL my/image/path/myImage.tif], met de standaard JPG-kenmerken die zijn geconfigureerd in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Zie ook {#section-b6eccefad63f441d922699c4aba58fc9}

[IC-hulpprogramma](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [kenmerk::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
