---
description: Modus Nieuwe pixels berekenen. Kies het algoritme voor resampling en/of interpolatie dat u wilt gebruiken voor het schalen van afbeeldingsgegevens. Dit is ook van toepassing op het roteren van tekstlagen en het wijzigen van de grootte van samengestelde afbeeldingen tijdens het transformeren van de weergave.
seo-description: Modus Nieuwe pixels berekenen. Kies het algoritme voor resampling en/of interpolatie dat u wilt gebruiken voor het schalen van afbeeldingsgegevens. Dit is ook van toepassing op het roteren van tekstlagen en het wijzigen van de grootte van samengestelde afbeeldingen tijdens het transformeren van de weergave.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# resMode{#resmode}

Modus Nieuwe pixels berekenen. Kies het algoritme voor resampling en/of interpolatie dat u wilt gebruiken voor het schalen van afbeeldingsgegevens. Dit is ook van toepassing op het roteren van tekstlagen en het wijzigen van de grootte van samengestelde afbeeldingen tijdens het transformeren van de weergave.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u de standaard bi-lineaire interpolatie. Snelste methode voor het berekenen van nieuwe monsters; sommige aliasingartefacten kunnen waarneembaar zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert bi-cubische interpolatie. Meer CPU-intensief dan bi-lineaire interpolatie, maar levert scherpere beelden op met minder merkbare aliasing-artefacten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert een gewijzigde functie van het Venster Lanczos als interpolatiealgoritme. Dit levert mogelijk iets scherpere resultaten op dan bi-cubisch tegen hogere CPU-kosten. <span class="codeph"> scherp  </span> is vervangen door  <span class="codeph"> shark2  </span>, waardoor het minder waarschijnlijk is dat aliasing artefacten (Moiré) wordt veroorzaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u Photoshop standaardreampler voor het reduceren van de afbeeldingsgrootte, de zogenaamde 'bicubische scherper' in Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-a171bacf4ddf43c782e46b86a16d443e}

Request-kenmerk. Is van toepassing op alle schaalbewerkingen die nodig zijn voor het maken van de uiteindelijke antwoordafbeelding, inclusief alle laagschaling.

## Standaard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Voorbeeld {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Hiermee wordt een kwalitatief hoogstaande uitvoering opgehaald van een gelaagde afbeelding die in een afbeeldingscatalogus is opgeslagen. De afbeelding kan tekst bevatten. We verwachten dat u verder gaat met het bewerken van afbeeldingen en dus een alfakanaal bij de afbeelding aanvraagt.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Zie ook {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[kenmerk:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
