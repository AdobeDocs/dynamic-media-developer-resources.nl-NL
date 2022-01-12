---
title: Command reference - Configuration attributes
description: Documentatie over configuratiekenmerken voor de Flyout-viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor de Flyout-viewer

U kunt om het even welk configuratiebevel in URL plaatsen. U kunt ook `setParam()`, `setParams()`, of beide API-methoden. U kunt ook om het even welk configuratiekenmerk in het server-zijconfiguratieverslag specificeren.

Sommige configuratieopdrachten krijgen de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De `zoomfactor` wordt als volgt beschreven:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

De opdracht wordt als volgt gebruikt:

* `zoomfactor` (korte syntaxis)
* `FlyoutZoomView.zoomfactor` (gekwalificeerd met de naam van een componentklasse)
* `cont_flyout.zoomfactor` (gekwalificeerd met de component-id, ervan uitgaande dat `cont` is de id van het containerelement)

Zie ook [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
