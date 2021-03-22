---
description: Patroonelement voor reguliere expressie. Optioneel in elementen <rule>.
seo-description: Patroonelement voor reguliere expressie. Optioneel in elementen <rule>.
seo-title: expression
solution: Experience Manager
title: expression
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# expression{#expression}

Patroonelement voor reguliere expressie. Optioneel in `<rule>`-elementen.

## Kenmerken {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Geen.

## Gegevens {#section-e2601008d71243109af1a8c55b58416d}

Patroontekenreeks met reguliere expressie.

## Beschrijving {#section-759bfb738ddb45dba1f0807aba8c1113}

Het element `<expression>` kan leeg zijn of een eenvoudige zoektekenreeks of een reguliere-expressiepatroon bevatten. Het patroon wordt toegepast op de volledige aanvraagtekenreeks.

Er vindt altijd een overeenkomst plaats wanneer `<expression>` leeg is of niet is opgegeven. dit komt overeen met het opgeven van `<expression>.*</expression>`.

De implementatie is gebaseerd op het Java-pakket [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), dat een syntaxis voor reguliere expressies biedt die vergelijkbaar is met die van Perl.

## Notities {#section-10b472a902674893b49ca49a7052c366}

De expressiereeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen worden gecodeerd met respectievelijk `&` en `<`, of de volledige tekenreeks kan worden ingesloten in een sectie XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle tekens tussen de `<expression>`- en `</expression>`-tags worden doorgegeven aan de reguliere-expressieparser, inclusief tekens buiten de optionele `CDATA`-sectie. Wees voorzichtig om extra witruimte te voorkomen.

## Zie ook {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
