---
title: Command reference - Configuration attributes
description: Documentatie over configuratiekenmerken voor Panoramische Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Panoramische Viewer.

Elke configuratieopdracht kan worden ingesteld in een URL of via `setParam()` en/of `setParams()` API-methoden. Om het even welk config attribuut kan ook in server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende HTML5 SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer die is doorgegeven aan `setContainerId()` API-methode. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. Bijvoorbeeld: `vrrender` deze opdracht wordt als volgt beschreven:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Dit betekent dat deze opdracht op de volgende manier wordt gebruikt:

* `vrrender` (korte syntaxis)
* `PanoramicView.vrrender` (gekwalificeerd met naam van componentklasse)
* `cont_panoramicView.vrrender` (gekwalificeerd met component-id, ervan uitgaande dat de inhoud de id van het containerelement is)


Zie [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Zie [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
