---
description: Gebeurteniscallbacks
solution: Experience Manager
title: Gebeurteniscallbacks
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e6cffe77-f653-4e8e-bdec-2661051fe8cf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Gebeurteniscallbacks{#event-callbacks}

De viewer ondersteunt JavaScript-gebeurteniscallbacks die de webpagina gebruikt om het initialisatieproces of het runtimegedrag van de viewer bij te houden.

Callback-handlers worden toegewezen door gebeurtenisnamen en corresponderende handlerfuncties met de eigenschap `handlers` door te geven aan `config` JSON-object in de constructor van de viewer. U kunt ook de API-methode `setHandlers()` gebruiken.

Tot de ondersteunde viewergebeurtenissen behoren:

* `initComplete` - wordt geactiveerd wanneer de viewerinitialisatie is voltooid en alle interne componenten zijn gemaakt, zodat de  `getComponent()` API kan worden gebruikt. De callback-handler neemt geen argumenten aan.

* `trackEvent` - activeert telkens wanneer een gebeurtenis binnen de viewer plaatsvindt die kan worden afgehandeld door een systeem voor het bijhouden van gebeurtenissen, zoals Adobe Analytics. De callback manager neemt de volgende argumenten:

   * `objID {String}` momenteel niet gebruikt.
   * `compClass {String}` momenteel niet gebruikt.
   * `instName {String}` een instantienaam van de Viewer SDK-component die de gebeurtenis heeft geactiveerd.
   * `timeStamp {Number}` tijdstempel van de gebeurtenis.
   * `eventInfo {String}` gebeurtenislading.

Zie ook [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) en [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
