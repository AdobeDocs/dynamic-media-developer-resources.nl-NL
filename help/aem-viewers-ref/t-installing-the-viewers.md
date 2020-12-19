---
description: Instructies voor het installeren van de Dynamic Media Viewers API.
seo-description: Instructies voor het installeren van de Dynamic Media Viewers API.
seo-title: Meerdere viewers op dezelfde server installeren
solution: Experience Manager
title: Meerdere viewers op dezelfde server installeren
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Meerdere viewers op dezelfde server installeren{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructies voor het installeren van de API voor Dynamic Media-viewers.

Installeer en test Image Serving voordat u de viewers voor Image Serving installeert.

Kopieer de bestanden voor IS-viewers naar de vaste schijf en implementeer het bestand `s7viewers.war` in de map `../ImageServing/webapps`. Raadpleeg de documentatie bij Image Serving voor instructies over het implementeren, starten, stoppen en beheren van de Image Server.

>[!NOTE]
>
>Er is geen upgrade-installatie voor de viewers van Image Serving. Adobe raadt u aan een back-up te maken van een bestaande map voor Dynamic Media-viewers voordat u verdergaat met de installatie.

**De viewers op dezelfde server installeren**

1. Wijzig de naam van de viewer .war in de gewenste context en stel het bestand in op de gewenste locatie.
1. Stel de parameter `this.isViewerRoot` in `config.js` in.
1. Open `config.js` in de hoofdmap van de nieuwe viewermap.
1. Stel parameter `this.isViewerRoot = "/s7viewers"` in op de context van het `s7viewers.war`-bestand. Bijvoorbeeld, `"/s7viewers-4.0"`. Sla het bestand op en sluit het.
1. Sla het bestand op en sluit het.
