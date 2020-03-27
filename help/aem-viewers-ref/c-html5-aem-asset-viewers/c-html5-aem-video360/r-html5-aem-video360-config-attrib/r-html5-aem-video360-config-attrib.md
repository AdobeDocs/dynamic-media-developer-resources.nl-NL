---
description: Documentatie over configuratiekenmerken voor Video360 Viewer.
seo-description: Documentatie over configuratiekenmerken voor Video360 Viewer.
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Video360 Viewer.

Elke configuratieopdracht kan worden ingesteld in URL of via API-methoden `setParam()`of `setParams()`, of beide. Om het even welk configuratiekenmerk kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die aan de API-methode is doorgegeven. `setContainerId()` Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht wordt bijvoorbeeld als volgt `playback` beschreven:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `playback` (korte syntaxis)
* `VideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_videoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat `cont` de id van het containerelement is)

Zie ook de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
