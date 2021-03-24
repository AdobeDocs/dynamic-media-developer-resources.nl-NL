---
description: Patroonelement met reguliere expressie. Optioneel in elementen <rule>.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# expression{#expression}

Patroonelement met reguliere expressie. Optioneel in `<rule>`-elementen.

## Kenmerken {#section-fd0574eee1f9423cbb2ed709c0906800}

Geen.

## Gegevens {#section-4cd740c511a1432da0955e9acfbcf96f}

Patroontekenreeks met reguliere expressie.

## Beschrijving {#section-3245c8a531bb455d8398449f6ea63b37}

Het element `<expression>` kan leeg zijn of een eenvoudige zoektekenreeks of een reguliere-expressiepatroon bevatten. Het patroon wordt toegepast op de volledige aanvraagtekenreeks.

Er vindt altijd een overeenkomst plaats wanneer `<expression>` leeg is of niet is opgegeven. dit komt overeen met het opgeven van `<expression>.*</expression>`.

De implementatie is gebaseerd op het Java-pakket [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), dat een syntaxis voor reguliere expressies biedt die lijkt op die van Perl.

## Opmerking {#section-6b41a900b0ce4a9590e5861e3c81599c}

De expressiereeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met respectievelijk `&` en `<`, of de volledige tekenreeks kan worden ingesloten in een sectie XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle tekens tussen de `<expression>`- en `</expression>`-tags worden doorgegeven aan de reguliere-expressieparser, inclusief tekens buiten de optionele `CDATA`-sectie. Wees voorzichtig om extra witruimte te voorkomen.

## Zie ook {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
