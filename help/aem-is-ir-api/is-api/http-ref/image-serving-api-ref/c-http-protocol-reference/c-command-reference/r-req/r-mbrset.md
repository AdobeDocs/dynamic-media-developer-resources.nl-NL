---
description: Gegevens met meerdere bitsnelheden.
seo-description: Gegevens met meerdere bitsnelheden.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# mbrSet{#mbrset}

Gegevens met meerdere bitsnelheden.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

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

De vorige vereiste dat een geldig video-item een waarde voor `catalog::VideoBitRate` bevat, is nu versoepeld. Het item kan een waarde bevatten voor `catalog::VideoBitRate`*of* `catalog::AudioBitRate`*of* `catalog::TotalStreamBitRate`. Het video-item is alleen geldig als een van deze waarden is gedefinieerd. De vereisten voor `catalog::Path` en een geldige videobestandsextensie zijn niet gewijzigd.

Reacties zijn bedoeld voor gebruik door Apple en Flash Streaming Servers en voldoen dus structureel aan deze specificaties. URL&#39;s worden gegenereerd met behulp van voorvoegsels `attribute::HttpAppleStreamingContext` en `attribute::HttpFlashStreamingContext`.

m3u8-reacties bevatten alleen MP4-bestanden, als deze aanwezig zijn in de videoset. Als er geen MP4-bestanden aanwezig zijn, bevatten deze reacties alleen f4v-bestanden. Als er geen MP4-bestanden of f4v-bestanden aanwezig zijn, is de reactie leeg.

f4m-reacties bevatten alleen f4v-bestanden als deze aanwezig zijn in de videoset. Als er geen f4v-bestanden aanwezig zijn, bevatten deze reacties alleen MP4-bestanden. Als er geen f4v-bestanden of MP4-bestanden aanwezig zijn, is de reactie leeg.

De bitsnelheden die worden weergegeven in f4m/m3u8-reacties komen overeen met de waarden in `catalog::TotalStreamBitRate` (omgezet in de juiste eenheden). Wanneer `catalog::TotalStreamBitRate` niet is gedefinieerd, wordt de som van `catalog::VideoBitRate` en `catalog::AudioBitRate` gebruikt.

De reactie van HTTP is cacheable met TTL die op `catalog::NonImgExpiration` wordt gebaseerd.
