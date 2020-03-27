---
description: Type aanvraag. Hier geeft u het type gevraagde gegevens op.
seo-description: Type aanvraag. Hier geeft u het type gevraagde gegevens op.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

Type aanvraag. Hier geeft u het type gevraagde gegevens op.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> foutopsporing </span> </p> </td> 
  <td class="stentry"> <p>Voer opdrachten uit in de foutopsporingsmodus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> inhoud </span> </p> </td> 
  <td class="stentry"> <p>Retourneer informatie over de objecten in het vignet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Voer de opdrachten uit en retourneer de gerenderde afbeelding. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Retourneert eigenschappen van het opgegeven vignet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> map </span> </p> </td> 
  <td class="stentry"> <p>Retourneert afbeeldingskaartgegevens die zijn ingesloten in het vignet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>Voer de opdrachten uit en retourneer de gerenderde afbeelding die is gemaskeerd aan de huidige objectselectie. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Voer de opdrachten uit en retourneer de eigenschappen van de antwoordafbeelding. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> gebruikersgegevens </span> </p> </td> 
  <td class="stentry"> <p>Retourneert de inhoud van <span class="codeph"> vignet::UserData </span>. </p> </td> 
 </tr> 
</table>

Tenzij anders vermeld in de gedetailleerde beschrijvingen, retourneert de server tekstreacties met het MIME-type &lt;text/plain>.

`debug`

Voert de opgegeven opdrachten uit en retourneert de gerenderde afbeelding. Als er een fout optreedt, worden de fout- en foutopsporingsgegevens geretourneerd in plaats van de foutafbeelding ( `attribute::ErrorImagePath`).

`contents`

Retourneert een XML-representatie van de objecthiërarchie in het vignet, inclusief geselecteerde objectkenmerken. Andere opdrachten in de aanvraag worden genegeerd.

`img`

Voert de opgegeven opdrachten uit en retourneert de gerenderde afbeelding. Het formaat van antwoordgegevens en het reactietype worden bepaald door `fmt=`.

`imageprops`

