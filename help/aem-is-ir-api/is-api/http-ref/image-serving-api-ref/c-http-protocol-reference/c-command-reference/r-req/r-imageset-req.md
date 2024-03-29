---
description: Afbeeldingssetgegevens uit afbeeldingscatalogus. Retourneert de afbeeldingssetgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# imageset{#imageset}

Afbeeldingssetgegevens uit afbeeldingscatalogus. Retourneert de afbeeldingssetgegevens voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=imageset[,text|javascript|{xml[, *`coderen`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

De inhoud van `catalog::ImageSet` wordt geretourneerd zonder verdere wijziging (behalve tekenreekslokalisatie, indien van toepassing), gevolgd door een single-line terminator (CR/LF). Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord alleen uit een terminator met één regel.

Andere opdrachten in de tekenreeks request worden genegeerd. De HTTP-respons is cacheable met de TTL op basis van `catalog::NonImgExpiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.
