---
description: Afbeeldingskaartgegevens.
solution: Experience Manager
title: map
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# map{#map}

Afbeeldingskaartgegevens.

`req=map[,text|{xml[, *`coderen`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

Retourneert `catalog::Map` zonder wijzigingen wanneer een eenvoudig item in een catalogus wordt opgevraagd waarvoor geen aanvullende opdrachten zijn opgegeven (wordt niet geschaald naar `catalog::maxPix`).

Als er andere opdrachten zijn opgegeven in de aanvraag, wordt een samengestelde afbeelding met hyperlinks geretourneerd. Deze worden verkregen door alle opdrachten te schalen, uit te snijden, te roteren en in lagen te plaatsen `catalog::Map` en/of `map=` opdrachten die in de aanvraag zijn opgenomen, net als de afbeeldingsgegevens `req=img`.

Opgeven `text` of laat de tweede parameter weg om de gegevens van de beeldkaart in de vorm van een `HTML <AREA>` elementtekenreeks met MIME-type reactie `text/plain`.

Opgeven `xml` om de reactie op te maken als XML in plaats van als HTML. U kunt desgewenst tekstcodering opgeven. De standaardwaarde is `UTF-8`.

Retourneert een lege tekenreeks (of leeg) `<AREA>` element) als er geen kaartgegevens zijn gevonden voor de opgegeven catalogusobjecten, en/of als er geen toewijzingsgegevens zijn gevonden `<AREA>` blijven na het uitsnijden van de afbeeldingen.

De HTTP-respons is cacheable met de TTL op basis van `catalog::Expiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.

Zie [Afbeeldingen met hyperlinks](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
