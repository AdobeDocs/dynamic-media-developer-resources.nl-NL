---
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen. Macro's worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.
seo-description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen. Macro's worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.
seo-title: Opdrachtmacro's
solution: Experience Manager
title: Opdrachtmacro's
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '342'
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

` *`De `*` naam is niet hoofdlettergevoelig en kan bestaan uit een combinatie van ASCII-letters, getallen, &#39;-&#39;, &#39;_&#39; en &#39;.&#39; tekens.

Macro&#39;s kunnen overal in een verzoek na &quot;?&quot;worden aangehaald, evenals overal binnen een `catalog::Modifier` of `catalog::PostModifier` gebied. Macro&#39;s kunnen slechts een of meer volledige opdrachten in de afbeeldingsserver vertegenwoordigen en moeten van andere opdrachten worden gescheiden met scheidingstekens &#39;&amp;&#39;.

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Dit verschilt van `catalog::Modifier`, waar de bevelen in het verzoekkoord altijd bevelen in het `catalog::Modifier` koord zullen met voeten treden, ongeacht positie in het verzoek.

Opdrachtmacro&#39;s kunnen geen argumentwaarden hebben, maar aangepaste variabelen kunnen worden gebruikt om waarden van de aanvraag in de macro door te geven.

Macro&#39;s kunnen worden genest, met de volgende beperking: Een macro kan alleen worden aangeroepen als deze al is gedefinieerd op het moment dat de macrodefinitie wordt geparseerd, door eerder in hetzelfde macrodefinitiebestand te verschijnen of door de definitie voor een dergelijke ingesloten macro in het standaard macrodefinitiebestand te plaatsen.

## Voorbeeld {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Macro&#39;s kunnen handig zijn als dezelfde kenmerken op verschillende afbeeldingen moeten worden toegepast.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Wij kunnen een macro voor de gemeenschappelijke attributen bepalen:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

De macro wordt als volgt gebruikt:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Aangezien `wid=` voor het derde verzoek verschillend is, wij eenvoudig de waarde *after* met voeten treden wordt de macro aangehaald (specificerend `wid=`*before* `$view$` zou geen effect hebben).

## Zie ook {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md),  [Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
