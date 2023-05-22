---
description: Gebruikersgegevens uit afbeeldingscatalogus. Retourneert gebruikersgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
solution: Experience Manager
title: gebruikersgegevens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# gebruikersgegevens{#userdata}

Gebruikersgegevens uit afbeeldingscatalogus. Retourneert gebruikersgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=userdata[,text|{xml[, *`coderen`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coderen</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

De inhoud van `catalog::UserData` worden geretourneerd. Wanneer de opmaak &#39;text&#39; is opgegeven, worden alle instanties van `??` in `catalog::UserData`worden vervangen door regeleinde en aan het einde wordt één regeleinde (CR/LF) toegevoegd. Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord uit slechts één regeleinde. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

Andere opdrachten in de tekenreeks request worden genegeerd.

De HTTP-respons is cacheable met de TTL op basis van `catalog::Expiration`.

>[!NOTE]
>
>Het dubbele teken is niet toegestaan in sleutelnamen van gebruikerseigenschappen.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.
