---
title: Gebeurteniscallbacks
description: Gebeurteniscallbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '154'
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
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) en [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
