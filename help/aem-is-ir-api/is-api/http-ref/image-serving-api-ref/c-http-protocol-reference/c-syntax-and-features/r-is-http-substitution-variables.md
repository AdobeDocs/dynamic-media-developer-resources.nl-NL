---
description: Vervangende variabelen worden gebruikt om waarden van verzoekURL naar samenstellende malplaatjes over te brengen die in beeldcatalogi worden opgeslagen. U kunt ook variabelen gebruiken om dezelfde waarde over te brengen naar verschillende plaatsen in een complexe aanvraag.
solution: Experience Manager
title: Vervangende variabelen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Vervangende variabelen{#substitution-variables}

Vervangende variabelen worden gebruikt om waarden van verzoekURL naar samenstellende malplaatjes over te brengen die in beeldcatalogi worden opgeslagen. U kunt ook variabelen gebruiken om dezelfde waarde over te brengen naar verschillende plaatsen in een complexe aanvraag.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Naam variabele. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Waarde waarop de variabele moet worden ingesteld (tekenreeks). </p> </td> 
 </tr> 
</table>

De veranderlijke definities en de verwijzingen kunnen in het vraaggedeelte van het verzoek voorkomen, in `catalog::Modifier`, en in `catalog::PostModifier`.

Variabelen worden als hierboven gedefinieerd, net als andere IS-opdrachten. De regelafstand &#39;$&#39; geeft de opdracht aan als een variabele definitie. Variabelen moeten worden gedefinieerd voordat er naar wordt verwezen.

De variabelenaam *`var`* is niet hoofdlettergevoelig en kan bestaan uit een combinatie van ASCII-letters, -cijfers, &#39;-&#39;, &#39;_&#39; en &#39;.&#39;.

>[!NOTE]
>
>*`value`* moet URL-gecodeerd voor één controle zijn voor veilige HTTP-verzending. Dubbele codering is vereist als *`value`* wordt opnieuw verzonden via HTTP. Dit is het geval wanneer *`value`* wordt vervangen in een geneste buitenlandse aanvraag of in het href-kenmerk van een SVG `<image>` element.

Variabele-verwijzingen bestaan uit de variabelenaam gescheiden door het regelafstand en het nakomen &#39;$&#39; ($)*var*$). Verwijzingen kunnen overal in het waardegedeelte van om het even welke bevelen van IS voorkomen (namelijk tussen &#39;=&#39; na de bevelnaam en verdere &#39;&amp;&#39; of het eind van het verzoek). Aangepaste variabelen kunnen niet worden toegepast op de `layer=` en `effect=` opdrachten. Meerdere variabelen zijn toegestaan in dezelfde opdrachtwaarde. De server vervangt elke instantie van ` $ *`var`*$` with *`value`*.

Variabeleverwijzingen mogen niet genest zijn. Alle exemplaren van ` $ *`var`*$` binnen *`value`* niet vervangen.

Het aanvraagfragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

lost op aan:

`text=my$var2$tree`

>[!NOTE]
>
>‘$’ is geen gereserveerd teken; dit komt anders voor in het verzoek. Bijvoorbeeld: `src=my$image$file.tif` is een geldige opdracht (ervan uitgaande dat een item of afbeeldingsbestand met de naam van een catalogus `my$image$file.tif` bestaat), while `wid=$number$` is niet, omdat `wid` vereist een numeriek argument.

## Variabele verwerking in geneste aanvragen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beelddienst of Beeld teruggeven verzoek voorkomen, met inbegrip van links van &#39;?? het pad scheiden van de query. De server vervangt deze verwijzingen door waarden (van de URL of van `catalog::Modifier` (van de hoofdafbeeldingscatalogus) voordat de geneste aanvraag verder wordt geparseerd en verwerkt.

Bovendien ` $ *`var`*=` definities van de URL of `catalog::Modifier` worden doorgestuurd naar alle aanvragen voor geneste beeldservers en het renderen van afbeeldingen. Dit zorgt ervoor dat alle veranderlijke definities aan alle malplaatjes, ongeacht het nestelen niveau beschikbaar zijn.

Ongeacht het nestniveau moet alleen HTTP-codering met één controle worden toegepast op variabelewaarden die overal in geneste aanvragen voor het renderen van afbeeldingen of de bijbehorende verzoeken moeten worden vervangen `catalog::Modifier` tekenreeksen.

## Variabele verwerking in ingesloten externe verzoeken {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` verwijzingen die ergens binnen de accolades van een ingesloten extern verzoek voorkomen, worden vervangen door overeenkomstige waarden voor de definitie van variabelen. Hierdoor kunnen ingesloten externe verzoeken in een sjabloon in een afbeeldingscatalogus worden geplaatst.

De veranderlijke waarden die in buitenlandse verzoeken moeten worden vervangen moeten typisch dubbel-gecodeerd zijn, aangezien geen hercodering wordt toegepast alvorens de server probeert om definitieve buitenlandse url over te brengen.

## Variabele verwerking in SVG-bestanden {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` verwijzingen kunnen voorkomen in SVG dossiers in attributenwaarden en in `<text>` tekenreeksen. In afbeeldingsserver worden deze vervangen door de overeenkomende ` $ *`var`*=` definities die bekend zijn op het nestingniveau van het verzoek waarop het SVG-bestand wordt opgegeven.

>[!NOTE]
>
>Elke variabele die in een `href` kenmerkwaarde moet dubbel-URL-gecodeerd zijn; alle anderen moeten afzonderlijk worden gecodeerd.

## Vooraf gedefinieerde padvariabele {#section-930d0dd12e8f49499becc9fe8df24092}

De *`object`* opgegeven in het aanvraagpad wordt toegewezen aan de vooraf gedefinieerde variabele `*`$object`*`. &#39; ` $ *`object`*$`&#39; kan ergens in de aanvraag worden geplaatst, in de sjabloon waarnaar door de aanvraag wordt verwezen, of in een geneste/ingesloten aanvraag waar een dergelijk object is toegestaan, inclusief de waarde van `src=` en `mask=`en het pad van een geneste/ingesloten aanvraag.

In het volgende verzoek wordt bijvoorbeeld de afbeelding die in het pad is opgegeven, opnieuw gebruikt als bron van een laag in een geneste aanvraag:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dit is gelijk aan

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

De definitie van `*`$object`*` kan worden overschreven door expliciet ` $ *`object`*=` met de gewenste waarde.

De vooraf gedefinieerde padvariabele wordt doorgaans gebruikt in combinatie met `template=`.

## Standaard {#section-b02483d15529444586a2e9504805b155}

Geen. Alleen variabelen die zijn gedefinieerd, worden vervangen door de server (behalve de vooraf gedefinieerde padvariabele $object, die altijd wordt vervangen). Alle exemplaren van ` $ *`var`*$` letterlijk blijven als `*`var`*`kan niet met een bestaande veranderlijke definitie worden aangepast.

## Voorbeelden {#section-fba9393df6984247b7e30b3f93992e86}

Zie &quot;Voorbeeld A&quot; in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Zie ook {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
