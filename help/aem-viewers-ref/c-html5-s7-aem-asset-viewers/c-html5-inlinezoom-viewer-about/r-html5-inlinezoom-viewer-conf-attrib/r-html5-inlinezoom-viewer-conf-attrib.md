---
description: Documentatie over configuratiekenmerken voor de Flyout-viewer
seo-description: Documentatie over configuratiekenmerken voor de Flyout-viewer
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor de Flyout-viewer

U kunt om het even welk configuratiebevel in URL plaatsen. U kunt ook `setParam()`, `setParams()` of beide API-methoden gebruiken. U kunt ook om het even welk configuratiekenmerk in het server-zijconfiguratieverslag specificeren.

Sommige configuratieopdrachten krijgen de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `zoomfactor` wordt bijvoorbeeld als volgt beschreven:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

De opdracht wordt als volgt gebruikt:

* `zoomfactor` (korte syntaxis)
* `FlyoutZoomView.zoomfactor` (gekwalificeerd met de naam van een componentklasse)
* `cont_flyout.zoomfactor` (gekwalificeerd met de component-id, ervan uitgaande dat dit de id van het containerelement  `cont` is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
