---
description: Een lijst met paden, gescheiden door puntkomma's, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.
solution: Experience Manager
title: Bronhoofdmappen (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Bronhoofdmappen (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Een lijst met paden, gescheiden door puntkomma&#39;s, fungeert als basis voor alle gegevensbestanden met relatieve bestandspaden.

Dit kunnen absolute paden of paden zijn ten opzichte van *[!DNL install_folder]*. Wanneer meerdere paden zijn opgegeven, probeert de server elke hoofdmap in de gegeven volgorde uit tot het bestand is gevonden. De standaardwaarde is [!DNL ./resources], voor een standaardwortelweg van [!DNL install_folder/resources].
