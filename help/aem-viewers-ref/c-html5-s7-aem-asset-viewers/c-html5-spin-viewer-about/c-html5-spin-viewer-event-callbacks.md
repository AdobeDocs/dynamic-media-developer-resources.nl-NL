---
description: 'null'
seo-description: 'null'
seo-title: Gebeurteniscallbacks
solution: Experience Manager
title: Gebeurteniscallbacks
topic: Dynamic media
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gebeurteniscallbacks{#event-callbacks}

De viewer ondersteunt JavaScript-gebeurteniscallbacks die de webpagina gebruikt om het initialisatieproces of het runtimegedrag van de viewer bij te houden.

Callback-handlers worden toegewezen door gebeurtenisnamen en bijbehorende handlerfuncties met de `handlers` eigenschap door te geven aan `config` JSON-object in de constructor van de viewer. U kunt ook de `setHandlers()` API-methode gebruiken.

Tot de ondersteunde viewergebeurtenissen behoren:

* `initComplete` - wordt geactiveerd wanneer de viewerinitialisatie is voltooid en alle interne componenten zijn gemaakt, zodat de `getComponent()` API kan worden gebruikt. De callback-handler neemt geen argumenten aan.

* `trackEvent` - activeert telkens wanneer een gebeurtenis binnen de viewer plaatsvindt. Dit kan worden afgehandeld door een systeem voor het bijhouden van gebeurtenissen, zoals Adobe Analytics. De callback manager neemt de volgende argumenten:

   * `objID {String}` momenteel niet gebruikt.
   * `compClass {String}` momenteel niet gebruikt.
   * `instName {String}` een instantienaam van de Viewer SDK-component die de gebeurtenis heeft geactiveerd.
   * `timeStamp {Number}` tijdstempel van de gebeurtenis.
   * `eventInfo {String}` gebeurtenislading.

Zie ook [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) en [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
