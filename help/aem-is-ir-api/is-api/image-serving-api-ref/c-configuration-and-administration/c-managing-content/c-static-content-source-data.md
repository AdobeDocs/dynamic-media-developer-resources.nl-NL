---
description: Statische gegevensbestanden van inhoudsbronnen worden alleen benaderd door de [!DNL Platform Server].
solution: Experience Manager
title: Statische brongegevens van inhoud
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Statische brongegevens van inhoud{#static-content-source-data}

Statische gegevensbestanden van inhoudsbronnen worden alleen benaderd door de [!DNL Platform Server].

Het pad voor bestanden met statische inhoudsgegevens wordt als volgt opgelost:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

De server combineert padsegmenten van rechts naar links totdat een absoluut bestandspad is ingesteld.

Alles ` *[!DNL rootPath]*` segmenten kunnen leeg, relatief of absoluut zijn.

` *[!DNL catalogPath]*` is een absoluut of relatief bestandspad/-naam. *[!DNL requestPath]* moet een relatief bestandspad/-naam zijn.

Meerdere `PS::staticContent.rootPaths` waarden kunnen worden gedefinieerd in [!DNL PlatformServer.conf]. Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De [!DNL Platform Server] Hiermee probeert u alternatieve paden in de opgegeven volgorde totdat het gegevensbestand wordt gevonden.
