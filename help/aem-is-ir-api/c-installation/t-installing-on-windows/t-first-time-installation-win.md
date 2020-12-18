---
description: Gebruik deze stappen om Image Serving voor het eerst op Vensters te installeren.
seo-description: Gebruik deze stappen om Image Serving voor het eerst op Vensters te installeren.
seo-title: Voor het eerst installeren
solution: Experience Manager
title: Voor het eerst installeren
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Voor het eerst installeren{#installing-for-the-first-time}

Gebruik deze stappen om Image Serving voor het eerst op Vensters te installeren.

1. Meld u met beheerdersrechten aan bij uw serverhost.
1. Als u al een licentie hebt ontvangen, kopieert u deze naar uw server en voert u de installatie van de licentie uit door op het bestand te dubbelklikken.

   Als u nog geen licentie hebt, kunt u verdergaan met de installatie en de licentie later installeren.
1. Extraheer de inhoud van het ZIP-bestand van de Afbeeldingsserver.
1. Voer [!DNL setup]/ [!DNL setup.exe] uit om de installatiewizard te starten.
1. Klik op Volgende om naar de licentieovereenkomst voor eindgebruikers (EULA) te gaan, lees de licentieovereenkomst en klik op **[!UICONTROL Yes]**.

   Het dialoogvenster [!DNL Authentication] wordt hierna weergegeven.
1. Als er al een licentie is geïnstalleerd en de licentiegegevens worden weergegeven in het dialoogvenster [!DNL Authentication], klikt u op **[!UICONTROL Next]** om door te gaan.

   Als u geen licentie hebt, klikt u op **[!UICONTROL Request License]**. In het volgende dialoogvenster ziet u een van de MAC-adressen van de netwerkinterfacekaart van uw computer. E-mail dit adres van MAC, uw bedrijfsnaam, en het product u zoals die door de herinnering wordt geleid installeert.

   **Belangrijk:** de licentie is gebaseerd op het MAC-adres van een van de netwerkinterfacekaarten die op deze host zijn geïnstalleerd. Als u deze kaart uitschakelt, verwijdert of vervangt, wordt de licentie niet meer als geldig herkend. Ben zeker om een vergunning voor de hardwareconfiguratie te verkrijgen die u voor IS zult gebruiken.

   U kunt IS zonder geldige licentie blijven installeren en de licentie later installeren. Als u wilt doorgaan, klikt u op **[!UICONTROL Back]** om terug te keren naar het dialoogvenster [!DNL Authentication] en klikt u vervolgens op **[!UICONTROL Next]**.
1. Ga aan de pagina van de Montages van het Beheer van de Server van het Platform te werk. Voer zonodig nieuwe waarden in of accepteer de standaardinstellingen.

   U kunt de volgende punten vormen:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> HTTP-verbindingspoort Platform Server </p> </td> 
   <td> <p>Hoofd HTTP luisterende haven voor het Beeld Serven en het Teruggeven van het Beeld </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Admin Listening Port </p> </td> 
   <td> <p>Admin Listening Port </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Cachegrootte Platform-server in MB </p> </td> 
   <td> <p>Oorspronkelijke grootte van de hoofdresponscache </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Cachelocatie Platform-server </p> </td> 
   <td> <p>PS-cachemap </p> </td> 
  </tr> 
 </tbody> 
</table>

De gespecificeerde aantallen van de haven moeten uniek zijn en niet gebruikt door andere toepassingen of de diensten.

In het volgende scherm kunt u de geselecteerde instellingen bekijken.
1. Klik **[!UICONTROL Back]** om veranderingen aan te brengen, of **[!UICONTROL Next]** te klikken om de installatie te beginnen.
1. Klik **[!UICONTROL Finish]** om de installatietovenaar weg te gaan.
