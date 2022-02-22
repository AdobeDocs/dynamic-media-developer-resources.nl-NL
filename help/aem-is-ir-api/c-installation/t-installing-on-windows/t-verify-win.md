---
title: De installatie controleren
description: Nadat u Dynamic Media Image Serving hebt geïnstalleerd, moet u de installatie controleren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# De installatie controleren {#verifying-the-installation}

Nadat u Dynamic Media Image Serving hebt geïnstalleerd, moet u de installatie controleren.

De server van het Beeld is geïnstalleerd als Dienst van Vensters.

1. Open het Controlebord van de Diensten en controleer dat `Dynamic Media Image Serving` is aanwezig met een status van `Started`.
1. Open een internetbrowser op dezelfde of op een andere host en controleer de standaardreacties van de server:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Controleren op de aanwezigheid van &quot; `imageServer.`&quot;punten in de reactie, die erop wijzen dat de Server van het Beeld luistert.
>Aanvullende verificatie kan worden uitgevoerd met de voorbeeldpagina&#39;s van de pakketten Documentatie en Demo, indien geïnstalleerd.
