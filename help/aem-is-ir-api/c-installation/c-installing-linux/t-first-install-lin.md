---
title: Voor het eerst installeren
description: Deze procedure laat zien hoe u Image Serving voor het eerst kunt installeren op Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Voor het eerst installeren{#installing-for-the-first-time}

Deze procedure laat zien hoe u Image Serving voor het eerst kunt installeren op Linux®.

1. Meld u aan bij de serverhost met basismachtigingen.
1. De map maken [!DNL /usr/local/scene7/licenses].

   Als het bestand met de licentiecode voor Beeldbewerking en/of Afbeelding renderen (met [!DNL .sc8] bestandsachtervoegsel) beschikbaar is. Kopieer het bestand naar deze map. Anders gaat u verder met de installatie en installeert u de licentiecode later.
1. Decomprimeer en verwijder het Teerbestand voor distributie van Image Serving.
1. In de [!DNL Setup] map, start de installatiewizard door [!DNL ./install-is].

   Als er geen licentiecode wordt gevonden, worden instructies weergegeven die beschrijven hoe u een licentiebestand kunt verkrijgen. Doe dit op dit moment of ga verder met de installatie van Image Serving en installeer de licentiecode later.
1. Wanneer de licentieovereenkomst voor eindgebruikers (EULA) wordt weergegeven, leest u de licentieovereenkomst en voert u vervolgens de licentieovereenkomst in `y` om verder te gaan.

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
   <td colname="col2"> <p>De gebruikersaccount waaronder de Image Serving-server moet worden geïnstalleerd. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Id van afbeeldingsservergroep [root]:</span> </p> </td>
   <td colname="col2"> <p>De groepsaccount waaronder de Image Serving-server moet worden geïnstalleerd. </p> </td>
  </tr>
 </tbody>
</table>

1. Druk **[!UICONTROL Enter]** om de standaardwaarde te accepteren of een andere waarde op te geven.

   Zorg ervoor dat alle opgegeven poortnummers uniek zijn en niet op een andere manier op deze host worden gebruikt.

   >[!IMPORTANT]
   >
   >Als een andere rekening dan wortel wordt gespecificeerd, moet u ervoor zorgen dat de toegangstoestemmingen voor alle dossiers en omslagen de Server van het Beeld moet lezen en schrijven, correct opstelling zijn wanneer deze omslagen in de configuratiedossiers worden aangepast.
   >
   >Beeldserver is nu geïnstalleerd op [!DNL /usr/local/Scene7/ImageServing]. Bepaalde inhoud voor het renderen van afbeeldingen is geïnstalleerd op [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Tegen het einde van de installatie probeert de installatiewizard Image Server te starten. Als er geen geldige licentiecode wordt gevonden, kan de imageserver niet worden gestart. Als er een geldige vergunning is en de Server van het Beeld niet opstelling is, raadpleeg de logboekdossiers.

>[!NOTE]
>
>Als de licentie na de installatie van Image Serving is geïnstalleerd, moet de Image Server handmatig worden gestart voordat u het image kunt gebruiken.
