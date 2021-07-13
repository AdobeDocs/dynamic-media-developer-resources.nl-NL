---
description: Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving.
solution: Experience Manager
title: Bijwerken vanaf IS 4.7.4 of hoger
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving.

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
