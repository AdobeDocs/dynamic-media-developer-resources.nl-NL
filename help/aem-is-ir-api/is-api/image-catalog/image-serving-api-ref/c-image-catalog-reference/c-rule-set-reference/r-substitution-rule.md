---
description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
seo-description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
seo-title: vervanging
solution: Experience Manager
title: vervanging
topic: Scene7 Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# vervanging{#substitution}

Vervangend tekenreekselement. Optioneel in `<rule>` elementen.

## Attributen {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Geen.

## Gegevens {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Vervangende tekenreeks.

## Beschrijving {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definieert een vervangende tekenreeks voor de overeenkomende tekenreeks of subtekenreeks in het pad of de query.

Als de patroonexpressie subexpressies bevat (gescheiden door ronde haakjes), wordt de eerste overeenkomende subtekenreeks vervangen door de vervangende tekenreeks. Als de patroonexpressie geen subexpressies bevat, wordt de gehele overeenkomende tekenreeks vervangen.

Als de vervangende tekenreeks leeg of afwezig `<expression>` is, wordt deze aan het pad of de query toegevoegd.

Als `<substitution>` de overeenkomende tekenreeks of subtekenreeks leeg is, wordt deze verwijderd. Als `<substitution>` niet is opgegeven, wordt de pad- of querytekenreeks niet gewijzigd.

>[!NOTE]
>
>Alle overeenkomsten in de invoertekenreeks worden vervangen wanneer `replace="all"` dit wordt opgegeven in het `<rule>`,element waartoe dit `<substitution>` element behoort. Standaard wordt alleen de eerste overeenkomst vervangen door de vervangende tekenreeks.

## Opmerking {#section-cedf2adabaaf441c9f598fb0ea180246}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met `&` en `<`, respectievelijk, of de gehele tekenreeks kan worden ingesloten in een XML CDATA-sectie:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
