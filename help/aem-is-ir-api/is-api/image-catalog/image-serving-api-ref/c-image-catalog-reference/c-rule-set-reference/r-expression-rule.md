---
description: Patroonelement voor reguliere expressie. Optioneel in <rule> elementen.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# expression{#expression}

Patroonelement voor reguliere expressie. Optioneel in `<rule>` elementen.

## Attributen {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Geen.

## Gegevens {#section-e2601008d71243109af1a8c55b58416d}

Patroontekenreeks met reguliere expressie.

## Beschrijving {#section-759bfb738ddb45dba1f0807aba8c1113}

De `<expression>` Het element kan leeg zijn of een eenvoudige zoektekenreeks of een reguliere-expressiepatroon bevatten. Het patroon wordt toegepast op de volledige aanvraagtekenreeks.

Er is altijd een overeenkomst wanneer `<expression>` leeg is of niet is gespecificeerd; dit komt overeen met `<expression>.*</expression>`.

De implementatie is gebaseerd op het Java-pakket [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), die een syntaxis met reguliere expressies biedt die lijkt op die van Perl.

## Notities {#section-10b472a902674893b49ca49a7052c366}

De expressiereeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met `&` en `<`, of de gehele tekenreeks kan worden ingesloten in een XML `CDATA` sectie:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle tekens tussen de `<expression>` en `</expression>` -tags worden doorgegeven aan de reguliere-expressieparser, inclusief tekens buiten de optionele `CDATA` sectie. Wees voorzichtig om extra witruimte te voorkomen.

## Zie ook {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
