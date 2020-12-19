---
description: Source Object Specifier. Afbeeldings-, SVG- en ICC-profielobjecten kunnen worden opgegeven als afbeeldingscatalogus-items of relatieve bestandspaden
seo-description: Source Object Specifier. Afbeeldings-, SVG- en ICC-profielobjecten kunnen worden opgegeven als afbeeldingscatalogus-items of relatieve bestandspaden
seo-title: object
solution: Experience Manager
title: object
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---


# object{#object}

Source Object Specifier. Afbeeldings-, SVG- en ICC-profielobjecten kunnen worden opgegeven als afbeeldingscatalogus-items of relatieve bestandspaden

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>naam van de afbeeldingscatalogus ( <span class="codeph">-kenmerk::basisId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID van de afbeeldings-, SVG-, sjabloon- of ICC-profielrecord in de opgegeven, hoofd- of standaardafbeeldingscatalogus </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> pad  </span> </span> </p> </td> 
  <td class="stentry"> <p>pad en naam van relatieve afbeelding, masker of ICC-profielbestand </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>kan voorkomen hetzij in het belangrijkste URL weg, of in <span class="codeph"> src= </span>, <span class="codeph"> masker= </span>, of <span class="codeph"> icc= </span> bevel </p> </td> 
 </tr> 
</table>

*`rootId`* geeft een afbeeldingscatalogus aan. (Zie [Afbeeldingscatalogus](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) voor meer informatie.) Als *`rootId`* in de weg URL wordt gespecificeerd, wordt die catalogus *belangrijkste catalogus* voor dit verzoek. Anders wordt de standaardcatalogus gebruikt als de hoofdcatalogus. In dezelfde aanvraag kunnen meerdere verschillende afbeeldingcatalogi worden gebruikt.

De server gaat er aanvankelijk van uit dat *`rootId`* wordt weggelaten in de opdrachten `src=`, `mask=` en `icc=` en dat wordt geprobeerd een item in de catalogus te zoeken. In feite probeert de server de gehele *`object`*-tekenreeks als *`objId.`* te gebruiken

Als een item uit een catalogus wordt gevonden, wordt dit gebruikt; anders, probeert de server volgende om *`rootId`* van een beeldcatalogus aan te passen. Als een catalogus wordt geïdentificeerd, wordt het gezocht naar *`objId`*. Als en de ingang wordt gevonden, wordt het gebruikt.

Anders wordt *`object`* verondersteld om een expliciete dossierweg te zijn. Als `attribute::FullMatch` in dit geval is ingesteld in de hoofdcatalogus, wordt de catalogus voor dit object genegeerd en wordt in plaats daarvan de standaardcatalogus gebruikt. Als `attribute::FullMatch` niet is ingesteld, wordt de hoofdcatalogus gebruikt voor verdere verwerking.

Zowel *`rootId`* als *`objId`* zijn case-sensitive. *`path`* is alleen hoofdlettergevoelig op UNIX.

Als een regelafstand &#39;/&#39; is opgegeven, wordt in plaats van de hoofdcatalogus gezocht naar de standaardcatalogus. Dit is vooral handig wanneer een expliciet pad `default::RootPath` vereist in plaats van `attribute::RootPath` van de hoofdcatalogus, maar ook kan worden gebruikt om toegang te krijgen tot items in de standaardcatalogus die anders zouden worden overschreven door items in de hoofdcatalogus.

Raadpleeg *Inhoud beheren* in de *Server Configuration Guide* voor meer informatie over hoe *`path`* wordt vertaald naar een fysiek bestandspad.

>[!NOTE]
>
>Komma &#39;,&#39;-tekens zijn niet toegestaan in *`object.`*

## Ondersteunde bestandsindelingen {#section-12c85aead78e4f759856ca9ff10637d7}

Raadpleeg de beschrijving van het hulpprogramma IC (Image Converter) voor een volledige lijst met ondersteunde bestandsindelingen.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het beste als de indeling voor meerresolutie van de Scene7 piramid TIFF (PTIF) wordt gebruikt. Het hulpprogramma IC wordt gebruikt om PTIF-afbeeldingen te maken in elke ondersteunde afbeeldingsindeling.

## Voorbeelden {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Een afbeelding en een ICC-profiel openen in twee verschillende afbeeldingcatalogi**

Haal de afbeelding &#39; [!DNL myImage]&#39; op in de afbeeldingscatalogus die is geïdentificeerd als &#39; [!DNL myCatalog]&#39; en koppel het ICC-profiel &#39; [!DNL sRGB]&#39; dat zich bevindt in de afbeeldingscatalogus met de naam &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Eén afbeeldingscatalogus met lagen gebruiken

**Maak een eenvoudige samengestelde afbeelding die bestaat uit drie lagen, die allemaal zijn opgehaald uit &#39;  [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Afbeeldingsbestanden rechtstreeks openen terwijl u nog steeds een catalogus gebruikt voor kenmerken**

Toegang [!DNL my/image/path/myImage.tif] met de standaard JPG-kenmerken die zijn geconfigureerd in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Zie ook {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
