---
title: Meerdere Dynamic Media-viewers op dezelfde server installeren
description: Instructies voor het installeren van de Dynamic Media Viewers API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Meerdere viewers op dezelfde server installeren{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructies voor het installeren van de API voor Dynamic Media-viewers.

Installeer en test Image Serving voordat u de viewers voor Image Serving installeert.

Kopieer de bestanden met IS Viewers naar de vaste schijf en implementeer vervolgens de `s7viewers.war` in het bestand `../ImageServing/webapps` directory. Raadpleeg de documentatie bij Image Serving voor instructies over het implementeren, starten, stoppen en beheren van de Image Server.

>[!NOTE]
>
>Er is geen upgrade-installatie voor de viewers van Image Serving. Adobe raadt u aan een back-up te maken van een bestaande map voor Dynamic Media-viewers (s7viewers) voordat u verdergaat met de installatie.

**Meerdere viewers op dezelfde server installeren:**

1. Wijzig de naam van de viewer .war in de gewenste context en stel het bestand in op de gewenste locatie.
1. Set `this.isViewerRoot` parameter in `config.js`.
1. Openen `config.js` in de hoofdmap van de nieuwe viewermap.
1. Parameter instellen `this.isViewerRoot = "/s7viewers"` in de context van de `s7viewers.war` bestand. Bijvoorbeeld: `"/s7viewers-4.0"`.
1. Sla het bestand op en sluit het.
