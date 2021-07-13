---
description: Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.
solution: Experience Manager
title: Starten of stoppen in Linux
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Starten of stoppen in Linux{#starting-or-stopping-on-linux}

Er zijn twee opties voor het starten of stoppen van Image Serving op Linux.

* Het script dat moet worden gestart, gestopt en gecontroleerd of de status van Image Serving is opgeslagen in de map [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Het volgende alternatief zou aan systeembeheerders vertrouwd moeten zijn:

   `/sbin/service ImageServing {start|stop|status}`
