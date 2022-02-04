---
title: Command reference - Configuration attributes
description: Documentatie met configuratiekenmerken voor gemengde Media Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie met configuratiekenmerken voor gemengde Media Viewer.

Elke configuratieopdracht kan worden ingesteld in een URL of via `setParam()`, of `setParams()`, of beide, API-methoden. Om het even welk config attribuut kan ook in server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomstige Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. Bijvoorbeeld: `zoomstep` wordt als volgt beschreven:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Dit betekent dat u deze opdracht als volgt kunt gebruiken

* `zoomstep` (korte syntaxis)
* `ZoomView.zoomstep` (gekwalificeerd met naam van componentklasse)
* `cont_zoomView.zoomstep` (gekwalificeerd met component-id, aannemen `cont` is de id van het containerelement)

Zie ook [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
