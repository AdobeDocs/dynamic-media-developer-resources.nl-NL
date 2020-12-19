---
description: Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
seo-description: Foutbericht met details. Geeft het detailniveau voor foutberichten op die via HTTP worden geretourneerd als de error.message-waarde.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '180'
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
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Korte boodschap. Gereserveerd voor toekomstig gebruik. Retourneert momenteel dezelfde informatie als 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Gedetailleerd bericht. Verstrekt gebruiker-vlakke details over de fout. Kan vertrouwelijke informatie bevatten, zoals bestandspaden. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Volledige foutopsporingsinformatie. Voegt Java-stacktraceringen toe, indien van toepassing. Foutafbeeldingen bevatten nooit stacktraces en retourneren in plaats daarvan niveau 2-informatie in <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Niveau 0 wordt geadviseerd voor levende servers die openbaar kunnen worden betreden.
* Niveau 2 wordt aanbevolen voor testservers, kwaliteitsborgingsservers en toepassingsontwikkelingsservers.
* Informatie van niveau 3 kan nuttig zijn bij het melden van problemen aan de Technische Steun van Scene7.

## Eigenschappen {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Opsommende waarde, moet 0, 1, 2 of 3 zijn.

## Standaard {#section-5e78d550050840cc9a1de811c581b94f}

Overgenomen van `default::ErrorDetail` indien niet opgegeven of indien leeg.

## Zie ook {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
