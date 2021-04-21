---
description: Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.
solution: Experience Manager
title: Prioriteitswaarschuwing voor heapruimte
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Prioriteitswaarschuwing voor heapruimte{#heap-space-priority-alert}

Er wordt een prioriteitswaarschuwing verzonden wanneer de gratis Java-heapruimte zich direct na een Java-opschooncyclus onder de opgegeven drempel bevindt.

Herhaalde waarschuwingen moeten worden aangepakt door de Java-heapruimte te vergroten. Als deze voorwaarde daarna optreedt, wordt er pas een e-mailwaarschuwing weergegeven als de vertragingsperiode die met `AS::monitorAlertGenerator.heapSpaceResetInterval` is opgegeven, is verlopen.
