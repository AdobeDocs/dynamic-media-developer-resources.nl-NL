---
description: Nieuwe batchtaak verzenden.
seo-description: Nieuwe batchtaak verzenden.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Scene7 Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 65cf517cb75d35cbd3761397ee99d1d8ec074ad6
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

---


# batchjobsubmit{#batchjobsubmit}

Nieuwe batchtaak verzenden.

Deze parameter:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>XML-fragment met volledige taakgegevens. </p> </td> 
 </tr> 
</table>

Retourneert:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Status van het werk </p> </td> 
  <td class="stentry"> <p>Of indiening is geslaagd of mislukt; als dit lukt, moet de taak-id de XML-indeling hebben. </p> </td> 
 </tr> 
</table>

## Voorbeeld {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
