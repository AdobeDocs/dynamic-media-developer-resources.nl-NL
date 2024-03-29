---
description: De Server van het beeld verstrekt een mechanisme om een hiërarchische tekstreactie (xml of json) op te halen die alle middelen en meta-gegevens verbonden aan catalogus ImageSet voor een bepaald verslag vertegenwoordigt.
solution: Experience Manager
title: Mediasetaanvragen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Mediasetaanvragen{#media-set-requests}

De Server van het beeld verstrekt een mechanisme om een hiërarchische tekstreactie (xml of json) op te halen die alle middelen en meta-gegevens verbonden aan catalogus vertegenwoordigt::ImageSet voor een bepaald verslag.

De kijkers kunnen dit mechanisme gebruiken om reacties te produceren om de presentatie van eenvoudige beelden, video&#39;s, videoreeksen, monsterreeksen, spin reeksen, paginasets (e-catalogi), en media reeksen te informeren.

## Aanvraagsyntaxis {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

De ingestelde reactie voor een `catalog::ImageSet` kan worden opgehaald met het gereedschap `req=set` wijzigen en verwijzen naar de catalogusrecord-id in het netto pad. De afbeeldingsset kan ook rechtstreeks in de URL worden opgegeven met de opdracht `imageset=` modifier. Als de `imageset=` De bepaling wordt gebruikt om imageset te specificeren, zou de volledige waarde in krullende steunen moeten worden ingesloten om de beeld te ontsnappen vastgestelde waarde en ervoor te zorgen dat om het even welke inbegrepen bepalingen niet als deel van het URL vraagkoord worden geïnterpreteerd.

## Typen ingestelde reacties {#section-93eb0a1f70344da2a888e56372ad3896}

Het ingestelde mechanisme ondersteunt de volgende typen reacties:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>eenvoudige afbeeldingen </p></td> 
  <td class="stentry"> <p>Een afbeeldingsrecord zonder <span class="codeph"> catalogus::ImageSet</span> gedefinieerd. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>eenvoudige video's </p></td> 
  <td class="stentry"> <p>Een video-opname in de statische inhoudscatalogus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>stalensets </p></td> 
  <td class="stentry"> <p>Een set items die bestaat uit een verwijzing naar een afbeeldingsrecord en een optionele aparte verwijzing naar een afbeeldingsrecord die als staal wordt gebruikt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>hiërarchische stalensets </p></td> 
  <td class="stentry"> <p>Een set items die bestaat uit een standaardstaalitem of een verwijzing naar een record in een stalenset. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>spin-sets </p></td> 
  <td class="stentry"> <p>Een set items die bestaat uit een eenvoudige lijst met afbeeldings-id's. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>tweedimensionale centrifuges </p></td> 
  <td class="stentry"> <p>Een set items die bestaat uit een eenvoudige afbeelding of een verwijzing naar een elementaire reeks spinnen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>paginasets </p></td> 
  <td class="stentry"> <p>Een reeks items die bestaat uit een lijst met maximaal drie pagina-afbeeldingen </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>mediasets </p></td> 
  <td class="stentry"> <p>Een set items die bestaat uit eenvoudige afbeeldingen, videoreeksen, stalensets, hiërarchische stalensets, centrifuges, tweedimensionale centrifuges, paginasets en video-elementen. Elk mediaset-item kan ook een optioneel staal bevatten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>videosets </p></td> 
  <td class="stentry"> <p>Een reeks items die bestaat uit een lijst met eenvoudige video's. </p></td> 
 </tr> 
</table>

## Typedetectie buiten instellen {#section-3dd6e453528d46898e559d31458a59ba}

Wanneer een `req=set` verzoek wordt ontvangen, wordt het type te produceren reactie bepaald door de waarde van `catalog::AssetType`. Indien `catalog::AssetType` niet wordt bepaald, dan wordt het reactietype bepaald door de volgende regels:

* Indien record wordt gevonden in de afbeeldingscatalogus EN `catalog::ImageSet` is gedefinieerd

   * Een e-catalogusset aannemen als ten minste één item in het veld Recordafbeeldingsset een dubbele punt bevat
   * Mediaset aannemen als ten minste één item in het veld Afbeeldingsset record twee puntkomma&#39;s bevat.
   * Afbeeldingsset aannemen als ten minste één item in het veld Afbeeldingsset record één puntkomma bevat.
   * Er wordt aangenomen dat er een centrifuge is ingesteld als geen item dubbele punt of puntkomma bevat, maar ten minste één item een set waarnaar wordt verwezen of een in-line set bevat (dit is een 2D-centrifuge).
   * Onbekende set veronderstellen als geen item dubbele punt of puntkomma bevat, noch als set of inline set waarnaar wordt verwezen (d.w.z. een door komma&#39;s gescheiden lijst met afbeeldingen).

* Als record wordt gevonden in zowel afbeeldings- ALS statische inhoudcatalogi

   * Video aannemen als de bestandsextensie zich in de volgende set bevindt: mp3, mp4, flv, f4v, swf, xml
   * Anders de afbeelding aannemen

* Als record wordt gevonden in statische inhoudscatalogus maar NIET in afbeeldingscatalogus

   * Video aannemen als de bestandsextensie zich in de volgende set bevindt: mp3, mp4, flv, f4v, swf, xml
   * Anders statisch aannemen

* Indien opname is gevonden in de afbeeldingscatalogus maar NIET in de catalogus met statische inhoud

   * Afbeelding aannemen

* Als er geen record wordt gevonden in de afbeeldingscatalogus en NIET in de catalogus met statische inhoud

   * Op bestanden gebaseerde video aannemen als de bestandsextensie de volgende set heeft: mp3, mp4, flv, f4v, swf, xml
   * Anders wordt een op een bestand gebaseerde afbeelding aangenomen

In alle gevallen komt de resulterende xml-reactie overeen met het opgegeven XML-document met het ingestelde hoofdknooppunt dat overeenkomt met het gedetecteerde type.

## Typedetectie binnen {#section-8f46490e467247e69ce284704def06f3}

Wanneer de buitenste set wordt gedetecteerd als een mediaset, bevat de reactie een set mediasetitems die overeenkomen met elk mediasetitem in `catalog::ImageSet`. Als de optionele parameter type is opgegeven voor een bepaald mediaset-item, wordt deze toegewezen aan een uitvoertype volgens de volgende tabel:

| Invoertype | Uitvoertype |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Als de optionele parameter type voor een bepaald mediaset-item niet is opgegeven of overeenkomt met een niet-ondersteund type, wordt het mediaset-itemtype automatisch gedetecteerd volgens dezelfde regels als die welke op het buitenste setniveau zijn toegepast.

## XML-specificatie {#section-c1bd60948ef545759a16885bb6fcc607}

De geretourneerde xml-reactie voldoet aan de volgende specificatie:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

De `labelkey=` modifier wordt gebruikt samen met de `catalog::UserData`veld voor het genereren van labels voor afbeeldingen en stalen. De `catalog:UserData` veld wordt geparseerd als een set sleutel/waardeparen en de index van de labeltoets in deze set om de waarde voor de opgegeven toets op te halen. Deze waarde wordt vervolgens geretourneerd in het dialoogvenster *`l`* kenmerk voor de *`s`* en *`i`*.

## Afgedwongen beperkingen {#section-b9f042873bee45a5ae11b69fd42f2bca}

Om de grootte van de reactie te beperken en zelf-verwijzingskwesties te verhinderen, wordt de maximum het nesten diepte gecontroleerd door het serverbezit `PS::fvctx.nestingLimit`. Als deze limiet wordt overschreden, wordt een fout geretourneerd.

Om de grootte van de xml- reacties voor grote e-catalogusreeksen te beperken, worden de privé meta-gegevens onderdrukt voor brochure vastgestelde punten volgens het serverbezit `PS::fvctx.brochureLimit`. Alle persoonlijke metagegevens die aan de brochure zijn gekoppeld, worden geëxporteerd totdat de brochure-limiet is bereikt. Nadat de limiet is overschreden, worden privékaarten en gebruikersgegevens onderdrukt en wordt een bijbehorende markering ingesteld om aan te geven welk type gegevens is onderdrukt.

Geneste mediasets worden niet ondersteund. Een geneste mediaset wordt gedefinieerd als een mediaset die een mediaset-item van het type mediaset bevat. Als deze voorwaarde wordt gedetecteerd, wordt een fout geretourneerd.

## Voorbeelden {#section-588c9d33aa05482c86cd2b1936887228}

Voor voorbeeld-XML-reacties voor `req=set` verzoek, verwijs naar de pagina van Eigenschappen onder de kopbal van de Voorbeelden van de HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Zie ook {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalogus::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Referentie afbeeldingscatalogus](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
