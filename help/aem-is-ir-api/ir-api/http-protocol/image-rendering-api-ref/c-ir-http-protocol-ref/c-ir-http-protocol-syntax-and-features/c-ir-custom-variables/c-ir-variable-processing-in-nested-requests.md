---
description: $var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van '? voorkomen het pad scheiden van de query.
solution: Experience Manager
title: Variabele verwerking in geneste aanvragen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Variabele verwerking in geneste aanvragen{#variable-processing-in-nested-requests}

$var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van &#39;? voorkomen het pad scheiden van de query.

Deze verwijzingen worden door de server vervangen door waarden (van de URL of van `catalog::Modifier` van de hoofdafbeeldingscatalogus) voordat de geneste aanvraag verder wordt geparseerd en verwerkt.

Daarnaast worden alle `$ *[!DNL var]*=`-definities van de URL en `catalog::Modifier` doorgestuurd naar alle geneste aanvragen voor beeldbewerking en het renderen van afbeeldingen. Dit zorgt ervoor dat alle veranderlijke definities aan alle malplaatjes, ongeacht het nestelen niveau beschikbaar zijn.

Ongeacht het nestniveau, slechts single-pass HTTP-codering moet op veranderlijke waarden worden toegepast die overal in genestelde het Teruggeven van het Beeld of Beeld het Serven verzoeken moeten worden vervangen.
