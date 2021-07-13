---
description: Documentatie over configuratiekenmerken voor Video360 Viewer.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR-video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

Documentatie over configuratiekenmerken voor Video360 Viewer.

Om het even welk configuratiebevel kan in URL worden geplaatst of gebruikend `setParam()`, of `setParams()`, of allebei, API methodes. Om het even welk configuratiekenmerk kan ook in het server-zijconfiguratieverslag worden gespecificeerd.

Sommige configuratieopdrachten kunnen worden voorafgegaan door de klassenaam of instantienaam van de overeenkomende Viewer SDK-component. Een instantienaam van de component is dynamisch en is afhankelijk van de id van het DOM-element van de viewercontainer dat is doorgegeven aan de API-methode `setContainerId()`. Documentatie bevat een optioneel voorvoegsel voor dergelijke opdrachten. De opdracht `playback` wordt bijvoorbeeld als volgt beschreven:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Dit betekent dat u deze opdracht kunt gebruiken als:

* `playback` (korte syntaxis)
* `VideoPlayer.playback` (gekwalificeerd met naam van componentklasse)
* `cont_videoPlayer.playback` (gekwalificeerd met component-id, ervan uitgaande dat  `cont` dit de id van het containerelement is)

Zie ook [Command reference common for all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
