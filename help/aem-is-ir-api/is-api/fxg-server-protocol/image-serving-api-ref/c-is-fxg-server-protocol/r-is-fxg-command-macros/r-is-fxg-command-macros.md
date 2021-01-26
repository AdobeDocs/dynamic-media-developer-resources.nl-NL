---
description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
seo-description: De macro's van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.
seo-title: Opdrachtmacro's
solution: Experience Manager
title: Opdrachtmacro's
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Command macros{#command-macros}

De macro&#39;s van het bevel verstrekken genoemde kortere weg voor reeksen bevelen.

Macro&#39;s worden gedefinieerd in afzonderlijke macrodefinitiebestanden, die kunnen worden gekoppeld aan afbeeldingscatalogi of de standaardcatalogus.

Macro&#39;s kunnen overal in een verzoek na &#39;?&#39;, evenals overal binnen een `catalog::Modifier` gebied worden aangehaald. Macro&#39;s kunnen slechts één of meerdere volledige bevelen vertegenwoordigen van de Dienstverlening van het Beeld, daarom moet door (&amp;) separators worden ingesloten (behalve wanneer aan het begin of het eind van het bepalingskoord).

Macro-aanroepen worden tijdens het parseren vervangen door hun vervangende tekenreeksen. Opdrachten binnen macro&#39;s overschrijven dezelfde opdrachten in de aanvraag als deze vóór de macroactivering in de aanvraag worden uitgevoerd. Dit verschilt van `catalog::Modifier`, waar de bevelen in het verzoekkoord altijd bevelen in het `catalog::Modifier` koord zullen met voeten treden, ongeacht positie in het verzoek.

Macro&#39;s kunnen worden genest, met de volgende beperking: een macro kan alleen worden aangeroepen als deze al is gedefinieerd op het moment dat de macrodefinitie wordt geparseerd, door deze eerder in hetzelfde macrodefinitiebestand te plaatsen of door de definitie voor een dergelijke ingesloten macro in het standaard macrodefinitiebestand te plaatsen.

Macro&#39;s kunnen handig zijn als dezelfde kenmerken op verschillende afbeeldingen moeten worden toegepast.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Wij kunnen een macro voor de gemeenschappelijke attributen bepalen:

`view wid=240&fmt=pdf&imageRes=300`

De macro wordt als volgt gebruikt:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Aangezien `wid=` voor het derde verzoek verschillend is, wij eenvoudig de waarde *after* met voeten treden wordt de macro aangehaald (specificerend `wid=`*before* `$view$` zou geen effect hebben).

+ [name](r-name.md)
