---
description: Gebruik deze serverinstellingen voor SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# SSL{#ssl}

Gebruik deze serverinstellingen voor SSL.

## TC::SslPort - Luisterpoort {#section-c80eb582bf684b3fa7313a77cc606769}

Geeft de luisterpoort aan voor de [!DNL Platform Server] voor SSL-verbindingen. De standaardwaarde is 8443.

## TC::sleutelarchiefbestand - Bestandspad sleutelarchief {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geef het pad/de naam van het SSL-sleutelarchiefbestand op. Kan een absoluut pad of een pad zijn ten opzichte van [!DNL *[!DNL install_folder]*/conf]. Standaard is *install_folder*/conf/scene7keystore.

## TC::sleutelarchiefDoorgeven - Wachtwoord sleutelarchief {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Het wachtwoord voor het sleutelarchiefbestand. Standaard is `scene7`.

## TC::sleutelarchieftype - Type sleutelarchief {#section-8f263e1ba67740728cd39181960d7c7d}

Selecteer het type sleutelarchief. &#39; `Java'` (standaardwaarde) en &#39; `PKCS12`&#39; worden ondersteund.
