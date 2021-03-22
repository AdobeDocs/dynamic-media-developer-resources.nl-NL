---
description: Nadat u Image Serving op Linux hebt geïnstalleerd, verifieert u de installatie.
seo-description: Nadat u Image Serving op Linux hebt geïnstalleerd, verifieert u de installatie.
seo-title: De installatie controleren
solution: Experience Manager
title: De installatie controleren
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# De installatie controleren{#verifying-the-installation}

Nadat u Image Serving op Linux hebt geïnstalleerd, verifieert u de installatie.

De Image Server wordt geïnstalleerd als Linux-daemon.

**De installatie controleren**

1. Verifieer dat de Serving van het Beeld wordt gevormd om automatisch te beginnen en dat het loopt:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >U moet over basismachtigingen beschikken om deze scripts uit te voeren.

1. Open een internetbrowser op dezelfde of op een andere host en controleer de standaardreactie(s) van de server:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

In de reacties, controleer de aanwezigheid van punten die met &quot; `imageServer.`&quot;beginnen, die erop wijzen dat de Server van het Platform met de Server van het Beeld kon met succes communiceren.
>Aanvullende verificatie kan worden uitgevoerd met de voorbeeldpagina&#39;s van de pakketten Documentatie en Demo, indien geïnstalleerd.

