---
description: Modus Nieuwe pixels berekenen. Kies het algoritme voor resampling en/of interpolatie dat u wilt gebruiken voor het schalen van afbeeldingsgegevens. Dit is ook van toepassing op het roteren van tekstlagen en het wijzigen van de grootte van samengestelde afbeeldingen tijdens het transformeren van de weergave.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# resMode{#resmode}

Modus Nieuwe pixels berekenen. Kies het algoritme voor resampling en/of interpolatie dat u wilt gebruiken voor het schalen van afbeeldingsgegevens. Dit is ook van toepassing op het roteren van tekstlagen en het wijzigen van de grootte van samengestelde afbeeldingen tijdens het transformeren van de weergave.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u de standaard bi-lineaire interpolatie. Snelste methode voor het berekenen van nieuwe monsters; er zijn enkele aliasingartefacten waarneembaar . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert bi-cubische interpolatie. Meer CPU-intensief dan bi-lineaire interpolatie, maar geeft scherpere beelden met minder merkbare aliasing artefacten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Selecteert een gewijzigde functie van het Venster Lanczos als interpolatiealgoritme. Dit levert iets scherpere resultaten op dan bi-cubisch tegen hogere CPU-kosten. <span class="codeph"> scherp  </span> is vervangen door  <span class="codeph"> shark2  </span>, waardoor het minder waarschijnlijk is dat aliasing artefacten (Moiré) wordt veroorzaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee selecteert u Photoshop standaardreampler voor het reduceren van de afbeeldingsgrootte, de zogenaamde 'bicubische scherper' in Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Als u de hoogte-breedteverhouding van een afbeelding wilt behouden wanneer u zowel `resMode=bisharp` als `fit=stretch` gebruikt, kunt u het beste de parameter width of de parameter height gebruiken. Als beide parameters moeten worden gedefinieerd, kunt u ze in een andere laag plaatsen, zoals in het volgende voorbeeld wordt getoond:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Eigenschappen {#section-a171bacf4ddf43c782e46b86a16d443e}

Request-kenmerk. Is van toepassing op alle schaalbewerkingen die nodig zijn voor het maken van de uiteindelijke antwoordafbeelding, inclusief alle laagschaling.

## Standaard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Voorbeeld {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Hiermee wordt een kwalitatief hoogstaande uitvoering opgehaald van een gelaagde afbeelding die in een afbeeldingscatalogus is opgeslagen. De afbeelding kan tekst bevatten. De afbeelding wordt verder verwerkt in een beeldbewerkingstoepassing en vraagt dus om een alfakanaal met de afbeelding.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Zie ook {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[kenmerk:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
