---
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
seo-description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
seo-title: Command macros *
solution: Experience Manager
title: Command macros *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# Command macros *{#command-macros}

De macro&#39;s van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Macronaam

Macro&#39;s worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan materiaalcatalogi of de standaardcatalogus.

*[!DNL name]* is niet hoofdlettergevoelig en kan bestaan uit elke combinatie van ASCII-letters, -cijfers , &#39;-&#39;, &#39;_&#39; en &#39;.&#39; tekens.

U kunt macro&#39;s overal aanroepen in een aanvraag na &#39;?&#39; of ergens in een veld `vignette::Modifier`. Macro&#39;s kunnen slechts een of meer volledige opdrachten voor het renderen van afbeeldingen vertegenwoordigen en moeten van andere opdrachten worden gescheiden met scheidingstekens &#39;&amp;&#39;.

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Dit verschilt van `vignette::Modifier`, waar de bevelen in het verzoekkoord altijd bevelen in het `vignette::Modifier` koord zullen met voeten treden, ongeacht de positie in het verzoek.

Opdrachtmacro&#39;s kunnen geen argumentwaarden hebben, maar aangepaste variabelen kunnen worden gebruikt om waarden van de aanvraag in de macro door te geven.

Macro&#39;s mogen niet genest zijn.

**Voorbeeld**

Macro&#39;s kunnen handig zijn als dezelfde opdrachten of kenmerken moeten worden toegepast op verschillende gerenderde afbeeldingen.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

U kunt een macro definiëren voor de algemene kenmerken:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

De macro wordt als volgt gebruikt:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Aangezien `qlt=` voor het derde verzoek verschillend is, treden wij eenvoudig de waarde met voeten nadat de macro wordt aangehaald (specificerend `qlt=`*before* `$render$`zou geen effect hebben).

**Zie ook**

`catalog::MacroFile`,  `catalog::Modifier`macrodefinitie

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

