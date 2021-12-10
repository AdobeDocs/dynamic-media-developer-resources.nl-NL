---
title: Opdrachtverwijzing - URL
description: Referentiedocumentatie voor opdracht voor SmartCrop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Opdrachtverwijzing - URL{#command-reference-url}

Referentiedocumentatie voor opdracht voor SmartCrop Video Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. U kunt ook de API-methoden gebruiken `setParam()`, of `setParams()`of beide om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. Bijvoorbeeld: `playback` wordt als volgt gedocumenteerd:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Dit betekent dat deze opdracht op de volgende manier wordt gebruikt:

* `playback` (korte syntaxis)
* `SmartCropVideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_smartCropVideoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat `cont` is de id van het containerelement)

Zie ook [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Zie ook [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
