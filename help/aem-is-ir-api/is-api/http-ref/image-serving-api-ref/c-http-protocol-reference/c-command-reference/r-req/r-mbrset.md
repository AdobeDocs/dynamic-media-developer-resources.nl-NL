---
description: Gegevens met meerdere bitsnelheden.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# mbrSet{#mbrset}

Gegevens met meerdere bitsnelheden.

`req=mbrSet[,text|xml[, *`coderen`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coderen</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Retourneert een tekst- of xml-reactie die een lijst bevat met URL&#39;s (en bijbehorende bitsnelheden) die overeenkomen met geldige video-items in een videoset die is gekoppeld aan netto-pad-id.

De vorige vereiste dat een geldig video-item een waarde bevat voor `catalog::VideoBitRate` is nu versoepeld. Het item kan een waarde bevatten voor `catalog::VideoBitRate`*of* `catalog::AudioBitRate`*of* `catalog::TotalStreamBitRate`. Het video-item is alleen geldig als een van deze waarden is gedefinieerd. De voorschriften voor `catalog::Path` en een geldige videobestandsextensie is niet gewijzigd.

Reacties zijn bedoeld voor gebruik door Apple en Flash-streaming servers en voldoen dus structureel aan deze specificaties. URL&#39;s worden met voorvoegsels gegenereerd `attribute::HttpAppleStreamingContext` en `attribute::HttpFlashStreamingContext`.

m3u8-reacties bevatten alleen MP4-bestanden, als deze aanwezig zijn in de videoset. Als er geen MP4-bestanden aanwezig zijn, bevatten deze reacties alleen f4v-bestanden. Als er geen MP4-bestanden of f4v-bestanden aanwezig zijn, is de reactie leeg.

f4m-reacties bevatten alleen f4v-bestanden als deze aanwezig zijn in de videoset. Als er geen f4v-bestanden aanwezig zijn, bevatten deze reacties alleen MP4-bestanden. Als er geen f4v-bestanden of MP4-bestanden aanwezig zijn, is de reactie leeg.

De bitsnelheden die worden weergegeven in f4m/m3u8-reacties komen overeen met de waarden in `catalog::TotalStreamBitRate` (omgezet in de juiste eenheden). Indien `catalog::TotalStreamBitRate` niet is gedefinieerd, de som van `catalog::VideoBitRate` en `catalog::AudioBitRate` wordt gebruikt.

De HTTP-respons is cacheable met de TTL op basis van `catalog::NonImgExpiration`.
