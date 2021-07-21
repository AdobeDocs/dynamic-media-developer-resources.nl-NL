---
description: Gebruik deze serverinstellingen voor SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# SSL{#ssl}

Gebruik deze serverinstellingen voor SSL.

## TC::SslPort - Luisterpoort {#section-c80eb582bf684b3fa7313a77cc606769}

Specificeert de luisterpoort voor de Server van het Platform voor SSL verbindingen. De standaardwaarde is 8443.

## TC::sleutelarchiefbestand - Bestandspad sleutelarchief {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geef het pad/de naam van het SSL-sleutelarchiefbestand op. Kan een absoluut pad of een pad zijn ten opzichte van [!DNL *[!DNL install_folder]*/conf]. De standaardwaarde is *install_folder*/conf/scene7keystore.

## TC::sleutelarchiefDoorgeven - Wachtwoord sleutelarchief {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Het wachtwoord voor het sleutelarchiefbestand. De standaardwaarde is `scene7`.

## TC::sleutelarchieftype - Type sleutelarchief {#section-8f263e1ba67740728cd39181960d7c7d}

Selecteer het type sleutelarchief. &#39; `Java'` (standaardwaarde) en &#39; `PKCS12`&#39; worden ondersteund.
