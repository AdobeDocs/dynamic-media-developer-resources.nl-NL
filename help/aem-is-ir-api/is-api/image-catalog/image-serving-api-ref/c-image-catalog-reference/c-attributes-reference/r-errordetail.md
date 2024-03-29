---
description: Foutbericht Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 2%

---

# ErrorDetail{#errordetail}

Foutbericht Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.

De volgende waarden zijn toegestaan:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Alleen titel. Geeft een korte algemene beschrijving van de fout. Aanbevolen voor live servers die openbaar toegankelijk zijn. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Korte boodschap. Gereserveerd voor toekomstig gebruik. Retourneert momenteel dezelfde informatie als 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Gedetailleerd bericht. Verstrekt gebruiker-vlakke details over de fout. Kan vertrouwelijke informatie bevatten, zoals bestandspaden. Aanbevolen voor testservers, kwaliteitsborgingsservers en toepassingsontwikkelingsservers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Volledige foutopsporingsinformatie. Voegt Java-stapelsporen toe, indien van toepassing. Foutafbeeldingen bevatten nooit stapelsporen en retourneren in plaats daarvan niveau 2-informatie in <span class="codeph"> $error.message</span>. Deze informatie kan nuttig zijn bij het melden van problemen aan technische ondersteuning van Dynamic Media. </p></td> 
 </tr> 
</table>

## Eigenschappen {#section-e167895723ca4ad4ba283d3d7b4324de}

Opsommende waarde, moet 0, 1, 2 of 3 zijn.

## Standaard {#section-8f27098e509945a18676aca0675c8f41}

Overgenomen van `default::ErrorDetail` indien niet opgegeven of indien leeg.

## Zie ook {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
