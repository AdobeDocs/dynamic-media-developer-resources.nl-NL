---
description: Gebruik deze serverinstellingen voor de afbeeldingscatalogusservice.
seo-description: Gebruik deze serverinstellingen voor de afbeeldingscatalogusservice.
seo-title: Afbeeldingscatalogusservice
solution: Experience Manager
title: Afbeeldingscatalogusservice
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Afbeeldingscatalogusservice{#image-catalog-service}

Gebruik deze serverinstellingen voor de afbeeldingscatalogusservice.

## CS::catalog.rootPath - Map met afbeeldingscatalogus {#section-02d107f157384b18835f884f24fea3aa}

Locatie van de map met de afbeeldingscatalogus (waar alle [!DNL catalog.ini] bestanden moeten staan). Dit kan een absoluut bestandspad zijn of een pad dat relatief is ten opzichte van het pad *[!DNL install_folder]*. De server bewaakt deze map voortdurend en laadt of herlaadt catalogi wanneer een nieuw hoofdcatalogusbestand (met [!DNL .ini] achtervoegsel) wordt gevonden of wanneer de laatste gewijzigde tijd van een bestaand hoofdcatalogusbestand is gewijzigd.

## CS::catalog.cacheRoot - Cataloguscachemap {#section-73e499c3a5974f1aa4251e70272ff503}

De hoofdmap voor de cache van het catalogussysteem. Kan op hetzelfde worden ingesteld als een van de mappen in `PS::cache.rootPaths`. De map moet handmatig worden gemaakt voordat deze instelling wordt gewijzigd.

## CS::catalog.modificationWaitTime - Vertraging bij parseren catalogusbestand {#section-7348065bcc124cb68ea947bf1b9b0845}

Tijd in msec de catalogusdienst wacht nadat een [!DNL catalog.ini] dossier wordt veranderd tot het de secundaire catalogusdossiers laadt. Deze vertraging zorgt ervoor dat alle secundaire catalogusbestanden up-to-date zijn voordat de catalogusservice deze probeert te laden. Geheel getal in msec.

## CS::catalog.refreshInterval - Frequentie voor bestandscontrole van catalogus {#section-517fefc1d8784777a1026abec8630d58}

Frequentie waarop de catalogusservice controleert op wijzigingen in afbeeldingscatalogi. Geheel getal in msec.
