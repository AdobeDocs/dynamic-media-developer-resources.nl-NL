---
title: Command macros
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Command macros{#command-macros}

De macro&#39;s van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.

Macro&#39;s worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.

Macro&#39;s kunnen overal in een verzoek na &quot;?&quot;worden aangehaald, en overal binnen een `catalog::Modifier` veld. Macro&#39;s kunnen slechts één of meerdere volledige bevelen vertegenwoordigen van de Dienstverlening van het Beeld, daarom moet het door (&amp;) separators worden ingesloten (behalve wanneer aan het begin of het eind van het bepalingskoord).

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Deze stroom is anders dan `catalog::Modifier`, waarbij opdrachten in de tekenreeks request altijd opdrachten in de `catalog::Modifier` tekenreeks, ongeacht de positie in de aanvraag.

Macro&#39;s kunnen worden genest. Een macro kan echter alleen worden aangeroepen als deze al is gedefinieerd op het moment dat de macrodefinitie wordt geparseerd. Deze stroom wordt verwezenlijkt of door vroeger in het zelfde macrodefinitiedossier te verschijnen, of door de definitie voor zulk een ingebedde macro in het standaard macrodefinitiedossier te plaatsen.

Macro&#39;s kunnen handig zijn als dezelfde kenmerken op verschillende afbeeldingen moeten worden toegepast.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

U kunt een macro definiëren voor de algemene kenmerken:

`view wid=240&fmt=pdf&imageRes=300`

De macro wordt als volgt gebruikt:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Omdat `wid=` is anders voor de derde aanvraag. U overschrijft gewoon de waarde *na* de macro wordt aangeroepen (specificeren `wid=` *voor* `$view$` heeft geen effect).

+ [name](r-name.md)
