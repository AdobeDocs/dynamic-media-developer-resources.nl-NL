---
description: Afbeeldingssetgegevens uit afbeeldingscatalogus. Hiermee worden de gegevens van de afbeeldingsset geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-description: Afbeeldingssetgegevens uit afbeeldingscatalogus. Hiermee worden de gegevens van de afbeeldingsset geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---


# imageset{#imageset}

Afbeeldingssetgegevens uit afbeeldingscatalogus. Hiermee worden de gegevens van de afbeeldingsset geretourneerd voor het item van de afbeeldingscatalogus dat is opgegeven in het URL-pad.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

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

De inhoud van `catalog::ImageSet` wordt zonder verdere wijziging geretourneerd (behalve tekenreekslokalisatie, indien van toepassing), gevolgd door één regelafsluiter (CR/LF). Als het URL-pad niet wordt omgezet in een geldig catalogusitem, bestaat het antwoord uit slechts één regeleinde.

Andere opdrachten in de tekenreeks request worden genegeerd. De reactie van HTTP is cacheable met TTL die op `catalog::NonImgExpiration` wordt gebaseerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.
