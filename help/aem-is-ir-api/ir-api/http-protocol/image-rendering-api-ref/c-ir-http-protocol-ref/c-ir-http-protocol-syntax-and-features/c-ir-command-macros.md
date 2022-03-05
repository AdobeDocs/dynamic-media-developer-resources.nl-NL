---
title: Opdrachtmacro's
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Opdrachtmacro&#39;s{#command-macros}

De macro&#39;s van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Macronaam

Macro&#39;s worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan materiaalcatalogi of de standaardcatalogus.

*[!DNL name]* is niet hoofdlettergevoelig en kan bestaan uit elke combinatie van ASCII-letters, -cijfers , &#39;-&#39;, &#39;_&#39; en &#39;.&#39; tekens.

Macro&#39;s overal in een verzoek aanroepen na &#39;?&#39; of ergens in een `vignette::Modifier` veld. Macro&#39;s kunnen slechts een of meer opdrachten voor het renderen van afbeeldingen vertegenwoordigen en moeten worden gescheiden van andere opdrachten met scheidingstekens &#39;&amp;&#39;.

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Deze workflow verschilt van `vignette::Modifier`, waarbij opdrachten in de tekenreeks request de opdrachten in de `vignette::Modifier` tekenreeks, ongeacht de positie in de aanvraag.

Opdrachtmacro&#39;s kunnen geen argumentwaarden hebben, maar aangepaste variabelen kunnen worden gebruikt om waarden van de aanvraag in de macro door te geven.

Macro&#39;s mogen niet genest zijn.

**Voorbeeld**

Macro&#39;s kunnen handig zijn als dezelfde opdrachten of kenmerken moeten worden toegepast op verschillende gerenderde afbeeldingen.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

U kunt een macro definiëren voor de algemene kenmerken:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

De macro wordt als volgt gebruikt:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Omdat `qlt=` is verschillend voor het derde verzoek, treedt de software de waarde met voeten nadat de macro wordt aangehaald (specificerend `qlt=` *voor* `$render$`is niet effectief).

**Zie ook**

`catalog::MacroFile`, `catalog::Modifier`, Macrodefinitieverwijzing

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
