---
description: Documentatie over configuratiekenmerken voor Video Viewer.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Video Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. Of u kunt de API-methoden `setParam()`, `setParams()` of beide gebruiken om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. `playback` wordt bijvoorbeeld als volgt gedocumenteerd:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Dit betekent dat deze opdracht als volgt wordt gebruikt:

* `playback` (korte syntaxis)
* `VideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_videoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat dit de id van het containerelement  `cont` is)

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
