---
description: Een lijst met paden, gescheiden door puntkomma's, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.
solution: Experience Manager
title: Bronhoofdmappen (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Bronhoofdmappen (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Een lijst met paden, gescheiden door puntkomma&#39;s, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.

Dit kunnen absolute paden of paden zijn ten opzichte van *[!DNL install_folder]*. Wanneer meerdere paden zijn opgegeven, probeert de server elke hoofdmap in de gegeven volgorde uit tot het bestand is gevonden. Standaard is [!DNL ./resources], voor een standaardhoofdpad van [!DNL install_folder/resources].
