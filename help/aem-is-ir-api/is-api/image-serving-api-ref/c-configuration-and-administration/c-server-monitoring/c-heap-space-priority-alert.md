---
description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
seo-description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
seo-title: Prioriteitswaarschuwing voor heapruimte
solution: Experience Manager
title: Prioriteitswaarschuwing voor heapruimte
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prioriteitswaarschuwing voor heapruimte{#heap-space-priority-alert}

Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.

Herhaalde waarschuwingen moeten worden aangepakt door de Java-heapruimte te vergroten. Als deze voorwaarde daarna optreedt, resulteert dit niet in een e-mailwaarschuwing totdat de opgegeven vertragingsperiode `AS::monitorAlertGenerator.heapSpaceResetInterval` is verlopen.
