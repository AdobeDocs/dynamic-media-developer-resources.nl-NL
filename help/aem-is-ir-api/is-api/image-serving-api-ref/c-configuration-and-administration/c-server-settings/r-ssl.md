---
description: Gebruik deze serverinstellingen voor SSL.
seo-description: Gebruik deze serverinstellingen voor SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

Gebruik deze serverinstellingen voor SSL.

## TC::SslPort - Luisterpoort {#section-c80eb582bf684b3fa7313a77cc606769}

Specificeert de luisterpoort voor de Server van het Platform voor SSL verbindingen. De standaardwaarde is 8443.

## TC::sleutelarchiefbestand - Bestandspad sleutelarchief {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geef het pad/de naam van het SSL-sleutelarchiefbestand op. Kan een absoluut pad of een pad zijn ten opzichte van [!DNL *[!DNL install_folder]*/conf]. Standaard is *install_folder*/conf/scene7keystore.

## TC::sleutelarchiefDoorgeven - Wachtwoord sleutelarchief {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Het wachtwoord voor het sleutelarchiefbestand. Standaard is dit `scene7`.

## TC::sleutelarchieftype - Type sleutelarchief {#section-8f263e1ba67740728cd39181960d7c7d}

Selecteer het type sleutelarchief. &#39; `Java'` (standaardwaarde) en &#39; `PKCS12`&#39; worden ondersteund.
