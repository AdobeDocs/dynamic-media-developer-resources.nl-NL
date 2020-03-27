---
description: Informatie over mediaset.
seo-description: Informatie over mediaset.
seo-title: set
solution: Experience Manager
title: set
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# set{#set}

Informatie over mediaset.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coderen</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id </p></td> 
 </tr> 
</table>

Retourneert informatie over afbeeldingen, video&#39;s, stalen en verschillende metagegevens die zijn gekoppeld aan de catalogus::ImageSet voor de afbeeldingscatalogus die is opgegeven in het URL-pad. Deze reactie is een hiërarchische structuur zoals die door het verstrekte type van reeks wordt bepaald. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

De reactie van HTTP is cacheable met TTL gebaseerd op `catalog::NonImgExpiration`.

>[!NOTE]
>
>Het dubbele punt wordt niet toegestaan in req=set verzoeken.

Verzoeken die JSON reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van manager JS aanwezig in de reactie JSONP. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is dit `s7jsonResponse`.
