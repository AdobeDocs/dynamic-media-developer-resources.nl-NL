---
description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
seo-description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
seo-title: Prioriteitswaarschuwing voor heapruimte
solution: Experience Manager
title: Prioriteitswaarschuwing voor heapruimte
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Prioriteitswaarschuwing voor heapruimte{#heap-space-priority-alert}

Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.

Herhaalde waarschuwingen moeten worden aangepakt door de Java-heapruimte te vergroten. Als deze voorwaarde daarna optreedt, wordt er pas een e-mailwaarschuwing weergegeven als de vertragingsperiode die met `AS::monitorAlertGenerator.heapSpaceResetInterval` is opgegeven, is verlopen.
