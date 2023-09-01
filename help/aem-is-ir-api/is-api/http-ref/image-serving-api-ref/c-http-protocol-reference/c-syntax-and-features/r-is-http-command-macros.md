---
title: Command macros
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen. Macro's worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Command macros{#command-macros}

De macro&#39;s van het bevel verstrekken genoemde kortere weg voor reeksen bevelen. Macro&#39;s worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Naam macro. </p></td> 
 </tr> 
</table>

`*`name`*` is niet hoofdlettergevoelig en kan bestaan uit een combinatie van ASCII-letters, -cijfers , &#39;-&#39;, &#39;_&#39; en &#39;.&#39; tekens.

Macro&#39;s kunnen overal in een verzoek na &quot;?&quot;worden aangehaald, en overal binnen een `catalog::Modifier` of `catalog::PostModifier` veld. Macro&#39;s kunnen slechts één of meerdere, volledige, het Serven van het Beeld bevelen vertegenwoordigen, en moeten van andere bevelen met worden gescheiden `&` scheidingstekens.

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Deze verwerkingsstroom verschilt van `catalog::Modifier`, waarbij opdrachten in de tekenreeks request altijd opdrachten in de `catalog::Modifier` tekenreeks, ongeacht de positie in de aanvraag.

Opdrachtmacro&#39;s kunnen geen argumentwaarden hebben, maar aangepaste variabelen kunnen worden gebruikt om waarden van de aanvraag in de macro door te geven.

Macro&#39;s kunnen zijn genest. Een macro kan echter alleen worden aangeroepen als deze al is gedefinieerd op het moment dat de macrodefinitie wordt geparseerd. Deze workflow wordt uitgevoerd door eerder in hetzelfde macrodefinitiebestand te verschijnen of door de definitie voor een dergelijk ingesloten macro in het standaard macrodefinitiebestand te plaatsen.

## Voorbeeld {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Macro&#39;s kunnen handig zijn als dezelfde kenmerken op verschillende afbeeldingen moeten worden toegepast.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

U kunt een macro definiëren voor de algemene kenmerken:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

De macro wordt als volgt gebruikt:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Omdat `wid=` is anders voor de derde aanvraag. U kunt gewoon de waarde overschrijven *na* de macro wordt aangeroepen (specificeren `wid=`*voor* `$view$` heeft geen effect).

## Zie ook {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalogus::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalogus::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Referentie macrodefinitie](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
