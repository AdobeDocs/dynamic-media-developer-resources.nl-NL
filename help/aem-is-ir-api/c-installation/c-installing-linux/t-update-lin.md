---
title: Bijwerken vanaf IS 4.7.4 of hoger
description: Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving op Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving op Linux®.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

De [!DNL webapps] kan worden verwijderd bij een upgrade. Maak een back-up van de [!DNL webapps] voor upgrade.

1. Meld u aan bij de serverhost met de basisrechten.
1. Decomprimeer en verwijder het Teerbestand voor distributie van Image Serving.
1. In de [!DNL setup] map, uitvoeren [!DNL `./install-is`] om de installatiewizard te starten.

   Het updateinstallatieprogramma controleert de integriteit en de versie van het geïnstalleerde pakket. Als dit lukt, wordt de licentieovereenkomst voor eindgebruikers (EULA) weergegeven.
1. Lees de licentieovereenkomst en typ vervolgens **[!UICONTROL y]** om door te gaan met de installatie.

   Het installatieprogramma maakt een back-up van de oude serverconfiguratiebestanden naar de [!DNL BACKUP/] map.

   Wanneer de installatie is voltooid, wordt het volgende bericht getoond:

   `Image Server was started successfully`

Tijdens een update worden de [!DNL ImageServing/conf/server.xml] wordt bijgewerkt naar de meest recente instellingen. Als u waarden hebt gewijzigd of toegevoegd, slaat u uw bestaande [!DNL server.xml] en implementeer uw wijzigingen na de upgrade opnieuw.

Na een update-installatie kunt u de HTTP-responscache opwarmen voordat u de server live gaat. Zie de beschrijving van de [!DNL playlog] voor meer informatie.
