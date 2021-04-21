---
description: Afbeeldingskaartgegevens.
solution: Experience Manager
title: map
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# map{#map}

Afbeeldingskaartgegevens.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

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

Retourneert `catalog::Map` zonder wijziging wanneer een item in een eenvoudige catalogus wordt opgevraagd zonder dat er aanvullende opdrachten zijn opgegeven (wordt niet geschaald naar `catalog::maxPix`).

Als er andere opdrachten in de aanvraag worden opgegeven, wordt een samengestelde afbeelding met hyperlinks geretourneerd. Deze wordt verkregen door alle `catalog::Map`- en/of `map=`-opdrachten in de aanvraag te schalen, uit te snijden, te roteren en in lagen te plaatsen, net zoals de afbeeldingsgegevens met `req=img` zijn.

Geef `text` op of laat de tweede parameter weg om de afbeeldingskaartgegevens te retourneren in de vorm van een `HTML <AREA>`-elementtekenreeks met het MIME-responstype `text/plain`.

Geef `xml` op om de reactie op te maken als XML in plaats van HTML. U kunt desgewenst tekstcodering opgeven. De standaardwaarde is `UTF-8`.

Retourneert een lege tekenreeks (of leeg `<AREA>`-element) als er geen toewijzingsgegevens zijn gevonden voor de opgegeven catalogusobjecten en/of als er geen `<AREA>`-elementen overblijven na het uitsnijden van de afbeeldingen.

De reactie van HTTP is cacheable met TTL die op `catalog::Expiration` wordt gebaseerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

Zie [Afbeeldingskaarten](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
