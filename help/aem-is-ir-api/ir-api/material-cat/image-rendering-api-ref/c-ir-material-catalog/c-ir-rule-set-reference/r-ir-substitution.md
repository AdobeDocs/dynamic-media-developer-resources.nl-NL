---
description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
seo-description: Vervangend tekenreekselement. Optioneel in elementen <rule>.
seo-title: vervanging
solution: Experience Manager
title: vervanging
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# vervanging{#substitution}

Vervangend tekenreekselement. Optioneel in `<rule>` elementen.

## Attributen {#section-d955eefc53eb4274861270669c01f9ca}

Geen.

## Gegevens {#section-a2688866ed6d41279a8478886e511ae3}

Vervangende tekenreeks.

## Beschrijving {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definieert een vervangende tekenreeks voor de overeenkomende tekenreeks of subtekenreeks in het pad of de query.

Als de patroonexpressie subexpressies bevat (gescheiden door ronde haakjes), wordt de eerste overeenkomende subtekenreeks vervangen door de vervangende tekenreeks. Als de patroonexpressie geen subexpressies bevat, wordt de gehele overeenkomende tekenreeks vervangen.

Als de vervangende tekenreeks leeg of afwezig `<expression>` is, wordt deze aan het pad of de query toegevoegd.

Als `<substitution>` de overeenkomende tekenreeks of subtekenreeks leeg is, wordt deze verwijderd. Als `<substitution>` niet is opgegeven, wordt de pad- of querytekenreeks niet gewijzigd.

## Opmerking {#section-90fe89bb17a04804b7ff3c93df082892}

De vervangende tekenreeks mag geen letterlijke &lt; en &amp; tekens bevatten. Deze gereserveerde tekens kunnen respectievelijk met `&` en `<`worden gecodeerd, of de gehele tekenreeks kan worden ingesloten in een XML- `CDATA` sectie:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
