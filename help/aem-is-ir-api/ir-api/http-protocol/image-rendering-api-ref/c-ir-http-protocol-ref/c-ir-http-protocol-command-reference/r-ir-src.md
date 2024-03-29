---
title: src
description: Materiaalbestand. Hiermee worden materiaalgegevens opgegeven, in de vorm van één materiaalcatalogusverwijzing of als een of twee afbeeldings- of materiaalgegevensbestanden, gescheiden met een komma.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# src{#src}

Materiaalbestand. Hiermee worden materiaalgegevens opgegeven, in de vorm van één materiaalcatalogusverwijzing of als een of twee afbeeldings- of materiaalgegevensbestanden, gescheiden met een komma.

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;Accolade;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;Broce;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>&amp;Broce;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;resource;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>Materiaalcatalogus-id (<span class="codeph"> kenmerk::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Materiaalcatalogusitem (<span class="codeph"> catalogus::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Materiaalstijlbestand (<span class="filepath"> .vnc</span> of <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Afbeeldingsgegevensbestand. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Verzoek om beeldbewerking. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Verzoek om beeldweergave. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Aanvraag bij een externe server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Naam van een ingesloten materiaal. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Op 0 gebaseerd indexnummer voor een ingesloten materiaal. </p></td> 
 </tr> 
</table>

Voor herhaalbare Texture-, Decal- en Wallpaper-materialen is één afbeelding vereist, die kan worden opgegeven als een bestand of een ingesloten aanvraag.

Voor kabinetsmateriaal is een bestand met een kabinetstijl vereist ( [!DNL .vnc]), die niet als een geneste aanvraag kan worden opgegeven. Een bestand met een structuurafbeelding is optioneel voor kabinetten en kan, indien opgegeven, een bestand of een ingesloten aanvraag zijn.

Voor materiaal voor vensterbekleding is een stijlbestand voor vensterbekleding vereist ( [!DNL .vnw]), die niet als een geneste aanvraag kan worden opgegeven. Een structuurbestand is optioneel en kan, indien opgegeven, een bestand of een ingesloten aanvraag zijn.

Voor het renderen van afbeeldingen worden dezelfde regels gebruikt als voor het weergeven van afbeeldingen, zodat u materiaalcatalogi, catalogusitems en gegevensbestanden kunt opzoeken. Zie de beschrijving van de *`object`* Gegevenstype in de documentatie van de Beeldserver voor meer informatie.

*`materialFile`* Is een pad ten opzichte van `attribute::RootPath`.

*`foreignReq`* Kan een URL zijn die betrekking heeft op `attribute::RootUrl`of een absolute URL als `attribute::AllowDirectUrls` is ingesteld.

Indien *`catId`* niet is opgegeven, wordt de sessiecatalogus gebruikt.

`srcE=` en `srcN=` toegang bieden tot materialen die zijn ingesloten in het vignet.

## Ondersteunde bestandsindelingen {#section-f2186d3eef834fc8bbecb2bc68daacad}

Renderen van afbeeldingen ondersteunt dezelfde bronafbeeldingsindelingen als Dynamic Media Image Serving.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het best als de indeling voor meerresolutie van Scene7 piramid TIFF (PTIFF) wordt gebruikt. De Beeldserver omvat het hulpmiddel van de Omzetter van het Beeld (IC) dat tot beelden PTIFF van om het even welk gesteund formaat leidt.

Raadpleeg de beschrijving van het IC-hulpprogramma in de documentatie van Image Serving voor een volledige lijst met ondersteunde bestandsindelingen.

## Eigenschappen {#section-e68d03788d534e2184147987d51dfd0f}

Materiaalkenmerk. Vereist voor alle materialen behalve effen kleuren (niet toegestaan voor effen kleurstoffen). Alle tekenreeksen zijn hoofdlettergevoelig. *`index`* Moet 0 of groter zijn.

## Standaard {#section-dde549c1917540dc8f9555962202da3c}

Geen.

## Voorbeeld {#section-675865444f8a4d35b9fc6e58b36e3438}

Een MSS voor een gekleurde kast met een afzonderlijke herhaalbare structuur:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Hetzelfde materiaal kan zich in een materiaalcatalogus bevinden `'cat`&#39; in record &#39; `12-3-2`&quot;:

`…&obj=cabinets&src=cat/12-3-2&…`

Een geneste aanvraag voor een afbeelding in de afbeeldingsserver om een structuurafbeelding te verkrijgen:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Zie ook {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Materiaalcatalogi](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [kenmerk:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [kenmerk::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
