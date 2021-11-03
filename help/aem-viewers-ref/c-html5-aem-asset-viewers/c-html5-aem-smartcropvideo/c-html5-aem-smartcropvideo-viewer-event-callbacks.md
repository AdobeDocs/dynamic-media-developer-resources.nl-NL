---
title: Gebeurteniscallbacks
description: Gebeurteniscallbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Gebeurteniscallbacks{#event-callbacks}

De viewer ondersteunt JavaScript-gebeurteniscallbacks die de webpagina gebruikt om het initialisatieproces of het runtimegedrag van de viewer bij te houden.

Callback-handlers worden toegewezen door gebeurtenisnamen en corresponderende handlerfuncties door te geven met de `handlers` eigenschap aan `config` JSON-object in de constructor van de viewer. Het is ook mogelijk `setHandlers()` API-methode.

Tot de ondersteunde viewergebeurtenissen behoren:

* `initComplete` - wordt geactiveerd wanneer de viewer-initialisatie is voltooid en alle interne componenten zijn gemaakt, zodat het mogelijk is `getComponent()` API. De callback-handler neemt geen argumenten aan.

* `trackEvent` - activeert telkens wanneer een gebeurtenis binnen de viewer plaatsvindt die kan worden afgehandeld door een systeem voor het bijhouden van gebeurtenissen, zoals Adobe Analytics. De callback manager neemt de volgende argumenten:

   * `objID {String}` momenteel niet gebruikt.
   * `compClass {String}` momenteel niet gebruikt.
   * `instName {String}` een instantienaam van de Viewer SDK-component die de gebeurtenis heeft geactiveerd.
   * `eventInfo {String}` gebeurtenislading.

Zie ook [SmartCropVideoViewer]
(../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) en [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
