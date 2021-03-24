---
description: Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.
solution: Experience Manager
title: Starten of stoppen in Linux
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Starten of stoppen op Linux{#starting-or-stopping-on-linux}

Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.

* Het script dat moet worden gestart, gestopt en gecontroleerd of de status van Image Serving is opgeslagen in de map [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Het volgende alternatief zou aan systeembeheerders vertrouwd moeten zijn:

   `/sbin/service ImageServing {start|stop|status}`
