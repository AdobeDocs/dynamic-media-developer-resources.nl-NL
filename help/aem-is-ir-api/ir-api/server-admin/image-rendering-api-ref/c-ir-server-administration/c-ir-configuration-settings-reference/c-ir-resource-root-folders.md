---
title: Bronhoofdmappen (ir.resourceRootPaths)
description: Een lijst met paden, gescheiden door puntkomma's, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Bronhoofdmappen (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Een lijst met paden, gescheiden door puntkomma&#39;s, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.

Dit kunnen absolute paden of paden zijn ten opzichte van *[!DNL install_folder]*. Wanneer meerdere paden zijn opgegeven, probeert de server elke hoofdmap in de gegeven volgorde tot het bestand is gevonden. De standaardwaarde is [!DNL ./resources], voor een standaardhoofdpad van [!DNL install_folder/resources].
