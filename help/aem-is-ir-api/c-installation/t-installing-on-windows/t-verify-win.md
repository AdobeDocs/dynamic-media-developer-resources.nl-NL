---
description: Nadat u Dynamic Media Image Serving hebt geïnstalleerd, moet u de installatie controleren.
seo-description: Nadat u Dynamic Media Image Serving hebt geïnstalleerd, moet u de installatie controleren.
seo-title: De installatie controleren
solution: Experience Manager
title: De installatie controleren
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# De installatie controleren{#verifying-the-installation}

Nadat u Dynamic Media Image Serving hebt geïnstalleerd, moet u de installatie controleren.

De server van het Beeld is geïnstalleerd als Dienst van Vensters.

1. Open het configuratiescherm Services en controleer of &quot;Dynamic Media Image Serving&quot; aanwezig is met de status &quot;Started&quot;.
1. Open een internetbrowser op dezelfde of op een andere host en controleer de standaardreacties van de server:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Controleer op de aanwezigheid van &quot; `imageServer.`&quot;punten in de reactie, die erop wijzen dat de Server van het Beeld luistert.
>Aanvullende verificatie kan worden uitgevoerd met de voorbeeldpagina&#39;s van de pakketten Documentatie en Demo, indien geïnstalleerd.

