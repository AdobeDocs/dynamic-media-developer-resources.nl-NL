---
title: Systeemvereisten voor Dynamic Media HTML5-viewers
description: Systeemvereisten voor Dynamic Media HTML5-viewers.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Dynamic Media HTML5-systeemvereisten voor viewers{#system-requirements}

Systeemvereisten voor Dynamic Media HTML5-viewers.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Serverhardware en -software {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 of later.
* Voor HTML5-viewers zijn SDK JavaScript Server-side bibliotheken 3.11.5 of hoger vereist.
* *Een vriend e-mailen* voor sociale functies is s7ondemand 5.0.9 of hoger vereist.
* eCatalog-viewer - [Pop-up deelvenster Info](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) Voor ondersteuning is infoserver 2.1.8 of hoger vereist.
* Componenten van zoekfuncties vereisen s7search 2.3.0 of hoger.

## Systeemvereisten voor viewers {#section-cc72b1e209524d038b4d5b92b35e998e}

**Minimumeisen voor de clientbrowser voor componentviewers:**

* Ondersteund in de volgende versies van het besturingssysteem of hoger:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Ondersteund in de volgende browser/platformversies of hoger:
   * Android™ OS 4.x
   * BlackBerry® 10 op native browsers. Alleen het afspelen van video wordt ondersteund.
   * Chroom 82
   * Rand
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (alleen voor Safari- en Chrome-browsers)
   * iPhone 3GS
   * Safari 11
* Internet Explorer op mobiele apparaten wordt niet ondersteund.
* *PanoramaViewer* wordt ondersteund door de volgende browser/platformversies of hoger:
   * Android™ 4.4 (alleen telefoonapparaten)
   * Chroom 82
   * Rand
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* en *DimensionalViewer* wordt ondersteund door de volgende browser/platformversies of hoger:
   * Android™ 5 (alleen telefoonapparaten)
   * Chroom 82
   * Rand
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* wordt ondersteund door de volgende browser/platformversies of hoger:
   * Android™ 4.x
   * Chroom 82
   * Rand
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## Einde ondersteuning voor TLS 1.0 en 1.1 {#tls}

<!-- CQDOC-19433 -->

Vanaf 30 september 2022 is de ondersteuning voor Adobe Dynamic Media Viewers beëindigd voor:

* TLS (Transport Layer Security) 1.0 en 1.1
* De volgende zwakke ciphers in TLS 1.2:
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Niet-ondersteunde combinaties van webbrowser en besturingssysteem voor Dynamic Media Viewers {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media Viewers biedt geen ondersteuning voor de volgende webbrowser- en besturingssysteemcombinaties:

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1-update
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

