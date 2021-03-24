---
description: Voor nesten en insluiten gelden enkele beperkingen.
solution: Experience Manager
title: Beperkingen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Beperkingen{#restrictions}

Voor nesten en insluiten gelden enkele beperkingen.

Voor goede serverprestaties moet de resolutie van afbeeldingen die door geneste aanvragen worden geretourneerd, redelijk overeenkomen met de structuurresolutie van de objecten waarop het materiaal wordt toegepast.

Externe afbeeldingen worden lokaal in cache geplaatst. Wijzigingen in dergelijke afbeeldingen worden pas gedetecteerd nadat de lokale cachevermelding is verouderd (op basis van de HTTP-header die vervalt).
