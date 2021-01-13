---
description: Gebeurteniscallbacks
solution: Experience Manager
title: Gebeurteniscallbacks
topic: Dynamic media
uuid: 08756e93-2c6c-4c63-9dd0-c64531561d6f
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '147'
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

Zie ook [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) en [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
