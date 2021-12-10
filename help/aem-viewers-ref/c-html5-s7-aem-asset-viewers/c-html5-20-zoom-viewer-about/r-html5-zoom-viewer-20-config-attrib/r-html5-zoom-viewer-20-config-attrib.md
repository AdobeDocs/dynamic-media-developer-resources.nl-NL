---
title: Command reference - Configuration attributes
description: Documentatie over configuratiekenmerken voor Zoomviewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Zoomviewer.

Elke configuratieopdracht kan worden ingesteld in een URL of via `setParam()`, of `setParams()`, of beide, API-methoden. Om het even welk config attribuut kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. Bijvoorbeeld: `zoomstep` wordt als volgt beschreven:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Dit betekent dat u de opdracht als

* `zoomstep` (korte syntaxis)
* `ZoomView.zoomstep` (gekwalificeerd met naam van componentklasse)
* `cont_zoomView.zoomstep` (gekwalificeerd met component-id, aannemen `cont` is de id van het containerelement)

Zie ook [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
