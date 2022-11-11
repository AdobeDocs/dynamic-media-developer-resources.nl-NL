---
title: Voor het eerst installeren
description: Gebruik deze stappen om Image Serving voor het eerst op Vensters te installeren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Voor het eerst installeren{#installing-for-the-first-time}

Gebruik deze stappen om Image Serving voor het eerst op Vensters te installeren.

1. Meld u met beheerdersrechten aan bij uw serverhost.
1. Als u al een licentie hebt ontvangen, kopieert u deze naar uw server en voert u de installatie van de licentie uit door op het bestand te dubbelklikken.

   Als u nog geen licentie hebt, kunt u verdergaan met de installatie en de licentie later installeren.

1. Extraheer de inhoud van het ZIP-bestand van de Afbeeldingsserver.
1. De installatiewizard starten door uit te voeren [!DNL setup]/ [!DNL setup.exe].
1. Selecteren **[!UICONTROL Next]** om naar de licentieovereenkomst voor eindgebruikers (EULA) te gaan, leest u de licentieovereenkomst en selecteert u **[!UICONTROL Yes]**.

   De [!DNL Authentication] wordt de volgende weergegeven.
1. Als er al een licentie is geïnstalleerd en de licentiegegevens worden weergegeven in het dialoogvenster [!DNL Authentication] dialoogvenster selecteert u **[!UICONTROL Next]** om door te gaan.

   Als u geen licentie hebt, selecteert u **[!UICONTROL Request License]**. In het volgende dialoogvenster ziet u een van de MAC-adressen van de netwerkinterfacekaart van uw computer. Stuur een e-mail naar dit MAC-adres, uw bedrijfsnaam en het product dat u installeert, op de aanwijzing van de vraag.

   **Belangrijk:** De licentie is gebaseerd op het MAC-adres van een van de netwerkinterfacekaarten die op deze host zijn geïnstalleerd. Als u deze kaart uitschakelt, verwijdert of vervangt, wordt de licentie niet meer als geldig herkend. Zorg ervoor dat u een licentie verkrijgt voor de hardwareconfiguratie die u gebruikt voor het uitvoeren van images.

   U kunt IS zonder geldige licentie blijven installeren en de licentie later installeren. Selecteer **[!UICONTROL Back]** om terug te keren naar de [!DNL Authentication] en selecteert u vervolgens **[!UICONTROL Next]**.
1. Ga door naar &quot;[!DNL Platform Server] De pagina Beheerinstellingen.&quot; Voer zonodig nieuwe waarden in of accepteer de standaardinstellingen.

   U kunt de volgende punten vormen:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP-verbindingspoort </p> </td>
      <td> <p>Hoofd HTTP luisterende haven voor het Beeld Serven en het Teruggeven van het Beeld </p> </td>
   </tr> 
   <tr> 
      <td> <p> Admin Listening Port </p> </td>
      <td> <p>Admin Listening Port </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] Cachegrootte in MB </p> </td>
      <td> <p>Oorspronkelijke grootte van de hoofdresponscache </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Cachelocatie </p> </td>
      <td> <p>PS-cachemap </p> </td>
   </tr>
   </tbody>
   </table>

   De gespecificeerde aantallen van de haven moeten uniek zijn en niet gebruikt door andere toepassingen of de diensten.

   In het volgende scherm kunt u de geselecteerde instellingen bekijken.

1. Selecteren **[!UICONTROL Back]** om wijzigingen aan te brengen, of selecteer **[!UICONTROL Next]** om de installatie te starten.

1. Selecteren **[!UICONTROL Finish]** om de installatiewizard af te sluiten.
