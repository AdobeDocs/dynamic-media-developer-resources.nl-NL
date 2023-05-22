---
description: Vervangend tekenreekselement. Optioneel in <rule> elementen.
solution: Experience Manager
title: vervanging
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

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

Indien `<expression>` is leeg of ontbreekt, wordt het substitutietekenreeks toegevoegd aan de weg of de vraag.

Indien `<substitution>` is leeg, wordt de overeenkomende tekenreeks of subtekenreeks verwijderd. Indien `<substitution>` niet wordt opgegeven, wordt de pad- of querytekenreeks niet gewijzigd.

>[!NOTE]
>
>Alle overeenkomsten in de invoertekenreeks worden vervangen wanneer `replace="all"` wordt opgegeven in het dialoogvenster `<rule>`,element waaraan dit `<substitution>` element hoort. Standaard wordt alleen de eerste overeenkomst vervangen door de vervangende tekenreeks.

## Opmerking {#section-cedf2adabaaf441c9f598fb0ea180246}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met `&` en `<`of de gehele tekenreeks kan worden ingesloten in een XML CDATA-sectie:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
