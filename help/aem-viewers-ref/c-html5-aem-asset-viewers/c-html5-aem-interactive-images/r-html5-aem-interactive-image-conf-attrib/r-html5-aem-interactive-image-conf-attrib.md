---
description: Documentatie over configuratiekenmerken voor Interactive Image Viewer.
seo-description: Documentatie over configuratiekenmerken voor Interactive Image Viewer.
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: ef118730-1bd2-4b88-917c-1fa51c6a488b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Interactive Image Viewer.

Elke configuratieopdracht kan worden ingesteld in URL of via API-methoden `setParam()`of `setParams()`, of beide. Om het even welk config attribuut kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die aan de API-methode is doorgegeven. `setContainerId()` Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht wordt bijvoorbeeld als volgt `zoomstep` beschreven:

`[ZoomView.|<containerId>_zoomView].fmt`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `fmt` (korte syntaxis)
* `ZoomView.fmt` (gekwalificeerd met naam van componentklasse)
* `cont_zoomView.fmt` (gekwalificeerd met component-id, ervan uitgaande dat `cont` de id van het containerelement is)

Zie ook de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
