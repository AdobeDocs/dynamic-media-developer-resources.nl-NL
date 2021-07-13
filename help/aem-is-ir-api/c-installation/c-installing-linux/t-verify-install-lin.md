---
description: Nadat u Image Serving op Linux hebt geïnstalleerd, verifieert u de installatie.
solution: Experience Manager
title: De installatie controleren
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
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
