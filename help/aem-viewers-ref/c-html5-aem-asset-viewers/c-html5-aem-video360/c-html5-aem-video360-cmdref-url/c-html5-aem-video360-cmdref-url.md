---
title: Opdrachtverwijzing - URL
description: Referentiedocumentatie voor opdrachten voor Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Opdrachtverwijzing - URL{#command-reference-url}

Referentiedocumentatie voor opdrachten voor Video360 Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. Of u kunt de API-methoden `setParam()`, `setParams()` of beide gebruiken om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende HTML5 Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. `playback` wordt bijvoorbeeld als volgt gedocumenteerd:

```
[Video360Player.|<containerId>_video360Player].playback
```

Betekenis dat dit bevel op de volgende manier wordt gebruikt:

* `playback` (korte syntaxis)
* `Video360Player.playback` (gekwalificeerd met naam van componentklasse)
* `cont_video360Player.playback` (gekwalificeerd met component-id, ervan uitgaande dat dit de id van het containerelement  `cont` is)

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
