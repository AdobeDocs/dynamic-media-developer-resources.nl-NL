---
title: ErrorDetail
description: Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# ErrorDetail{#errordetail}

Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.

## Titel {#section-c10d75d72ee24d16a67cc8d927f1deba}

De volgende waarden zijn toegestaan:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Alleen titel. Geeft een korte algemene beschrijving van de fout. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Korte boodschap. Gereserveerd voor toekomstig gebruik. Retourneert momenteel dezelfde informatie als 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Gedetailleerd bericht. Verstrekt gebruiker-vlakke details over de fout. Kan vertrouwelijke informatie bevatten, zoals bestandspaden. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Volledige foutopsporingsinformatie. Voegt Java™-stacksporen toe, indien van toepassing. Foutafbeeldingen bevatten nooit stapelsporen en retourneren in plaats daarvan niveau 2-informatie in <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Niveau 0 wordt geadviseerd voor levende servers die openbaar kunnen worden betreden.
* Niveau 2 wordt aanbevolen voor testservers, kwaliteitsborgingsservers en toepassingsontwikkelingsservers.
* Informatie van niveau 3 kan nuttig zijn bij het melden van problemen aan technische ondersteuning van Dynamic Media.

## Eigenschappen {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Opsommende waarde, moet 0, 1, 2 of 3 zijn.

## Standaard {#section-5e78d550050840cc9a1de811c581b94f}

Overgenomen van `default::ErrorDetail` indien niet opgegeven of indien leeg.

## Zie ook {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
