---
description: Informatie over mediaset.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# set{#set}

Informatie over mediaset.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coderen</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id </p></td> 
 </tr> 
</table>

Retourneert informatie over afbeeldingen, video&#39;s, stalen en verschillende metagegevens die zijn gekoppeld aan de catalogus::ImageSet voor de afbeeldingscatalogus die is opgegeven in het URL-pad. Deze reactie is een hiërarchische structuur zoals die door het verstrekte type van reeks wordt bepaald. De juiste opmaak wordt toegepast wanneer de bestandsindeling xml of json wordt aangevraagd.

De HTTP-respons is cacheable met de TTL op basis van `catalog::NonImgExpiration`.

>[!NOTE]
>
>Het dubbele punt wordt niet toegestaan in req=set verzoeken.

Verzoeken die JSON reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van manager JS aanwezig in de reactie JSONP. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.
