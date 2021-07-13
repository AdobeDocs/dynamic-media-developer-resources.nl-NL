---
description: Documentatie van configuratiekenmerken voor Spin Viewer.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie van configuratiekenmerken voor Spin Viewer.

Om het even welk configuratiebevel kan in URL worden geplaatst of gebruikend `setParam()`, of `setParams()`, of allebei, API methodes. Om het even welk config attribuut kan ook in server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `zoomstep` wordt bijvoorbeeld als volgt beschreven:

`[SpinView.|<containerId>_spinView].zoomstep`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `zoomstep` (korte syntaxis)
* `SpinView.zoomstep` (gekwalificeerd met naam van componentklasse)
* `cont_spinView.zoomstep` (gekwalificeerd met component-id, ervan uitgaande dat  `cont` dit de id van het containerelement is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
