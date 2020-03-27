---
description: Vervangende variabelen worden gebruikt om waarden van verzoekURL naar samenstellende malplaatjes over te brengen die in beeldcatalogi worden opgeslagen. U kunt ook variabelen gebruiken om dezelfde waarde over te brengen naar verschillende plaatsen in een complexe aanvraag.
seo-description: Vervangende variabelen worden gebruikt om waarden van verzoekURL naar samenstellende malplaatjes over te brengen die in beeldcatalogi worden opgeslagen. U kunt ook variabelen gebruiken om dezelfde waarde over te brengen naar verschillende plaatsen in een complexe aanvraag.
seo-title: Vervangende variabelen
solution: Experience Manager
title: Vervangende variabelen
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vervangende variabelen{#substitution-variables}

Vervangende variabelen worden gebruikt om waarden van verzoekURL naar samenstellende malplaatjes over te brengen die in beeldcatalogi worden opgeslagen. U kunt ook variabelen gebruiken om dezelfde waarde over te brengen naar verschillende plaatsen in een complexe aanvraag.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>Naam variabele. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> waarde </span></span> </p> </td> 
  <td class="stentry"> <p>Waarde waarop de variabele moet worden ingesteld (tekenreeks). </p> </td> 
 </tr> 
</table>

Variabele definities en verwijzingen kunnen voorkomen in het vraaggedeelte van het verzoek, in `catalog::Modifier`, en in `catalog::PostModifier`.

Variabelen worden gedefinieerd als hierboven, vergelijkbaar met andere IS-opdrachten; de regelafstand &#39;$&#39; geeft de opdracht aan als een variabele definitie. Variabelen moeten worden gedefinieerd voordat er naar wordt verwezen.

De variabelenaam *`var`* is niet hoofdlettergevoelig en kan bestaan uit een willekeurige combinatie van ASCII-letters, getallen, &#39;-&#39;, &#39;_&#39; en &#39;.&#39;.

>[!NOTE]
>
>*`value`* moet URL-gecodeerd voor één controle zijn voor veilige HTTP-verzending. Dubbele codering is vereist als de gegevens opnieuw via HTTP *`value`* worden verzonden. Dit is het geval wanneer *`value`* een geneste externe aanvraag of het href-kenmerk van een SVG- `<image>` element wordt vervangen.

Variabeleverwijzingen bestaan uit de naam van de variabele die wordt afgebakend door het voorloopteken en navolgend &#39;$&#39; ($*var*$). Verwijzingen kunnen overal in het waardegedeelte van om het even welke bevelen van IS voorkomen (d.w.z. tussen &#39;=&#39; na de bevelnaam en verdere &#39;&amp;&#39; of het eind van het verzoek). Aangepaste variabelen kunnen niet worden toegepast op de opdrachten `layer=` en `effect=` opdrachten. Meerdere variabelen zijn toegestaan in dezelfde opdrachtwaarde. De server vervangt elke instantie van ` $ *`var`*$` door *`value`*.

Variabeleverwijzingen mogen niet genest zijn. Elke gebeurtenis van ` $ *`var`*$` binnen *`value`* wordt niet vervangen.

Het aanvraagfragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

lost op aan:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; is geen gereserveerd teken; het kan anders in het verzoek voorkomen. Dit `src=my$image$file.tif` is bijvoorbeeld een geldige opdracht (ervan uitgaande dat een catalogusitem of afbeeldingsbestand met de naam `my$image$file.tif` bestaat), maar `wid=$number$` niet omdat een numeriek argument `wid` vereist is.

## Variabele verwerking in geneste aanvragen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`Var`*$` verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beelddienst of Beeld teruggeven verzoek voorkomen, met inbegrip van links van &#39;?? het pad scheiden van de query. Deze verwijzingen worden door de server vervangen door waarden (van de URL of van de hoofdafbeeldingscatalogus) voordat de geneste aanvraag verder wordt geparseerd en verwerkt. `catalog::Modifier`

Daarnaast worden alle ` $ *`var`*=` -definities van de URL of `catalog::Modifier` doorgestuurd naar alle geneste aanvragen voor Beeldbewerking en Afbeelding renderen. Dit zorgt ervoor dat alle veranderlijke definities aan alle malplaatjes, ongeacht het nestelen niveau beschikbaar zijn.

Ongeacht het nestingniveau, moet slechts single-pass HTTP-codering op veranderlijke waarden worden toegepast die overal in genestelde het Teruggeven van het Beeld of Beeld dienen verzoeken of hun bijbehorende `catalog::Modifier` koorden moeten worden vervangen.

## Variabele verwerking in ingesloten externe verzoeken {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` references occur Anywhere within the curly braces of an embedded foreign request are substitued with matching variable definition values. Hierdoor kunnen ingesloten externe verzoeken in een sjabloon in een afbeeldingscatalogus worden geplaatst.

De veranderlijke waarden die in buitenlandse verzoeken moeten worden vervangen moeten typisch dubbel-gecodeerd zijn, aangezien geen hercodering wordt toegepast alvorens de server probeert om definitieve buitenlandse url over te brengen.

## Variabele verwerking in SVG-bestanden {#section-a8359f9909764142b6a18ae778dca913}

` $ *`In SVG-bestanden kunnen var`*$` -verwijzingen voorkomen in kenmerkwaarden en in `<text>` tekenreeksen. Image Serving vervangt deze door de overeenkomende ` $ *`var`*=` -definities die bekend zijn op het nestingniveau van het verzoek waarbij het SVG-bestand wordt opgegeven.

>[!NOTE]
>
>Elke waarde van een variabele die in een `href` kenmerkwaarde moet worden vervangen, moet een dubbele URL-codering hebben. alle andere moeten afzonderlijk worden gecodeerd.

## Vooraf gedefinieerde padvariabele {#section-930d0dd12e8f49499becc9fe8df24092}

Het *`object`* opgegeven aanvraagpad wordt toegewezen aan de vooraf gedefinieerde variabele ` *`$object`*`. &#39; ` $ *`object`*$`&#39; kan ergens in de aanvraag worden geplaatst, in de sjabloon waarnaar door de aanvraag wordt verwezen, of in een geneste/ingesloten aanvraag waar een dergelijk object is toegestaan, inclusief de waarde van `src=` en `mask=`, en het pad van een geneste/ingesloten aanvraag.

De volgende aanvraag gebruikt bijvoorbeeld de afbeelding die in het pad is opgegeven als bron van een laag in een geneste aanvraag:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dit is gelijk aan

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

De definitie van ` *`$object`*` kan worden overschreven door expliciet een ` $ *`object`*=` met de gewenste waarde op te geven.

De vooraf gedefinieerde padvariabele wordt meestal gebruikt in combinatie met `template=`.

## Standaard {#section-b02483d15529444586a2e9504805b155}

Geen. Alleen variabelen die zijn gedefinieerd, worden vervangen door de server (behalve de vooraf gedefinieerde padvariabele $object, die altijd wordt vervangen). Elk voorkomen van ` $ *`var`*$` blijft letterlijk als ` *``*`variabele niet kan worden aangepast met een bestaande definitie van variabele.

## Voorbeelden {#section-fba9393df6984247b7e30b3f93992e86}

Zie &quot;Voorbeeld A&quot; in [sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [sjabloon=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
