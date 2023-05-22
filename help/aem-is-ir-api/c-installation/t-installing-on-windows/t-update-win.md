---
title: Bijwerken vanaf IS 4.7.4 of hoger
description: Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Bijwerken vanaf IS 4.7.4 of hoger{#updating-from-is-or-later}

Gebruik deze procedure bij het upgraden van Dynamic Media Image Serving.

Als u een upgrade uitvoert van een oudere versie van Image Serving, neemt u contact op met de ondersteuning voor het juiste proces.

>[!NOTE]
>
>De [!DNL webapps] kan worden verwijderd tijdens de upgrade. Maak een back-up van de [!DNL webapps] voor upgrade.

1. Meld u met beheerdersrechten aan bij uw serverhost.
1. Extraheer de inhoud van het ZIP-bestand van de Afbeeldingsserver.
1. De installatiewizard starten door `setup/setup.exe`.
1. Selecteren **[!UICONTROL Next]** om naar de licentieovereenkomst voor eindgebruikers (EULA) te gaan, leest u de licentieovereenkomst en selecteert u **[!UICONTROL Yes]**.

   Op de volgende pagina worden de vorige configuratie-instellingen weergegeven.
1. Klikken **[!UICONTROL Next]** om de installatie van de update te starten.

   >[!NOTE]
   >
   >Het installatieprogramma maakt een back-up van de oude serverconfiguratiebestanden naar de [!DNL BACKUP/] map.

1. Selecteer **[!UICONTROL Finish]** om de installatiewizard af te sluiten.

   Soms vraagt de installatiewizard u het systeem opnieuw op te starten.

Tijdens een update worden de [!DNL ImageServing/conf/server.xml] wordt bijgewerkt naar de meest recente instellingen. Als u waarden hebt gewijzigd of toegevoegd, moet u de bestaande waarden opslaan [!DNL server.xml] en implementeer uw wijzigingen na de upgrade opnieuw.

Na een update-installatie kunt u de HTTP-responscache opwarmen voordat u de server live gaat. Zie de beschrijving van de `playlog` voor meer informatie.
