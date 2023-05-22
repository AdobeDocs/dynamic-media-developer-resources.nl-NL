---
title: Gebeurteniscallbacks
description: Gebeurteniscallbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
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
   * `timeStamp {Number}` tijdstempel van de gebeurtenis.
   * `eventInfo {String}` gebeurtenislading.

* `quickViewActivate` - wordt geactiveerd wanneer een gebruiker klikt of tikt op een interactief staal binnen de interactieve staalcomponent of in het scherm &quot;oproepen naar actie&quot; dat wordt weergegeven aan het einde van het afspelen van de video. Callback-handler gebruikt het enige argument dat een JSON-object met de volgende velden is:

   * `sku` { `String`} SKU-waarde die aan het interactieve staal is gekoppeld.
   * `<additionalVariable>` { `String`} nul of meer extra variabelen verbonden aan het interactieve monster.

Zie ook [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) en [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
