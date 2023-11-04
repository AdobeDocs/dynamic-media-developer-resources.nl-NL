---
description: Zoomen is gericht op gegevens uit afbeeldingscatalogus. Hiermee worden zoomdoelgegevens geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
solution: Experience Manager
title: streefdoelen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# streefdoelen{#targets}

Zoomen is gericht op gegevens uit afbeeldingscatalogus. Hiermee worden zoomdoelgegevens geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=targets[,text|{xml[, *`coderen`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

De inhoud van `catalog::Targets` worden geretourneerd. Wanneer de opmaak &#39;text&#39; wordt aangevraagd, worden alle varianten van `??` in `catalog::Targets` worden vervangen door regeleinde en een regeleinde ( `CR/LF`) aan het einde wordt toegevoegd. Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord alleen uit een terminator met één regel. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

Andere opdrachten in de tekenreeks request worden genegeerd.

De HTTP-respons is cacheable met de TTL op basis van `catalog::Expiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.
