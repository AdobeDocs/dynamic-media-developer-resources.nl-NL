---
description: Afbeeldingskaartgegevens.
seo-description: Afbeeldingskaartgegevens.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# map{#map}

Afbeeldingskaartgegevens.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

Retourneert `catalog::Map` zonder wijziging wanneer een eenvoudig item in de catalogus wordt opgevraagd zonder dat er aanvullende opdrachten zijn opgegeven (wordt niet geschaald naar `catalog::maxPix`).

Als er andere opdrachten in de aanvraag worden opgegeven, wordt een samengestelde afbeelding met hyperlinks geretourneerd. Deze map wordt afgeleid door alle `catalog::Map` en/of `map=` opdrachten in de aanvraag te schalen, uit te snijden, te roteren en in lagen te plaatsen, net als de afbeeldingsgegevens worden gebruikt `req=img`.

Geef de tweede parameter op `text` of laat deze weg om de afbeeldingskaartgegevens te retourneren in de vorm van een `HTML <AREA>` elementtekenreeks met het MIME-type response `text/plain`.

Geef op `xml` om de reactie op te maken als XML in plaats van HTML. U kunt desgewenst tekstcodering opgeven. De standaardwaarde is `UTF-8`.

Retourneert een lege tekenreeks (of leeg `<AREA>` element) als er geen kaartgegevens zijn gevonden voor de opgegeven catalogusobjecten en/of als er geen `<AREA>` elementen overblijven na het uitsnijden van de afbeeldingen.

De reactie van HTTP is cacheable met TTL gebaseerd op `catalog::Expiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is dit `s7jsonResponse`.

Zie [Afbeeldingen met hyperlinks](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
