---
title: Beperkingen
description: Voor nesten en insluiten gelden enkele beperkingen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Beperkingen{#restrictions}

Voor nesten en insluiten gelden enkele beperkingen.

Voor goede serverprestaties moet de resolutie van afbeeldingen die door geneste aanvragen worden geretourneerd, redelijk overeenkomen met de structuurresolutie van de objecten waarop het materiaal wordt toegepast.

Externe afbeeldingen worden lokaal in cache geplaatst. Wijzigingen in dergelijke afbeeldingen worden pas gedetecteerd nadat de lokale cachevermelding is verouderd (op basis van de HTTP-header die vervalt).