Hiermee worden de geselecteerde eigenschappen geretourneerd van het vignetbestand of de catalogusvermelding die is opgegeven in het URL-pad. Zie [Eigenschappen](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) voor een beschrijving van de antwoordsyntaxis en het type response MIME. Andere opdrachten in de aanvraag worden genegeerd. De volgende eigenschappen worden geretourneerd:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Dubbel </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk::Expiration </span> of de standaardtijd om te leven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Geheel </p> </td> 
   <td colname="col3"> <p>Hoogte volledige resolutie in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>naam/beschrijving van het profiel dat aan dit vignet is gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 als het bijbehorende profiel is ingesloten in het vignet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 als het vignet padgegevens insluit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk::Modifier </span> of leeg als er geen item uit de catalogus is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Pixeltype van de reactieafbeelding; kan 'CMYK', 'RGB' of 'BW' zijn (voor grijswaardenafbeeldingen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Standaardafdrukresolutie in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Wijzigingsdatum/-tijd (uit <span class="codeph"> catalogus::TimeStamp </span> of het vignetbestand). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Geheel </p> </td> 
   <td colname="col3"> <p>Breedte volledige resolutie in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignet.name </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Vignetnaam (naamreeks van het hoofdvignetobject). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignet.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Maximale objectresolutie in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materiaalresolutie- </a> eenheden (doorgaans pixels/inch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignet.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Gemiddelde objectresolutie in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materiaalresolutie- </a> eenheden (doorgaans pixels/inch <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materiaalresolutie </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignet.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Minimale objectresolutie in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materiaalresolutie- </a> eenheden (doorgaans pixels/inch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignet.version </span> </p> </td> 
   <td colname="col2"> <p>Geheel </p> </td> 
   <td colname="col3"> <p>Versie van vignetbestand. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Retourneert de afbeeldingskaartgegevens die in het vignet zijn opgenomen. Standaard worden de kaartgegevens voor alle buitenste groepen geretourneerd. De kaartgegevens voor alle binnenste groepen kunnen worden verkregen met

`req=map&groupLevel=-1`

De kaartgegevens worden niet geschaald naar `wid=` of `hei=` of anderszins gewijzigd. Het MIME-type van de reactie is `<text/xml>`.

De reactiegegevens bestaan uit een `<map>` element met een set `<area>` elementen, vergelijkbaar met de HTML- `<AREA>` tag.

Elk `<area>` element bevat de standaard `type=` - en `coord=` kenmerken, evenals een `name=` kenmerk dat de naam of het naampad van de vignetgroep opgeeft. Er zijn meerdere `<area>` elementen met dezelfde naam als de maskers van de overeenkomende objectgroep onderbroken gebieden hebben.

Naast de standaardkenmerken kunnen vignetten indien nodig aanvullende kenmerken definiëren. Dergelijke aangepaste kenmerken worden gedefinieerd als objectgroepkenmerken. De namen van aangepaste kenmerken moeten beginnen met `map`. in de `<area>` elementen op te nemen. Als de groepskenmerken bijvoorbeeld de kenmerken bevatten, bevat het overeenkomende `map.href=http://www.scene7.com`element ook `<area>` het element `href="http://www.scene7.com"`.

Een XML-document met een leeg `<map>` element wordt geretourneerd als het vignet geen kaartgegevens bevat.

`object`

Voert de opgegeven opdrachten uit en retourneert de gerenderde afbeelding die is gemaskeerd door de selectie van het resterende object (de groep of het object dat is geselecteerd met de laatste `sel=` of `obj=` opdracht in de aanvraag). Wordt meestal gebruikt in combinatie met een afbeeldingsindeling die alfa ondersteunt (zie [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Als een afbeeldingsindeling wordt gebruikt die geen alfa ondersteunt, zijn de gebieden buiten het masker zwart.

`props`

Voert de opgegeven opdrachten uit en retourneert vigneteigenschappen en groep- of objecteigenschappen in plaats van de gerenderde afbeelding. Zie [Eigenschappen](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) voor een beschrijving van de antwoordsyntaxis en het MIME-type van het antwoord. De standaardselectie is van toepassing, tenzij `obj=` of `sel=` ook opgegeven (zie [ `obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

De volgende eigenschappen kunnen in de reactie worden opgenomen:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Eigenschap </p> </th> 
   <th class="entry"> <p> Type </p> </th> 
   <th class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Achtergrondkleur afbeelding beantwoorden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Geheel </p> </td> 
   <td> <p> Hoogte van afbeelding reageren in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True if the ICC profile will be embedded in the response image (see <span class="codeph"> iccEmbed= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Naam van snelkoppeling van het profiel dat is gekoppeld aan de antwoordafbeelding (zie <span class="codeph"> icc= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True if the response image includes alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True if the response image includes path data (see <span class="codeph"> pathEmbed= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Afbeeldingstype Reageren, kan 'CMYK', 'RGB' of 'BW' zijn (voor grijswaardenafbeeldingen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Afdrukresolutie (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Geheel getal, Boolean </p> </td> 
   <td> <p> JPEG-markering voor kwaliteit en chroom (zie <span class="codeph"> qlt= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> MIME-type voor de antwoordafbeelding (zie <span class="codeph"> fmt= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> Breedte van afbeelding beantwoorden in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Kenmerktekenreeks voor de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> Aantal objecten in de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selectie.incident </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> Inspringingswaarde van de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Pad met volledige naam van de huidige objectselectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selectie.overlappen </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> aantal overlappende objecten in de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p>Aantal renderbare objecten in de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selectie.tekentabel </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> Aantal tekstuele objecten in de huidige selectie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> Huidige status van de huidige selectie tonen/verbergen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Geheel </p> </td> 
   <td> <p> De Z-volgorde van het eerste overlappende object in de huidige selectie. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Retourneert de inhoud van `vignette::UserData`. De server vervangt alle instanties van `'??'` in `vignette::UserData` door regeleinders ( `<cr><lf>`). De reactie is opgemaakt als tekstgegevens met het MIME-type van het antwoord ingesteld op &lt;text/plain>.

Als het object dat is opgegeven in het URL-pad niet wordt omgezet in een geldig item voor een vignettoewijzing, of als het object leeg `vignette::UserData` is, bevat het antwoord alleen een regelafsluiter ( `CR/LF`).

Eventuele andere opdrachten in de tekenreeks request worden genegeerd.

## Eigenschappen {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Verzoek, opdracht. Kan overal in het verzoekkoord voorkomen.

## Standaard {#section-00c593cbf1af4364b6b78812e6b93c64}

Als de URL geen afbeeldingspad of wijzigingstoetsen bevat, geldt het volgende:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Anders, `req=img`

## Zie ook {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignet::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
