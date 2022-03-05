---
title: Variabele verwerking in geneste aanvragen
description: $var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van '? voorkomen het pad scheiden van de query.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Variabele verwerking in geneste aanvragen{#variable-processing-in-nested-requests}

$var$ verwijzingen kunnen overal binnen de krullende steunen van een genestelde Beeldserver of Beeld teruggeven verzoek, met inbegrip van links van &#39;? voorkomen het pad scheiden van de query.

De server vervangt deze verwijzingen door waarden (van de URL of van `catalog::Modifier` (van de hoofdafbeeldingscatalogus) voordat de geneste aanvraag verder wordt geparseerd en verwerkt.

Bovendien `$ *[!DNL var]*=` definities van de URL en `catalog::Modifier` worden doorgestuurd naar alle aanvragen voor geneste beeldservers en het renderen van afbeeldingen. Zo zorgt u ervoor dat alle definities van variabelen beschikbaar zijn voor alle sjablonen, ongeacht het nestniveau.

Ongeacht het nestniveau, slechts single-pass HTTP-codering moet op veranderlijke waarden worden toegepast die overal in genestelde het Teruggeven van het Beeld of Beeld het Serven verzoeken moeten worden vervangen.
