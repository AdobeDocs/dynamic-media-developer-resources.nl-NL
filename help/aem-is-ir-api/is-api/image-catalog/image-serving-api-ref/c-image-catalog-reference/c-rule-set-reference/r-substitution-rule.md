---
description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
solution: Experience Manager
title: vervanging
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# substitution{#substitution}

Vervangend tekenreekselement. Optioneel in `<rule>`-elementen.

## Kenmerken {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Geen.

## Gegevens {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Vervangende tekenreeks.

## Beschrijving {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definieert een vervangende tekenreeks voor de overeenkomende tekenreeks of subtekenreeks in het pad of de query.

Als de patroonexpressie subexpressies bevat (gescheiden door ronde haakjes), wordt de eerste overeenkomende subtekenreeks vervangen door de vervangende tekenreeks. Als de patroonexpressie geen subexpressies bevat, wordt de gehele overeenkomende tekenreeks vervangen.

Als `<expression>` leeg of afwezig is, wordt het substitutietekenreeks toegevoegd aan de weg of de vraag.

Wanneer `<substitution>` leeg is, wordt de overeenkomende tekenreeks of subtekenreeks verwijderd. Als `<substitution>` niet wordt gespecificeerd, wordt het weg of vraagkoord niet gewijzigd.

>[!NOTE]
>
>Alle overeenkomsten in de invoertekenreeks worden vervangen wanneer `replace="all"` is opgegeven in het element `<rule>`, waartoe dit element `<substitution>` behoort. Standaard wordt alleen de eerste overeenkomst vervangen door de vervangende tekenreeks.

## Opmerking {#section-cedf2adabaaf441c9f598fb0ea180246}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met respectievelijk `&` en `<`, of de gehele tekenreeks kan worden ingesloten in een XML CDATA-sectie:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
