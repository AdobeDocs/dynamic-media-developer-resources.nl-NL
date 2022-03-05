---
title: Variabele verwerking in ingesloten externe verzoeken
description: $var$ verwijzingen die zich ergens binnen de accolades van een ingesloten extern verzoek voordoen, worden vervangen door overeenkomstige waarden voor de definitie van variabelen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Variabele verwerking in ingesloten externe verzoeken{#variable-processing-in-embedded-foreign-requests}

Alle `$var$` verwijzingen die ergens binnen de accolades van een ingesloten extern verzoek voorkomen, worden vervangen door overeenkomende waarden voor de definitie van variabelen.

Hiermee kunnen ingesloten externe aanvragen in een sjabloon in een afbeeldingscatalogus worden geplaatst.

De waarden van variabelen die in buitenlandse verzoeken moeten worden vervangen moeten typisch dubbel-gecodeerd zijn, omdat geen hercodering wordt toegepast alvorens de server probeert om definitieve buitenlandse url over te brengen.
