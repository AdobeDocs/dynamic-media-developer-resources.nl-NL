---
description: Zoomen is gericht op gegevens uit afbeeldingscatalogus. Hiermee worden zoomdoelgegevens geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-description: Zoomen is gericht op gegevens uit afbeeldingscatalogus. Hiermee worden zoomdoelgegevens geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-title: streefdoelen
solution: Experience Manager
title: streefdoelen
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# streefdoelen{#targets}

Zoomen is gericht op gegevens uit afbeeldingscatalogus. Hiermee worden zoomdoelgegevens geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

De inhoud van `catalog::Targets` wordt geretourneerd. Wanneer de opmaak &#39;text&#39; wordt aangevraagd, worden alle exemplaren van `??` de opmaak vervangen door regeleindes en wordt één regeleindteken ( `catalog::Targets` `CR/LF`) toegevoegd. Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord uit slechts één regeleinde. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

Andere opdrachten in de tekenreeks request worden genegeerd.

De reactie van HTTP is cacheable met TTL gebaseerd op `catalog::Expiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is dit `s7jsonResponse`.
