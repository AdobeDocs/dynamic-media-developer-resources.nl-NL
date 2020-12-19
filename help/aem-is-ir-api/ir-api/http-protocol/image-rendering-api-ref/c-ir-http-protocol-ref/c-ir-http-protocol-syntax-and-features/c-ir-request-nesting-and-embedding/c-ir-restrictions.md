---
description: Voor nesten en insluiten gelden enkele beperkingen.
seo-description: Voor nesten en insluiten gelden enkele beperkingen.
seo-title: Beperkingen
solution: Experience Manager
title: Beperkingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Beperkingen{#restrictions}

Voor nesten en insluiten gelden enkele beperkingen.

Voor goede serverprestaties moet de resolutie van afbeeldingen die door geneste aanvragen worden geretourneerd, redelijk overeenkomen met de structuurresolutie van de objecten waarop het materiaal wordt toegepast.

Externe afbeeldingen worden lokaal in cache geplaatst. Wijzigingen in dergelijke afbeeldingen worden pas gedetecteerd nadat de lokale cachevermelding is verouderd (op basis van de HTTP-header die vervalt).
