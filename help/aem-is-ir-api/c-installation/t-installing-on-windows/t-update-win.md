---
description: Gebruik deze procedure bij het upgraden van Scene7 Image Serving.
seo-description: Gebruik deze procedure bij het upgraden van Scene7 Image Serving.
seo-title: Bijwerken vanaf IS 4.7.4 of hoger
solution: Experience Manager
title: Bijwerken vanaf IS 4.7.4 of hoger
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Scene7 Image Serving.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

>[!NOTE]
>
>De map [!DNL webapps] kan bij een upgrade worden verwijderd. Maak een back-up van de map [!DNL webapps] voordat u de upgrade uitvoert.

1. Meld u met beheerdersrechten aan bij uw serverhost.
1. Extraheer de inhoud van het ZIP-bestand van de Afbeeldingsserver.
1. Voer setup/setup.exe uit om de installatiewizard te starten.
1. Klik **[!UICONTROL Next]** om naar de licentieovereenkomst voor eindgebruikers (EULA) te gaan, lees de licentieovereenkomst en klik op **[!UICONTROL Yes]**.

   Op de volgende pagina worden de vorige configuratie-instellingen weergegeven.
1. Klik **[!UICONTROL Next]** om de updateinstallatie te beginnen.

   >[!NOTE]
   >
   >Het installatieprogramma maakt een back-up van de oude serverconfiguratiebestanden in de map [!DNL BACKUP/].

1. Als de installatie is voltooid, klikt u op Voltooien om de installatiewizard af te sluiten.

   In sommige gevallen kan de installatiewizard vragen het systeem opnieuw op te starten.

Tijdens een update wordt het [!DNL ImageServing/conf/server.xml]-bestand bijgewerkt naar de meest recente instellingen. Als u om het even welke waarden hebt veranderd of toegevoegd zou u uw bestaande [!DNL server.xml] moeten bewaren en uw veranderingen na de verbetering opnieuw uitvoeren.

Na een update-installatie kunt u overwegen de HTTP-responscache op te warmen voordat u de server live gaat. Raadpleeg de beschrijving van het hulpprogramma `playlog` voor meer informatie.
