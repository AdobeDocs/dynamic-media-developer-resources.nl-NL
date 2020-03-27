---
description: Documentatie over configuratiekenmerken voor Video Viewer.
seo-description: Documentatie over configuratiekenmerken voor Video Viewer.
seo-title: Command reference - Configuration attributes
solution: Experience Manager
title: Command reference - Configuration attributes
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Video Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. U kunt ook de API-methoden gebruiken `setParam()`, of `setParams()`beide om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die aan de API-methode is doorgegeven. `setContainerId()` Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. Bijvoorbeeld, `playback` wordt gedocumenteerd als volgt:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Dit betekent dat deze opdracht als volgt wordt gebruikt:

* `playback` (korte syntaxis)
* `VideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_videoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat dit de id van het containerelement `cont` is)

Zie de verwijzing van het [Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Zie [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
