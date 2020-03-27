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

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie met configuratiekenmerken voor eCatalog Viewer.

Elke configuratieopdracht kan worden ingesteld in URL of via API-methoden `setParam()`of `setParams()`, of beide. U kunt ook om het even welk configuratiekenmerk specificeren dat in het server-zijconfiguratieverslag wordt gespecificeerd.

Voor sommige configuratieopdrachten kunt u een voorvoegsel toevoegen aan de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die aan de API-methode is doorgegeven. `setContainerId()` Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht wordt bijvoorbeeld als volgt `zoomstep` beschreven:

`[PageView.|<containerId>_pageView].zoomstep`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `zoomstep` (korte syntaxis)
* `PageView.zoomstep` (gekwalificeerd met naam van componentklasse)
* `cont_pageView.zoomstep` (gekwalificeerd met component-id, ervan uitgaande dat `cont` de id van het containerelement is)

Zie ook de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
