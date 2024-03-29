---
description: Patroonelement met reguliere expressie. Optioneel in <rule> elementen.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# expression{#expression}

Patroonelement met reguliere expressie. Optioneel in `<rule>` elementen.

## Attributen {#section-fd0574eee1f9423cbb2ed709c0906800}

Geen.

## Gegevens {#section-4cd740c511a1432da0955e9acfbcf96f}

Patroontekenreeks met reguliere expressie.

## Beschrijving {#section-3245c8a531bb455d8398449f6ea63b37}

De `<expression>` Het element kan leeg zijn of een eenvoudige zoektekenreeks of een reguliere-expressiepatroon bevatten. Het patroon wordt toegepast op de volledige aanvraagtekenreeks.

Er is altijd een overeenkomst wanneer `<expression>` leeg is of niet is gespecificeerd; dit komt overeen met `<expression>.*</expression>`.

De implementatie is gebaseerd op het Java-pakket [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), die een syntaxis met een reguliere expressie biedt die lijkt op die van Perl.

## Opmerking {#section-6b41a900b0ce4a9590e5861e3c81599c}

De expressiereeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met `&` en `<`, of de gehele tekenreeks kan worden ingesloten in een XML `CDATA` sectie:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle tekens tussen de `<expression>` en `</expression>` -tags worden doorgegeven aan de reguliere-expressieparser, inclusief tekens buiten de optionele `CDATA` sectie. Wees voorzichtig om extra witruimte te voorkomen.

## Zie ook {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
