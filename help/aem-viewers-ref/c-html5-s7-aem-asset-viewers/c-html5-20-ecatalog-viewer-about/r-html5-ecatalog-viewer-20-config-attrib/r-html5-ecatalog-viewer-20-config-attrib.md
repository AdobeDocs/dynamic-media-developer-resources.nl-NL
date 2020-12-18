---
description: Documentatie met configuratiekenmerken voor eCatalog Viewer.
seo-description: Documentatie met configuratiekenmerken voor eCatalog Viewer.
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie met configuratiekenmerken voor eCatalog Viewer.

Om het even welk configuratiebevel kan in URL worden geplaatst of gebruikend `setParam()`, of `setParams()`, of allebei, API methodes. U kunt ook om het even welk configuratiekenmerk specificeren dat in het server-zijconfiguratieverslag wordt gespecificeerd.

Voor sommige configuratieopdrachten kunt u een voorvoegsel toevoegen aan de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `zoomstep` wordt bijvoorbeeld als volgt beschreven:

`[PageView.|<containerId>_pageView].zoomstep`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `zoomstep` (korte syntaxis)
* `PageView.zoomstep` (gekwalificeerd met naam van componentklasse)
* `cont_pageView.zoomstep` (gekwalificeerd met component-id, ervan uitgaande dat  `cont` dit de id van het containerelement is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
