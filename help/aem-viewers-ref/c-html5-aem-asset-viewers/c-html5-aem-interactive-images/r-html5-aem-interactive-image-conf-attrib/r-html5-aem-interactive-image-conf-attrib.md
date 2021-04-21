---
description: Documentatie over configuratiekenmerken voor Interactive Image Viewer.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Interactive Image Viewer.

Om het even welk configuratiebevel kan in URL worden geplaatst of gebruikend `setParam()`, of `setParams()`, of allebei, API methodes. Om het even welk config attribuut kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `zoomstep` wordt bijvoorbeeld als volgt beschreven:

`[ZoomView.|<containerId>_zoomView].fmt`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `fmt` (korte syntaxis)
* `ZoomView.fmt` (gekwalificeerd met naam van componentklasse)
* `cont_zoomView.fmt` (gekwalificeerd met component-id, ervan uitgaande dat  `cont` dit de id van het containerelement is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
