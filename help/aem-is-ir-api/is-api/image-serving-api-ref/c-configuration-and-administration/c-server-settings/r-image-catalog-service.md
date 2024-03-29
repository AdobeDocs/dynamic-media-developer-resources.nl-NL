---
description: Gebruik deze serverinstellingen voor de afbeeldingscatalogusservice.
solution: Experience Manager
title: Afbeeldingscatalogusservice
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Afbeeldingscatalogusservice{#image-catalog-service}

Gebruik deze serverinstellingen voor de afbeeldingscatalogusservice.

## CS::catalog.rootPath - Map met afbeeldingscatalogus {#section-02d107f157384b18835f884f24fea3aa}

Locatie van de map met de afbeeldingscatalogus (waar alle [!DNL catalog.ini] bestanden moeten worden gevonden). Dit kan een absoluut bestandspad zijn of een pad dat relatief is ten opzichte van *[!DNL install_folder]*. De server bewaakt deze map voortdurend en laadt of herlaadt catalogi wanneer een nieuw hoofdcatalogusbestand (met [!DNL .ini] achtervoegsel) wordt gedetecteerd of wanneer de laatste gewijzigde tijd van een bestaand hoofdcatalogusbestand is gewijzigd.

## CS::catalog.cacheRoot - Cataloguscachemap {#section-73e499c3a5974f1aa4251e70272ff503}

De hoofdmap voor de cache van het catalogussysteem. Kan op hetzelfde worden ingesteld als een van de mappen in `PS::cache.rootPaths`. De map moet handmatig worden gemaakt voordat deze instelling wordt gewijzigd.

## CS::catalog.modificationWaitTime - Vertraging bij parseren catalogusbestand {#section-7348065bcc124cb68ea947bf1b9b0845}

Tijd in msec de catalogusdienst wacht na a [!DNL catalog.ini] bestand wordt gewijzigd totdat de secundaire catalogusbestanden worden geladen. Deze vertraging zorgt ervoor dat alle secundaire catalogusbestanden up-to-date zijn voordat de catalogusservice deze probeert te laden. Geheel getal in msec.

## CS::catalog.refreshInterval - Frequentie voor bestandscontrole van catalogus {#section-517fefc1d8784777a1026abec8630d58}

Frequentie waarop de catalogusservice controleert of er wijzigingen zijn aangebracht in afbeeldingscatalogi. Geheel getal in msec.
