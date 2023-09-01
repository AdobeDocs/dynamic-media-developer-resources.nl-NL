---
title: vervanging
description: Vervangend tekenreekselement. Optioneel in <rule> elementen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# vervanging{#substitution}

Vervangend tekenreekselement. Optioneel in `<rule>` elementen.

## Attributen {#section-d955eefc53eb4274861270669c01f9ca}

Geen.

## Gegevens {#section-a2688866ed6d41279a8478886e511ae3}

Vervangende tekenreeks.

## Beschrijving {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definieert een vervangende tekenreeks voor de overeenkomende tekenreeks of subtekenreeks in het pad of de query.

Als de patroonexpressie subexpressies bevat (gescheiden door ronde haakjes), wordt de eerste overeenkomende subtekenreeks vervangen door de vervangende tekenreeks. Als de patroonexpressie geen subexpressions bevat, wordt de volledige overeenkomende tekenreeks vervangen.

Indien `<expression>` is leeg of ontbreekt, wordt het substitutietekenreeks toegevoegd aan de weg of de vraag.

Indien `<substitution>` is leeg, wordt de overeenkomende tekenreeks of subtekenreeks verwijderd. Indien `<substitution>` niet wordt opgegeven, wordt de pad- of querytekenreeks niet gewijzigd.

## Opmerking {#section-90fe89bb17a04804b7ff3c93df082892}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met `&` en `<`, of de gehele tekenreeks kan worden ingesloten in een XML `CDATA` sectie:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
