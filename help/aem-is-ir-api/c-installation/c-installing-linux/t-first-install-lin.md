---
description: Deze procedure laat zien hoe u Image Serving voor het eerst in Linux kunt installeren.
seo-description: Deze procedure laat zien hoe u Image Serving voor het eerst in Linux kunt installeren.
seo-title: Voor het eerst installeren
solution: Experience Manager
title: Voor het eerst installeren
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---


# Voor het eerst installeren{#installing-for-the-first-time}

Deze procedure laat zien hoe u Image Serving voor het eerst in Linux kunt installeren.

1. Meld u aan bij de serverhost met basismachtigingen.
1. Maak de map [!DNL /usr/local/scene7/licenses].

   Als het licentiesleutelbestand voor Beeldbewerking en/of Afbeelding renderen (met het bestandsachtervoegsel [!DNL .sc8]) beschikbaar is, kopieert u dit naar deze map. Anders gaat u verder met de installatie en installeert u de licentiecode later.
1. Decomprimeer en verwijder het Teerbestand voor distributie van Image Serving.
1. Voer [!DNL ./install-is] uit in de map [!DNL Setup] om de installatiewizard te starten.

   Als er geen licentiecode wordt gevonden, worden instructies weergegeven die beschrijven hoe u een licentiebestand kunt verkrijgen. Doe dit op dit moment of ga verder met de installatie van Image Serving en installeer de licentiecode later.
1. Wanneer de licentieovereenkomst voor eindgebruikers (EULA) wordt weergegeven, leest u de licentieovereenkomst en voert u `y` in om door te gaan.

   In het installatieprogramma worden de aanwijzingen weergegeven die in de volgende tabel worden weergegeven.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Hoofdpoort voor luisteren [8080]:</span> </p> </td> 
   <td colname="col2"> <p>HoofdHTTP-luisterpoort voor Beeldservers en Afbeeldingsrendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin Listening Port [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Admin-luisterpoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximale grootte HTTP-cache (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Oorspronkelijke grootte van de hoofdresponscache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Hoofdmap in cache [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS-cachemap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Eigenaar-id van afbeeldingsserver [root]:</span> </p> </td> 
   <td colname="col2"> <p>De gebruikersaccount waaronder Image Serving-servers moeten worden geïnstalleerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Id van afbeeldingsservergroep [root]:</span> </p> </td> 
   <td colname="col2"> <p>The group account under which Image Serving servers is to be installed. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Druk op **[!UICONTROL Enter]** om de standaardwaarde te accepteren of een andere waarde op te geven.

   Zorg ervoor dat alle opgegeven poortnummers uniek zijn en niet op een andere manier op deze host worden gebruikt.

   >[!IMPORTANT]
   >
   >Als een andere rekening dan wortel wordt gespecificeerd, moet u ervoor zorgen dat de toegangstoestemmingen voor alle dossiers en omslagen de Server van het Beeld moet lezen en/of schrijven correct opstelling zijn wanneer deze omslagen in de configuratiedossiers worden aangepast.
   >
   >Beeldserver is nu geïnstalleerd op [!DNL /usr/local/Scene7/ImageServing]. Bepaalde inhoud voor het renderen van afbeeldingen is geïnstalleerd op [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Tegen het einde van de installatie probeert de installatiewizard Image Server te starten. Als er geen geldige licentiecode wordt gevonden, kan de imageserver niet worden gestart. Als er een geldige vergunning is en de Server van het Beeld niet opstelling is, raadpleeg de logboekdossiers.

>[!NOTE]
>
>Als de licentie na de installatie van Image Serving is geïnstalleerd, moet de Image Server handmatig worden gestart voordat u de toepassing kunt gebruiken.
