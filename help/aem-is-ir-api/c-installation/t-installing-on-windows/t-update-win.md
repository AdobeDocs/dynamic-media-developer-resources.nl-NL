---
description: Gebruik deze procedure wanneer het bevorderen van de Serving van het Beeld Scene7.
seo-description: Gebruik deze procedure wanneer het bevorderen van de Serving van het Beeld Scene7.
seo-title: Bijwerken vanaf IS 4.7.4 of hoger
solution: Experience Manager
title: Bijwerken vanaf IS 4.7.4 of hoger
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure wanneer het bevorderen van de Serving van het Beeld Scene7.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

>[!NOTE]
>
>De [!DNL webapps] map kan bij een upgrade worden verwijderd. Maak een back-up van de [!DNL webapps] map voordat u de upgrade uitvoert.

1. Meld u met beheerdersrechten aan bij uw serverhost.
1. Extraheer de inhoud van het ZIP-bestand van de Afbeeldingsserver.
1. Voer setup/setup.exe uit om de installatiewizard te starten.
1. Klik **[!UICONTROL Next]** om naar de licentieovereenkomst voor eindgebruikers (EULA) te gaan, lees de licentieovereenkomst en klik op **[!UICONTROL Yes]**.

   Op de volgende pagina worden de vorige configuratie-instellingen weergegeven.
1. Klik **[!UICONTROL Next]** om de update-installatie te starten.

   >[!NOTE]
   >
   >Het installatieprogramma maakt een back-up van de oude configuratiebestanden van de server naar de [!DNL BACKUP/] map.

1. Als de installatie is voltooid, klikt u op Voltooien om de installatiewizard af te sluiten.

   In sommige gevallen kan de installatiewizard vragen het systeem opnieuw op te starten.
>Tijdens een update wordt het [!DNL ImageServing/conf/server.xml] bestand bijgewerkt naar de meest recente instellingen. Als u waarden hebt gewijzigd of toegevoegd, slaat u uw bestaande wijzigingen op [!DNL server.xml] en implementeert u deze na de upgrade opnieuw.
>
>Na een update-installatie kunt u overwegen de HTTP-responscache op te warmen voordat u de server live gaat. Raadpleeg de beschrijving van het `playlog` hulpprogramma voor meer informatie.

