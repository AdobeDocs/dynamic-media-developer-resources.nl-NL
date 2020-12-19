---
description: Gebruikersgegevens uit afbeeldingscatalogus. Retourneert gebruikersgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-description: Gebruikersgegevens uit afbeeldingscatalogus. Retourneert gebruikersgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-title: gebruikersgegevens
solution: Experience Manager
title: gebruikersgegevens
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# userdata{#userdata}

Gebruikersgegevens uit afbeeldingscatalogus. Retourneert gebruikersgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=userdata[,text|{xml[, *`coderen`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coderen</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

De inhoud van `catalog::UserData` wordt geretourneerd. Als de indeling &#39;text&#39; is opgegeven, worden alle exemplaren van `??` in `catalog::UserData`vervangen door regeleindes en wordt aan het einde een enkele regeleindteken (CR/LF) toegevoegd. Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord uit slechts één regeleinde. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

Andere opdrachten in de tekenreeks request worden genegeerd.

De reactie van HTTP is cacheable met TTL die op `catalog::Expiration` wordt gebaseerd.

>[!NOTE]
>
>Het dubbele teken is niet toegestaan in sleutelnamen van gebruikerseigenschappen.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.
