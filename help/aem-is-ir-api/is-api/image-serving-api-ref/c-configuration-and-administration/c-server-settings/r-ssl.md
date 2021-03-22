---
description: Gebruik deze serverinstellingen voor SSL.
seo-description: Gebruik deze serverinstellingen voor SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# SSL{#ssl}

Gebruik deze serverinstellingen voor SSL.

## TC::SslPort - Luisterpoort {#section-c80eb582bf684b3fa7313a77cc606769}

Specificeert de luisterpoort voor de Server van het Platform voor SSL verbindingen. De standaardwaarde is 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geef het pad/de naam van het SSL-sleutelarchiefbestand op. Kan een absoluut pad of een pad zijn ten opzichte van [!DNL *[!DNL install_folder]*/conf]. De standaardwaarde is *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore-wachtwoord {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Het wachtwoord voor het sleutelarchiefbestand. De standaardwaarde is `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Selecteer het type sleutelarchief. &#39; `Java'` (standaardwaarde) en &#39; `PKCS12`&#39; worden ondersteund.
