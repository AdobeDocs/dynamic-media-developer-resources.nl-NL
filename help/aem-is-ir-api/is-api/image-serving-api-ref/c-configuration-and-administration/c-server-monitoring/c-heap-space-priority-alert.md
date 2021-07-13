---
description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
solution: Experience Manager
title: Prioriteitswaarschuwing voor heapruimte
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Prioriteitswaarschuwing voor heapruimte{#heap-space-priority-alert}

Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.

Herhaalde waarschuwingen moeten worden aangepakt door de Java-heapruimte te vergroten. Als deze voorwaarde daarna optreedt, wordt er pas een e-mailwaarschuwing weergegeven als de vertragingsperiode die met `AS::monitorAlertGenerator.heapSpaceResetInterval` is opgegeven, is verlopen.
