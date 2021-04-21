---
description: Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving op Linux.
solution: Experience Manager
title: Bijwerken vanaf IS 4.7.4 of hoger
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving op Linux.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

De map [!DNL webapps] kan bij een upgrade worden verwijderd. Maak een back-up van de map [!DNL webapps] voordat u de upgrade uitvoert.

1. Meld u aan bij de serverhost met de basisrechten.
1. Decomprimeer en verwijder het Teerbestand voor distributie van Image Serving.
1. Voer [!DNL ./install-is] uit om de installatiewizard te starten die zich in de map [!DNL setup] bevindt.

   Het updateinstallatieprogramma controleert de integriteit en de versie van het geïnstalleerde pakket. Als dit lukt, wordt de licentieovereenkomst voor eindgebruikers (EULA) weergegeven.
1. Lees de licentieovereenkomst en voer &quot;**[!UICONTROL y]**&quot; in om door te gaan met de installatie.

   Het installatieprogramma maakt een back-up van de oude serverconfiguratiebestanden in de map [!DNL BACKUP/].

   Wanneer de installatie is voltooid, wordt het volgende bericht getoond:

   `Image Server was started successfully`

Tijdens een update wordt het [!DNL ImageServing/conf/server.xml]-bestand bijgewerkt naar de meest recente instellingen. Als u om het even welke waarden hebt veranderd of toegevoegd zou u uw bestaande [!DNL server.xml] moeten bewaren en uw veranderingen na de verbetering opnieuw uitvoeren.

Na een update-installatie kunt u overwegen de HTTP-responscache op te warmen voordat u de server live gaat. Raadpleeg de beschrijving van het hulpprogramma [!DNL playlog] voor meer informatie.
