---
title: map
description: Afbeeldingskaartgegevens. Biedt afbeeldingskaartgegevens voor deze laag. Hiermee overschrijft u alle gegevens uit de catalogus Kaart voor deze laag.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# map{#map}

Afbeeldingskaartgegevens. Biedt afbeeldingskaartgegevens voor deze laag. Hiermee overschrijft u alle gegevens uit de catalogus::Kaart voor deze laag.

`map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Afbeeldingskaartgegevens voor deze laag in laagcoördinaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Afbeeldingskaartgegevens voor deze laag in coördinaten van de bronafbeelding. </p></td> 
 </tr> 
</table>

Een lege tekenreeks geeft aan dat deze laag geen afbeelding met hyperlinks mag bevatten. De tekenreeks moet correct zijn gecodeerd via HTTP om parseerproblemen te voorkomen.

Alle en-tekens (&amp;) komen voor in *`string`* moet http-encoded zijn.

while `mapA=` en `catalog::Map` kaartgegevens opgeven in coördinaten van bronafbeeldingen, `map=` neemt laagcoördinaten aan ten opzichte van de linkerbovenhoek van de laagrechthoek (na `rotate=` en `extend=` zijn toegepast).

De uitvoerafbeelding met hyperlinks wordt altijd geknipt naar de laagrechthoek. Als de `shape` kenmerk wordt weggelaten of ingesteld op `default`, wordt de volledige laagrechthoek gebruikt als het gebied van de beeldkaart.

## Eigenschappen {#section-a18d9ea95c71414a905a68b8839c0843}

Laagkenmerk. Wanneer toegepast op `layer=comp`, worden de opgegeven kaartgegevens in lagen achter alle andere afbeeldingen met hyperlinks geplaatst. Genegeerd tenzij `req=map`. Genegeerd door effectlagen. `mapA=` wordt genegeerd als `map=` wordt ook opgegeven.

## Standaard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` wordt gebruikt als `map=` is niet opgegeven.

## Voorbeeld {#section-cd7691c94f984222845c86dcb0051ce8}

Definieer een rechthoekige afbeeldingskaart voor een eenvoudige tekstlaag:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

An `AREA` -element met (meestal) standaardkenmerken wordt gebruikt om het kaartgebied voor de gehele laagrechthoek in te voegen.

## Zie ook {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Afbeeldingskaarten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
