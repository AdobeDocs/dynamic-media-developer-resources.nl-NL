---
title: dpr
description: DPR (Device Pixel Ratio)&mdash;ook wel CSS-pixelverhouding&mdash genoemd;is de relatie tussen de fysieke pixels van een apparaat en logische pixels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# dpr{#dpr}

De pixelverhouding van het apparaat (DPR), ook wel CSS-pixelverhouding genoemd, is de verhouding tussen de fysieke pixels van een apparaat en logische pixels. Vooral met de komst van Retina-schermen groeit de pixelresolutie van moderne mobiele apparaten snel.

Als u de pixelverhouding van het apparaat inschakelt, wordt de afbeelding weergegeven met de oorspronkelijke resolutie van het scherm, waardoor deze scherp wordt.

Momenteel is de pixeldichtheid van het beeldscherm afkomstig van Akamai CDN-headerwaarden.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> uit </span> </span> </p> </td> 
  <td class="stentry"> <p>Schakel DPR-optimalisatie op individueel afbeeldings-URL-niveau uit. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Overschrijf de DPR-waarde die door Smart Imaging wordt gedetecteerd, met een aangepaste waarde (zoals wordt gedetecteerd door elke logica aan de clientzijde of andere methode). Toegestane waarde voor dprValue is een getal groter dan 0. </p> </td> 
 </tr> 
</table>


U kunt `dpr=on,dprValue` zelfs als het bedrijf de DPR-instelling als uitgeschakeld heeft.

Als de resulterende afbeelding door DPR-optimalisatie groter is dan de Dynamic Media-instelling MaxPix, wordt de breedte van MaxPix altijd herkend door de hoogte-breedteverhouding van de afbeelding te behouden.

| Aangevraagde afbeeldingsgrootte | DPR-waarde | Afgeleverde afbeeldingsgrootte |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

## Eigenschappen



## Standaard

`dpr=off`


## Voorbeeld

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Zie ook

[netwerk](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Slimme afbeeldingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)