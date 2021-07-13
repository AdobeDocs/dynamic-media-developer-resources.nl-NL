---
description: $var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van '? voorkomen het pad scheiden van de query.
solution: Experience Manager
title: Variabele verwerking in geneste aanvragen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Variabele verwerking in geneste aanvragen{#variable-processing-in-nested-requests}

$var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van &#39;? voorkomen het pad scheiden van de query.

Deze verwijzingen worden door de server vervangen door waarden (van de URL of van `catalog::Modifier` van de hoofdafbeeldingscatalogus) voordat de geneste aanvraag verder wordt geparseerd en verwerkt.

Daarnaast worden alle `$ *[!DNL var]*=`-definities van de URL en `catalog::Modifier` doorgestuurd naar alle geneste aanvragen voor beeldbewerking en het renderen van afbeeldingen. Dit zorgt ervoor dat alle veranderlijke definities aan alle malplaatjes, ongeacht het nestelen niveau beschikbaar zijn.

Ongeacht het nestniveau, slechts single-pass HTTP-codering moet op veranderlijke waarden worden toegepast die overal in genestelde het Teruggeven van het Beeld of Beeld het Serven verzoeken moeten worden vervangen.
