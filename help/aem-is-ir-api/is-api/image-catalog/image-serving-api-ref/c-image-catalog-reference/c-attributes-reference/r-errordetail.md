---
description: Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
seo-description: Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---


# ErrorDetail{#errordetail}

Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.

De volgende waarden zijn toegestaan:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Alleen titel. Geeft een korte algemene beschrijving van de fout. Aanbevolen voor live servers die openbaar toegankelijk zijn. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Korte boodschap. Gereserveerd voor toekomstig gebruik. Retourneert momenteel dezelfde informatie als 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Gedetailleerd bericht. Verstrekt gebruiker-vlakke details over de fout. Kan vertrouwelijke informatie bevatten, zoals bestandspaden. Aanbevolen voor testservers, kwaliteitsborgingsservers en toepassingsontwikkelingsservers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Volledige foutopsporingsinformatie. Voegt Java-stacktraceringen toe, indien van toepassing. Foutafbeeldingen bevatten nooit stacktraces en retourneren in plaats daarvan niveau 2-informatie in <span class="codeph"> $error.message</span>. Deze informatie kan nuttig zijn wanneer het melden van problemen aan de Technische Steun van Scene7. </p></td> 
 </tr> 
</table>

## Eigenschappen {#section-e167895723ca4ad4ba283d3d7b4324de}

Opsommende waarde, moet 0, 1, 2 of 3 zijn.

## Standaard {#section-8f27098e509945a18676aca0675c8f41}

Overgenomen van `default::ErrorDetail` indien niet opgegeven of indien leeg.

## Zie ook {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
