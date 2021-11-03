---
description: Documentatie met configuratiekenmerken voor SmartCrop Video Viewer.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie met configuratiekenmerken voor SmartCrop Video Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. U kunt ook de API-methoden gebruiken `setParam()`, of `setParams()`of beide om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. Bijvoorbeeld: `playback` wordt als volgt gedocumenteerd:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Dit betekent dat deze opdracht als volgt wordt gebruikt:

* `playback` (korte syntaxis)
* `SmartCropVideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_videoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat `cont` is de id van het containerelement)

Zie [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Zie [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
