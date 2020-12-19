---
description: Referentiedocumentatie voor opdrachten voor Video360 Viewer.
seo-description: Referentiedocumentatie voor opdrachten voor Video360 Viewer.
seo-title: Opdrachtverwijzing - URL
solution: Experience Manager
title: Opdrachtverwijzing - URL
topic: Dynamic media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Opdrachtverwijzing - URL{#command-reference-url}

Referentiedocumentatie voor opdrachten voor Video360 Viewer.

U kunt om het even welk configuratiebevel in URL plaatsen. Of u kunt de API-methoden `setParam()`, `setParams()` of beide gebruiken om een configuratieopdracht in te stellen. U kunt om het even welk configattribuut in het server-zijconfiguratieverslag ook specificeren.

U kunt voor bepaalde configuratieopdrachten de klassenaam of de instantienaam opgeven van de overeenkomende HTML5 Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat optionele voorvoegsels voor dergelijke opdrachten. `playback` wordt bijvoorbeeld als volgt gedocumenteerd:

```
[Video360Player.|<containerId>_video360Player].playback
```

Dit betekent dat deze opdracht als volgt wordt gebruikt:

* `playback` (korte syntaxis)
* `Video360Player.playback` (gekwalificeerd met naam van componentklasse)
* `cont_video360Player.playback` (gekwalificeerd met component-id, ervan uitgaande dat dit de id van het containerelement  `cont` is)

Zie [De verwijzing van het Bevel gemeenschappelijk voor alle kijkers - de attributen van de Configuratie](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) en [De verwijzing van het Bevel gemeenschappelijk voor alle Kijkers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
