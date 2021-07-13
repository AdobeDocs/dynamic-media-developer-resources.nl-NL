---
description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
solution: Experience Manager
title: vervanging
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# vervanging{#substitution}

Vervangend tekenreekselement. Optioneel in `<rule>`-elementen.

## Attributen {#section-d955eefc53eb4274861270669c01f9ca}

Geen.

## Gegevens {#section-a2688866ed6d41279a8478886e511ae3}

Vervangende tekenreeks.

## Beschrijving {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definieert een vervangende tekenreeks voor de overeenkomende tekenreeks of subtekenreeks in het pad of de query.

Als de patroonexpressie subexpressies bevat (gescheiden door ronde haakjes), wordt de eerste overeenkomende subtekenreeks vervangen door de vervangende tekenreeks. Als de patroonexpressie geen subexpressies bevat, wordt de gehele overeenkomende tekenreeks vervangen.

Als `<expression>` leeg of afwezig is, wordt het substitutietekenreeks toegevoegd aan de weg of de vraag.

Wanneer `<substitution>` leeg is, wordt de overeenkomende tekenreeks of subtekenreeks verwijderd. Als `<substitution>` niet wordt gespecificeerd, wordt het weg of vraagkoord niet gewijzigd.

## Opmerking {#section-90fe89bb17a04804b7ff3c93df082892}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met respectievelijk `&` en `<`, of de volledige tekenreeks kan worden ingesloten in een sectie XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
