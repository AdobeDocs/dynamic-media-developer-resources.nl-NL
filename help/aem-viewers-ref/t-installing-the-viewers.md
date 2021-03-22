---
title: Meerdere Dynamic Media-viewers op dezelfde server installeren
description: Instructies voor het installeren van de Dynamic Media Viewers API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Meerdere viewers op dezelfde server installeren{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructies voor het installeren van de API voor Dynamic Media-viewers.

Installeer en test Image Serving voordat u de viewers voor Image Serving installeert.

Kopieer de bestanden voor IS-viewers naar de vaste schijf en implementeer het bestand `s7viewers.war` in de map `../ImageServing/webapps`. Raadpleeg de documentatie bij Image Serving voor instructies over het implementeren, starten, stoppen en beheren van de Image Server.

>[!NOTE]
>
>Er is geen upgrade-installatie voor de viewers van Image Serving. Adobe raadt u aan een back-up te maken van een bestaande map voor Dynamic Media-viewers (s7viewers) voordat u verdergaat met de installatie.

**Meerdere viewers op dezelfde server installeren**

1. Wijzig de naam van de viewer .war in de gewenste context en stel het bestand in op de gewenste locatie.
1. Stel de parameter `this.isViewerRoot` in `config.js` in.
1. Open `config.js` in de hoofdmap van de nieuwe viewermap.
1. Stel parameter `this.isViewerRoot = "/s7viewers"` in op de context van het `s7viewers.war`-bestand. Bijvoorbeeld, `"/s7viewers-4.0"`.
1. Sla het bestand op en sluit het.
