---
description: Gebruik deze procedure bij het upgraden van Scene7 Image Serving op Linux.
seo-description: Gebruik deze procedure bij het upgraden van Scene7 Image Serving op Linux.
seo-title: Bijwerken vanaf IS 4.7.4 of hoger
solution: Experience Manager
title: Bijwerken vanaf IS 4.7.4 of hoger
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Scene7 Image Serving op Linux.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

De [!DNL webapps] map kan bij een upgrade worden verwijderd. Maak een back-up van de [!DNL webapps] map voordat u de upgrade uitvoert.

1. Meld u aan bij de serverhost met de basisrechten.
1. Decomprimeer en verwijder het Teerbestand voor distributie van Image Serving.
1. Voer uit [!DNL ./install-is] om de installatiewizard te starten die zich in de [!DNL setup] map bevindt.

   Het updateinstallatieprogramma controleert de integriteit en de versie van het geïnstalleerde pakket. Als dit lukt, wordt de licentieovereenkomst voor eindgebruikers (EULA) weergegeven.
1. Lees de licentieovereenkomst en voer &quot; **[!UICONTROL y]**&quot; in om door te gaan met de installatie.

   Het installatieprogramma maakt een back-up van de oude configuratiebestanden van de server naar de [!DNL BACKUP/] map.

   Wanneer de installatie is voltooid, wordt het volgende bericht getoond:

   `Image Server was started successfully`

Tijdens een update wordt het [!DNL ImageServing/conf/server.xml] bestand bijgewerkt naar de meest recente instellingen. Als u waarden hebt gewijzigd of toegevoegd, slaat u uw bestaande wijzigingen op [!DNL server.xml] en implementeert u deze na de upgrade opnieuw.

Na een update-installatie kunt u overwegen de HTTP-responscache op te warmen voordat u de server live gaat. Raadpleeg de beschrijving van het [!DNL playlog] hulpprogramma voor meer informatie.
