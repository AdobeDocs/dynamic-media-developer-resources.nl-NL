---
description: Documentatie over configuratiekenmerken voor Carousel Viewer.
seo-description: Documentatie over configuratiekenmerken voor Carousel Viewer.
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: 036af728-ab00-4db3-98cf-d16f1bffa064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Carousel Viewer.

Om het even welk configuratiebevel kan in URL worden geplaatst of gebruikend `setParam()`, of `setParams()`, of allebei, API methodes. Om het even welk config attribuut kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `zoomstep` wordt bijvoorbeeld als volgt beschreven:

`[ZoomView.|<containerId>_carouselView].fmt`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `fmt` (korte syntaxis)
* `CarouselView.fmt` (gekwalificeerd met naam van componentklasse)
* `cont_carouselView.fmt` (gekwalificeerd met component-id, ervan uitgaande dat  `cont` dit de id van het containerelement is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
