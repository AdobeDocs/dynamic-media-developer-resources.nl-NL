---
description: Een lijst met paden, gescheiden door puntkomma's, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.
solution: Experience Manager
title: Bronhoofdmappen (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Bronhoofdmappen (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Een lijst met paden, gescheiden door puntkomma&#39;s, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.

Dit kunnen absolute paden of paden zijn ten opzichte van *[!DNL install_folder]*. Wanneer meerdere paden zijn opgegeven, probeert de server elke hoofdmap in de gegeven volgorde uit tot het bestand is gevonden. De standaardwaarde is [!DNL ./resources], voor een standaardwortelweg van [!DNL install_folder/resources].
