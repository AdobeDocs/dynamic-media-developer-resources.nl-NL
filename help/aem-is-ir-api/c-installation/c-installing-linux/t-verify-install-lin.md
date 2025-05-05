---
title: De installatie controleren
description: Nadat u Image Serving op Linux® installeert, verifieer de installatie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# De installatie controleren{#verifying-the-installation}

Nadat u Image Serving op Linux® installeert, verifieer de installatie.

De Image Server wordt geïnstalleerd als een Linux® daemon.

**De installatie controleren**

1. Verifieer dat de Serving van het Beeld wordt gevormd om automatisch te beginnen en dat het loopt:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >U moet over basismachtigingen beschikken om deze scripts uit te voeren.

1. Open een internetbrowser op dezelfde of op een andere host en controleer de standaardreacties van de server:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Controleer in de reacties of er items zijn die beginnen met `imageServer`, die aangeven dat de [!DNL Platform Server] kon met succes met de Server van het Beeld communiceren.

>Aanvullende verificatie kan worden uitgevoerd met de voorbeeldpagina&#39;s van de pakketten Documentatie en Demo, indien geïnstalleerd.
