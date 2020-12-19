---
description: Validatie aanvragen.
seo-description: Validatie aanvragen.
seo-title: validate
solution: Experience Manager
title: validate
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# validate{#validate}

Validatie aanvragen.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

Parseert de aanvraagtekenreeks alsof `req=img` is opgegeven, maar zonder variabelen te vervangen en objecten waarnaar wordt verwezen (afbeeldingen, ICC-profielen, lettertypen, enzovoort) te evalueren. De standaardfoutreactie wordt geretourneerd als parseren mislukt, anders wordt de volgende eigenschap geretourneerd:

`request.isValid=1`

De HTTP-respons is niet cacheable.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.
