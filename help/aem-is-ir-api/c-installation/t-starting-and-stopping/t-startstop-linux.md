---
description: Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.
seo-description: Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.
seo-title: Starten of stoppen in Linux
solution: Experience Manager
title: Starten of stoppen in Linux
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# Starten of stoppen op Linux{#starting-or-stopping-on-linux}

Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.

* Het script dat moet worden gestart, gestopt en gecontroleerd of de status van Image Serving is opgeslagen in de map [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Het volgende alternatief zou aan systeembeheerders vertrouwd moeten zijn:

   `/sbin/service ImageServing {start|stop|status}`
