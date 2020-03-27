---
description: Afbeeldingskaartgegevens. Biedt afbeeldingskaartgegevens voor deze laag. Hiermee overschrijft u alle gegevens uit de catalogus Kaart voor deze laag.
seo-description: Afbeeldingskaartgegevens. Biedt afbeeldingskaartgegevens voor deze laag. Hiermee overschrijft u alle gegevens uit de catalogus Kaart voor deze laag.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# map{#map}

Afbeeldingskaartgegevens. Biedt afbeeldingskaartgegevens voor deze laag. Hiermee overschrijft u alle gegevens uit de catalogus::Kaart voor deze laag.

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tekenreeks</span></span> </p></td> 
  <td class="stentry"> <p>Afbeeldingskaartgegevens voor deze laag in laagcoördinaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tekenreeksA</span></span> </p></td> 
  <td class="stentry"> <p>Afbeeldingskaartgegevens voor deze laag in coördinaten van de bronafbeelding. </p></td> 
 </tr> 
</table>

Een lege tekenreeks geeft aan dat deze laag geen afbeelding met hyperlinks mag bevatten. De tekenreeks moet correct zijn gecodeerd via HTTP om parseerproblemen te voorkomen.

Alle ampersand (&amp;) karakters die in voorkomen *`string`* moeten http-gecodeerd zijn.

Terwijl `mapA=` en `catalog::Map` kaartgegevens opgeven in coördinaten van bronafbeeldingen, `map=` wordt uitgegaan van laagcoördinaten ten opzichte van de bovenste, linkerhoek van de laagrechthoek (nadat `rotate=` en `extend=` toegepast).

De uitvoerafbeelding met hyperlinks wordt altijd geknipt naar de laagrechthoek. Als het `shape` kenmerk wordt weggelaten of is ingesteld op `default`, wordt de volledige laagrechthoek gebruikt als het gebied met afbeeldingskaart.

## Eigenschappen {#section-a18d9ea95c71414a905a68b8839c0843}

Laagkenmerk. Wanneer toegepast op `layer=comp`, worden de gespecificeerde kaartgegevens gelaagd achter alle andere beeldkaarten. Genegeerd tenzij `req=map`. Genegeerd door effectlagen. `mapA=` wordt genegeerd als `map=` ook wordt opgegeven.

## Standaard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` wordt gebruikt als `map=` niet is opgegeven.

## Voorbeeld {#section-cd7691c94f984222845c86dcb0051ce8}

Definieer een rechthoekige afbeeldingskaart voor een eenvoudige tekstlaag:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Een `AREA` element met (meestal) standaardattributen wordt gebruikt om het kaartgebied voor de volledige laagrechthoek op te nemen.

## Zie ook {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Afbeeldingskaarten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=kaart](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
