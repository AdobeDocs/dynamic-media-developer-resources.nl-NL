---
description: Het playlognut kan worden gebruikt om inhoud voor het de reactiecache van HTTP vooraf te produceren.
seo-description: Het playlognut kan worden gebruikt om inhoud voor het de reactiecache van HTTP vooraf te produceren.
seo-title: Het hulpprogramma 'playlog'
solution: Experience Manager
title: Het hulpprogramma 'playlog'
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Het hulpprogramma &#39;playlog&#39;{#the-playlog-utility}

Het playlognut kan worden gebruikt om inhoud voor het de reactiecache van HTTP vooraf te produceren.

De bestaande Image Serving HTTP response cache is niet bruikbaar na een belangrijke versieverbetering (wanneer het eerste of tweede cijfer van het versienummer is gewijzigd). Als de server live naar de volledige-laadvoorwaarden na de upgrade moet worden gebracht, kan de server overbelast raken met de eerste paar uur van verzoeken van het cachegeheugen die ontbreken totdat de cache redelijk gevuld is en de aanraaksnelheid in het cachegeheugen toeneemt.

Om deze eerste laadpunt te voorkomen, kunt u het hulpprogramma `playlog` gebruiken om inhoud voor de HTTP-responscache vooraf te genereren. `playlog` haalt HTTP- verzoeken uit een bestaand dossier van het toegangslogboek en verzendt het naar de server om geheim voorgeheugeningangen te produceren. Voor typische gebruiksscenario&#39;s, is het voldoende om één enkel dossier van het toegangslogboek terug te spelen dat een waarde van het volledige dagverkeer bevat.

Naast het primeren van het HTTP-responscache na upgradeinstallaties, wordt het hulpprogramma ook gebruikt om cacheinhoud vooraf te genereren wanneer een nieuwe server wordt toegevoegd aan een omgeving die evenwichtig is verdeeld over de taken. speel eenvoudig een recent logboekdossier van één van de andere servers terug.

`playlog` kan worden gevormd om de meeste dossiers van het toegangslogboek te steunen die door vroegere versies van Beeld worden geproduceerd die.

## Gebruik {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p,  <span class="varname"> voorvoegsel  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL van hoofdmap die wordt gebruikt als voorbereiding op de aanvragen die uit het logbestand worden geëxtraheerd. </p> <p>Standaard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>veldnummer (kolom) dat de aanvraag in de logboeken bevat; 1. </p> <p>Standaard: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s- <span class="varname"> scheidingsteken  </span> </span> </p> </td> 
  <td class="stentry"> <p>Veldscheidingsteken; reguliere-expressiepatroon. </p> <p>Standaard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> markering  </span> </span> </p> </td> 
  <td class="stentry"> <p>Aanvraagmarkering; de in het logbestand vermelde verzoeken die moeten worden afgespeeld; reguliere-expressiepatroon. </p> <p>Standaard: <span class="codeph"> Verzoek: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> achtervoegsel  </span> </span> </p> </td> 
  <td class="stentry"> <p>Achtervoegsel dat aan het verzoek wordt toegevoegd dat uit het logbestand wordt gehaald; kan worden gebruikt om afspeelverzoeken te scheiden van live-aanvragen in de logbestanden; a '? of het scheidingsteken '&amp;' automatisch wordt ingevoegd; Het achtervoegsel kan naar elk logveld verwijzen op positie binnen accolades. De standaardwaarde komt overeen met het handtekeningveld md5. </p> <p>Standaard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>In de modus Uitgebreid worden de gegenereerde verzoek-URL's afgedrukt naar <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Druk een synopsis aan <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r  </span> </p> </td> 
  <td class="stentry"> <p>request-method - HTTP request method to use ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standaard: <span class="codeph"> slim </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o  </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos in logboekdossier om originele methode van te pakken. </p> <p>Standaard: 15 </p> </td> 
 </tr> 
</table>

Voor Windows is de bestandsnaam [!DNL playlog.bat] en voor Linux [!DNL playlog.sh].

## Voorbeelden {#section-716e5c35e9fa4ee3a4b0687381fcea40}

In het volgende voorbeeld worden alle aanvragen afgespeeld van een toegangslogbestand dat is gemaakt door Image Serving op Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Het volgende bevel speelt alle verzoeken terug die in een dossier van het spoorlogboek worden gevonden dat door Beeld dat op Vensters wordt dienen wordt gecreeerd:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
